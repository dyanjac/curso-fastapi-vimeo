# 📘 Curso: Integración de APIs con Python, FastAPI y Vimeo  
## 🟢 Clase 1 – Introducción y Arranque del Proyecto

**Duración:** 2 horas  
**Modalidad:** Práctica guiada  
**Instructor:** ____________________  
**Fecha:** ____________________

---

## ✅ Resumen de lo realizado en la Clase 1

En esta primera sesión se configuró el entorno de trabajo, se revisaron conceptos fundamentales de arquitectura backend y APIs REST, y se levantó un primer servicio funcional con FastAPI, probado desde Postman.

---

## 1) Instalación y configuración de herramientas

Durante la clase se instaló y verificó el funcionamiento de:

- **Notepad++**
- **Python 3.13**
- **PyCharm**
- **Postman**
- **Node.js / JSON** *(se dejó instalado el entorno y se reforzó el uso de JSON como formato de intercambio de datos en APIs)*

> Nota: Se explicó el propósito de cada herramienta dentro del flujo de desarrollo (editar código, ejecutar Python, desarrollar en IDE, probar endpoints).

---

## 2) Conceptos: Monolito vs Microservicios

### 2.1 Monolito
- Una sola aplicación que contiene todas las funcionalidades.
- Generalmente se despliega como una única unidad.
- Ventaja: simplicidad inicial.
- Desventaja: puede volverse difícil de mantener/escalar conforme crece.

### 2.2 Microservicios
- Conjunto de servicios pequeños e independientes.
- Cada microservicio cumple una responsabilidad específica.
- Se comunican entre sí (o con clientes) mediante **APIs**.

### 2.3 ¿Cómo se implementa un microservicio?
- Exponiendo una **API REST** (por ejemplo, con FastAPI) para que otros sistemas consuman sus funciones.

---

## 3) Conceptos: API REST y métodos HTTP

Se introdujo el concepto de **API REST** como una forma estándar de exponer funcionalidades vía HTTP.

### Métodos HTTP explicados
- **GET**: obtener información
- **POST**: enviar/crear información
- **PUT**: actualizar información
- **DELETE**: eliminar información

---

## 4) Formatos de intercambio: XML vs JSON

### XML
- Formato basado en etiquetas.
- Más verboso.
- Históricamente usado en integraciones.

### JSON
- Formato ligero basado en pares clave/valor y listas.
- Fácil de leer y escribir.
- Estándar más común en APIs REST actuales.

Se revisaron:
- Diferencias principales
- Estructuras típicas de cada formato
- Ventajas de JSON para APIs modernas

---

## 5) Python: definición y ventajas

Se reforzó por qué Python es adecuado para el curso:

- Sintaxis simple y legible.
- Alto soporte de librerías.
- Ideal para backend y construcción de APIs.
- Productivo para prototipos y soluciones reales.

---

## 6) Proyecto de la clase: creación de `CLASE-1` y `main.py`

Se creó el proyecto:

- Carpeta: `CLASE-1`
- Archivo principal: `main.py`

---

## 7) Instalación de FastAPI

Se instaló FastAPI (junto con Uvicorn para ejecución del servidor):

```bash
pip install fastapi uvicorn

8) Codificación del método GET usando FastAPI

Se implementó un endpoint simple para verificar que el servicio esté arriba:

main.py
from fastapi import FastAPI

app = FastAPI(title="API DE INTEGRACION con Vimeo")

@app.get("/health")
def health_check():
    return {
        "status": "ok",
        "message": "API funcionando correctamente"
    }

9) Concepto: ¿Qué es un servidor web?

Se explicó que para que una API sea accesible desde el navegador o Postman:

Debe ejecutarse como un servicio en un servidor (local o remoto).

El servidor escucha en un host y un puerto.

El cliente (Postman/navegador) consume la API por URL.

10) Instalación y ejecución con Uvicorn
¿Qué es Uvicorn?

Servidor ASGI que levanta aplicaciones FastAPI.

Comando usado para levantar el servicio:
python -m uvicorn main:app --reload


main → archivo main.py

app → variable app = FastAPI(...)

--reload → reinicia automáticamente al guardar cambios

11) Revisión del despliegue del servicio

Se verificó que el servicio se encuentre ejecutándose y responda correctamente.

URLs utilizadas:

Endpoint:

http://localhost:8000/health


Documentación automática (Swagger):

http://localhost:8000/docs

12) Consumo del endpoint usando Postman

Se realizó una prueba del endpoint:

Método: GET

URL: http://localhost:8000/health

Respuesta esperada:

{
  "status": "ok",
  "message": "API funcionando correctamente"
}

✅ Resultado final de la clase

Al finalizar la sesión, los alumnos lograron:

Tener el entorno instalado y listo (Python, PyCharm, Postman).

Entender conceptos base de monolito y microservicios.

Entender métodos HTTP y formatos XML/JSON.

Crear un proyecto simple y levantar un servicio FastAPI.

Probar un endpoint real usando Postman.
