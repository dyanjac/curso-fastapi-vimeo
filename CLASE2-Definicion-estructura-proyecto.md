📁 vimeo/ (raíz del proyecto)

👉 Es el contenedor principal del proyecto.
Aquí vive todo el código, configuración y documentación.

📁 app/

👉 Es el corazón de la aplicación.
Todo lo que hace funcionar la API está aquí.

💡 Frase para clase:
“Si esto fuera una empresa, app/ sería la oficina principal.”

📁 app/main.py

👉 Punto de entrada de la API.

Se crea la instancia de FastAPI

Se levantan los routers

Es el archivo que ejecuta Uvicorn

python -m uvicorn app.main:app


💡 “Sin main.py, la API no arranca.”

📁 app/api/

👉 Capa de exposición de la API.
Aquí se define qué endpoints existen.

📁 app/api/routes/

👉 Contiene las rutas (endpoints) de la aplicación.

Cada archivo representa un grupo de endpoints

Ejemplo: videos.py, health.py

💡 “Aquí definimos las URLs que el cliente puede usar.”

📁 app/core/

👉 Configuración central y transversal del proyecto.

💡 “Cosas importantes que usa toda la app.”

📄 config.py

Variables de entorno

Tokens (Vimeo, etc.)

Configuración general

“Aquí vive la configuración, no la lógica.”

📄 logging.py

Configuración de logs

Formato de mensajes

Nivel de logs (INFO, ERROR, etc.)

“Sirve para saber qué está pasando dentro de la API.”

📁 app/schemas/

👉 Modelos de datos (Pydantic).

Define cómo se ven los datos

Valida entradas y salidas

📄 video.py

Estructura de un video

Request y Response models

💡 “Aquí decimos qué datos esperamos y qué datos devolvemos.”

📁 app/services/

👉 Lógica de negocio e integraciones externas.

No hay rutas aquí

No hay FastAPI aquí

Solo funciones que hacen trabajo

💡 “Los servicios hacen el trabajo pesado.”

Ejemplo:

Consumir la API de Vimeo

Llamadas HTTP

Procesamiento de datos

📁 docker/

👉 Archivos relacionados a Docker.

Dockerfile

Configuración de contenedores

💡 “Sirve para desplegar la app más adelante.”

📁 tests/

👉 Pruebas automáticas.

Tests de endpoints

Tests de servicios

💡 “Aquí verificamos que el código no se rompa.”

📁 venv/

👉 Entorno virtual de Python.

Librerías instaladas

Dependencias del proyecto

⚠️ Nunca se sube a GitHub

📄 .env

👉 Variables sensibles:

Tokens

Claves

Configuración por entorno

💡 “Nunca se versiona.”

📄 requirements.txt

👉 Lista de dependencias del proyecto.

fastapi
uvicorn
httpx


💡 “Esto le dice a Python qué instalar.”

📄 README.md

👉 Documentación del proyecto.

Qué hace la API

Cómo ejecutarla

Ejemplos de uso

💡 “Es el manual del proyecto.”

🧠 Resumen mental para el alumno
Carpeta	¿Para qué sirve?
api/	URLs y endpoints
schemas/	Forma de los datos
services/	Lógica e integraciones
core/	Configuración
main.py	Arranque de la app
