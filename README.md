# 📘 Curso: Integración de APIs con Python, FastAPI y Vimeo

## 🧑‍🏫 Información General

**Instructor:** ____________________  
**Empresa / Marca:** ____________________  
**Correo:** ____________________  
**Duración total:** 31 horas  
**Horario:** 7:30 p. m. – 9:30 p. m.  
**Días:** Martes, Miércoles, Jueves y Viernes  
**Costo por hora:** S/ 35.00  
**Costo total:** S/ 1,085.00  

---

## 🎯 Objetivo General del Curso

Capacitar a los participantes en el **desarrollo de APIs REST profesionales** utilizando **Python y FastAPI**, mediante la construcción progresiva de un **proyecto real de integración con la API de Vimeo**, aplicando buenas prácticas de arquitectura backend.

---

## 🧠 Público Objetivo

- Programadores junior
- Estudiantes con conocimientos básicos de programación
- Personas que conocen:
  - Variables
  - Condicionales
  - Bucles
- No se requiere experiencia previa en APIs ni FastAPI

---

## 🧪 Metodología de Enseñanza

- Enfoque **100 % práctico**
- Codificación en vivo
- Proyecto incremental desde la Clase 1
- Uso de herramientas reales (Postman, FastAPI, Uvicorn)
- Resolución de dudas en tiempo real

---

## 🏗️ Proyecto del Curso

Durante el curso se desarrollará una **API REST funcional** que permitirá:

- Listar videos
- Buscar videos
- Reproducir videos
- Subir videos
- Manejar errores
- Documentar la API con Swagger

El proyecto se desarrollará progresivamente desde la Clase 1 hasta la Clase 4, y se consolidará en la **Semana 5**, dedicada exclusivamente al **Proyecto Final Integrador (8 horas)**.

---

# 📚 Contenido del Curso por Clases

---

## 🟢 Clase 1 – Introducción y Arranque del Proyecto (2 horas)

### Contenido desarrollado
- Instalación de herramientas:
  - Notepad++
  - Python 3.13
  - PyCharm
  - Postman
  - Node.js / JSON
- Conceptos:
  - Monolito vs Microservicios
  - Qué es un microservicio
  - API REST
  - Métodos HTTP (GET, POST, PUT, DELETE)
  - XML vs JSON
  - Ventajas del lenguaje Python
- Creación del proyecto `CLASE-1`
- Creación del archivo `main.py`
- Instalación de FastAPI
- Implementación del método GET (`/health`)
- Concepto de servidor web
- Instalación y uso de Uvicorn
- Consumo del endpoint usando Postman

### Resultado
Primer servicio FastAPI levantado y probado.

---

## 🟢 Clase 2 – Métodos POST y envío de datos (2 horas)

### Contenido
- Diferencia entre GET y POST
- Envío de datos en el body
- Uso de JSON en POST
- Pruebas con Postman
- Introducción a errores comunes de sintaxis

### Avance del proyecto
- Endpoint POST funcional
- Recepción de datos desde el cliente

---

## 🟢 Clase 3 – Validación de datos con Pydantic (2 horas)

### Contenido
- ¿Qué es Pydantic?
- Modelos de entrada (request)
- Modelos de salida (response)
- Validaciones automáticas
- Errores HTTP básicos

### Avance del proyecto
- Reemplazo de `dict` por modelos Pydantic
- API más robusta y validada

---

## 🟢 Clase 4 – Estructura profesional del proyecto (2 horas)

### Contenido
- Separación de responsabilidades
- Organización por carpetas
- Buenas prácticas en proyectos FastAPI
- Uso de variables de entorno (`.env`)

### Avance del proyecto
- Refactor del proyecto a estructura profesional

---

## 🟢 Clase 5 – Consumo de APIs externas (parte 1) (2 horas)

### Contenido
- Qué es una API externa
- Autenticación por token
- Headers HTTP
- Introducción a `httpx`

### Avance del proyecto
- Cliente HTTP base
- Consumo de API externa de prueba

---

## 🟢 Clase 6 – Consumo de APIs externas (parte 2) (2 horas)

### Contenido
- Requests asíncronos
- Manejo de errores externos
- Reintentos y validaciones

### Avance del proyecto
- Cliente HTTP reutilizable
- Preparación para integración con Vimeo

---

## 🟢 Clase 7 – Introducción a la API de Vimeo (2 horas)

### Contenido
- Qué es Vimeo Developer API
- Creación de App en Vimeo
- Tokens y scopes
- Revisión de documentación oficial

### Avance del proyecto
- Configuración del token de Vimeo
- Primer request real a Vimeo

---

## 🟢 Clase 8 – Listado de videos (2 horas)

### Contenido
- Endpoint para listar videos
- Paginación
- Normalización de datos

### Avance del proyecto
- Implementación de `GET /videos`

---

## 🟢 Clase 9 – Búsqueda de videos (2 horas)

### Contenido
- Búsqueda por texto
- Query parameters
- Manejo de resultados vacíos

### Avance del proyecto
- Implementación de `GET /videos/search`

---

## 🟢 Clase 10 – Reproducción de videos (2 horas)

### Contenido
- Links de reproducción
- Embed HTML
- Redirect HTTP (302)

### Avance del proyecto
- Endpoint `/videos/{id}/play`

---

## 🟢 Clase 11 – Subida de videos (parte 1) (2 horas)

### Contenido
- Subida de archivos
- `multipart/form-data`
- Flujo de subida de Vimeo

### Avance del proyecto
- Endpoint `/videos/upload` (base)

---

## 🟢 Clase 12 – Subida de videos (parte 2) (2 horas)

### Contenido
- Manejo de errores
- Validaciones
- Confirmación de subida

### Avance del proyecto
- Subida completa y validada de videos

---

## 🟢 Clase 13 – Manejo de errores y logging (2 horas)

### Contenido
- Errores HTTP
- Manejo centralizado de errores
- Logging básico

### Avance del proyecto
- API más estable y mantenible

---

# 🏁 Semana 5 – Proyecto Final Integrador (8 horas)

### Objetivo
Consolidar el proyecto como un **producto funcional y profesional**.

### Actividades
- Revisión completa del código
- Correcciones y mejoras
- Limpieza de arquitectura
- Documentación final (README y Swagger)
- Pruebas finales

### Entregable
- API REST funcional
- Código organizado
- Documentación lista
- Proyecto presentable

---

## ✅ Resultados del Curso

Al finalizar el curso, el participante será capaz de:

- Diseñar APIs REST con FastAPI
- Integrar servicios externos reales
- Manejar validaciones y errores
- Estructurar proyectos backend profesionales
- Documentar y probar APIs
- Desarrollar un proyecto real de inicio a fin

---

## 📌 Notas Finales

Este documento se actualizará conforme avance el curso.  
Cada clase podrá contar adicionalmente con su propio archivo `.md` si se requiere mayor detalle.

