📘 Curso: Integración de APIs con Python, FastAPI y Vimeo
🟢 Clase 2 – Pydantic y Estructura Profesional del Proyecto

Duración: 2 horas
Fecha: Miércoles 17
Horario: 7:30 p. m. – 9:30 p. m.
Modalidad: Práctica guiada

🎯 Objetivo de la Clase

Que el alumno:

Comprenda qué es Pydantic y por qué se utiliza en FastAPI.

Aprenda a validar datos de entrada y salida.

Entienda una estructura profesional de proyecto FastAPI.

Relacione cada carpeta del proyecto con su responsabilidad.

📂 Estructura del Proyecto (Estado Actual)

La clase parte de una estructura ya definida y funcional:

vimeo/
├── app/
│   ├── api/
│   │   └── routes/
│   │       └── videos.py
│   ├── core/
│   │   ├── config.py
│   │   └── logging.py
│   ├── schemas/
│   │   └── video.py
│   ├── services/
│   │   └── vimeo_client.py
│   └── main.py
├── docker/
│   ├── Dockerfile
│   ├── run_all.sh
│   └── set_env_secrets.sh
├── tests/
│   ├── conftest.py
│   └── test_videos.py
├── .env
├── README.md
└── requirements.txt

1️⃣ ¿Qué es Pydantic?

Pydantic es una librería que permite:

Definir la estructura de los datos.

Validar automáticamente el contenido recibido.

Evitar errores por datos mal formados.

Generar documentación clara en Swagger.

📌 FastAPI utiliza Pydantic de forma nativa.

2️⃣ ¿Por qué NO usar dict directamente?

En la Clase 1 se usó:

def crear_video(data: dict):
    ...

Problemas de este enfoque:

No hay validación.

Se aceptan datos incorrectos.

Swagger no documenta correctamente.

👉 Pydantic soluciona estos problemas.

3️⃣ Creación de un Schema con Pydantic

📄 app/schemas/video.py

from pydantic import BaseModel
from typing import Optional

class VideoCreate(BaseModel):
    title: str
    description: Optional[str] = None
    is_public: bool = True

Explicación:

BaseModel: clase base de Pydantic.

title: obligatorio.

description: opcional.

is_public: valor por defecto.

4️⃣ Uso del Schema en un Endpoint

📄 app/api/routes/videos.py

from fastapi import APIRouter
from app.schemas.video import VideoCreate

router = APIRouter(prefix="/videos", tags=["Videos"])

@router.post("/")
def create_video(video: VideoCreate):
    return {
        "message": "Video creado correctamente",
        "data": video
    }


📌 FastAPI:

Valida automáticamente el JSON recibido.

Genera documentación en Swagger.

Retorna errores claros si el JSON es inválido.

5️⃣ Registro del Router en la Aplicación

📄 app/main.py

from fastapi import FastAPI
from app.api.routes import videos

app = FastAPI(title="API de Integración con Vimeo")

app.include_router(videos.router)

6️⃣ Revisión de Swagger

Acceder a:

http://localhost:8000/docs


Se valida que:

El endpoint POST /videos.

Muestre la estructura esperada.

Aplique validaciones automáticamente.

7️⃣ Arquitectura del Proyecto (Concepto Clave)
📁 api/routes

Define los endpoints.

Maneja HTTP (GET, POST, etc.).

📁 schemas

Define la estructura de los datos.

Validación y documentación.

📁 services

Lógica de negocio.

Integraciones externas (Vimeo).

📁 core

Configuración general.

Logging.

Variables de entorno.

📌 Regla de oro:
Un endpoint NO debe contener lógica compleja.

8️⃣ Ejercicio Guiado (en clase)

Agregar un nuevo campo opcional al schema VideoCreate.

Probar validación incorrecta desde Swagger.

Observar el error automático generado por FastAPI.

✅ Resultado de la Clase 2

Al finalizar la sesión, el alumno es capaz de:

Usar Pydantic para validar datos.

Comprender el flujo request → schema → endpoint.

Identificar responsabilidades por carpeta.

Trabajar sobre una estructura profesional.

Leer y entender Swagger con modelos.
