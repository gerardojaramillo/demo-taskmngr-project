




# Demo TaskMngr Project

<span style="color:green">Demo TaskMngr Project</span> (`demo-taskmngr-project`) el proyecto contiene el archivo `docker-compose.yml que hace referencia a la aplicación web (`demo-taskmngr-app`) para uso demostrativo meramente, está construida con **Java Ver. 17** como lenguage principal y **Spring Boot Ver. 3.5.0** cómo framework, se comunica a una base de datos relacional **MySQL Ver. 8.0.24** (`demo-taskmngr-db`) 




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
