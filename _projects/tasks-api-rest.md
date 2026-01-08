---
layout: default
title: "Tasks API · Proyecto docente (API REST)"
date: 2025-01-08
nivel: "Intermedio"
promocion: "Project"
stack:
  - Java 17
  - Spring Boot 3
  - H2
  - Swagger
---

## ¿Qué es este proyecto?

> **Tasks API** es un proyecto que sirve como base para enseñar la **construcción de una API REST profesional** en Java, e incluyendo buenas prácticas habituales en backend en las siguientes versiones.

<div align="center" style="margin-top: 12px;">
  <img src="{{ '/assets/exec/images/tasks-api-rest.png' | relative_url }}"
       width="520" style="max-width:100%; height:auto;"
       alt="tecnologias api rest java">
</div>

Forma parte del conjunto de *Projects* publicados en  
👉 https://jpexposito.github.io/projects/

---

## Objetivos

> El foco del proyecto es **aprender haciendo**, de forma incremental.

- Diseñar una API REST clara y mantenible.
- Implementar un **CRUD completo** de recursos.
- Introducir **Spring Data JPA** y persistencia.
- Documentar la API con **Swagger / OpenAPI**.

<hr/>

## Funcionalidades principales

- Crear tareas
- Listar tareas
- Obtener tareas por identificador
- Actualizar tareas
- Eliminar tareas

<hr/>

## Modelo de dominio

Una **tarea** se define con los siguientes campos:

- `id` → Identificador único
- `title` → Título de la tarea
- `description` → Descripción
- `completed` → Estado de finalización

Este modelo permite explicar:
- Entidades JPA
- Repositorios
- Serialización JSON
- Operaciones CRUD

<hr/>

## Stack tecnológico

- **Java 17**
- **Spring Boot 3**
- Spring Web
- Spring Data JPA
- H2 Database
- Swagger / OpenAPI
- Maven

<hr/>

## Ejecución del proyecto

Clonar el repositorio:

```bash
git clone https://github.com/jpexposito/tasks-api.git
cd tasks-api
```

Construir y ejecutar:

```bash
mvn clean install
mvn spring-boot:run
```

La API quedará accesible en:

```
http://localhost:8080/api/tasks
```

<hr/>

## Documentación y pruebas (Swagger)

La documentación interactiva se genera automáticamente:

```
http://localhost:8080/swagger-ui.html
```

Swagger permite:
- Explorar endpoints
- Probar peticiones
- Ver esquemas de datos
- Introducir el **Bearer Token** cuando la API está securizada

<hr/>

## Endpoints principales

| Método | Endpoint |
|------|---------|-----|
| GET | /api/tasks | 
| GET | /api/tasks/{id} | 
| POST | /api/tasks | 
| PUT | /api/tasks/{id} | 
| DELETE | /api/tasks/{id} |

<hr/>

## Enfoque

Este proyecto está diseñado para:

- Introducir **arquitectura REST**
- Trabajar seguridad en APIs modernas
- Usar Swagger como herramienta real
- Evolucionar el proyecto paso a paso


<hr/>

<div class="cardx__cta">
  <a class="btnx btnx--ghost" href="https://github.com/jpexposito/tasks-api" target="_blank" rel="noopener">
    Repo · GitHub
  </a>
</div>

