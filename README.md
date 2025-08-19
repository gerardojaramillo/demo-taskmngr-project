# Demo TaskMngr Project

El **Demo TaskMngr Project** (`demo-taskmngr-project`) es un entorno demostrativo que distribuye un archivo `docker-compose.yml`. Este archivo orquesta la ejecución de los siguientes servicios:

**Aplicación Web** (`demo-taskmngr-app`) Está construida con **Java Ver. 17** como lenguage principal y **Spring Boot Ver. 3.5.0** cómo framework.

**Base de Datos** (`demo-taskmngr-db`) Una instancia de **MySQL Ver. 8.0.24** para persistencia de datos relacionales.

El proyecto tiene un propósito exclusivamente demostrativo, orientado a mostrar las operaciones CRUD (Crear, Leer, Actualizar y Eliminar) sobre entidades de ejemplo.

Este entorno puede utilizarse como referencia para:

- Aprender a estructurar una aplicación Java + Spring Boot con persistencia en MySQL.
- Probar despliegues rápidos con Docker Compose.
- Explorar buenas prácticas de arquitectura para microservicios básicos.

## Docker Installation

You can download Docker desktop in the docker site.

```bash
  https://www.docker.com
```
    
## Run Locally

Clone the project

```bash
  git clone https://github.com/gerardojaramillo/demo-taskmngr-project.git
```

Go to the project directory

```bash
  cd demo-taskmngr-project
```

Run the containers.

```bash
  docker compose up -d
```

Open a browser and write in the url bar.

```bash
  http://localhost:8080/
```
