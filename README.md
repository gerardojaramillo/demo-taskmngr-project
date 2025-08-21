# Task Manager Demo

Aplicación de gestión de tareas y proyectos orientada a equipos de trabajo.  
Permite organizar actividades, priorizarlas y dar seguimiento al avance de manera colaborativa.  

⚠️ **Nota:** Este proyecto tiene fines **demostrativos**. No busca ser un producto completo de producción, sino un ejemplo técnico de arquitectura moderna con **Spring Boot 3.5.0** y buenas prácticas en desarrollo backend.


## Características principales
- **Gestión de Tareas (CRUD)**: crear, visualizar, actualizar y eliminar.
- **Proyectos**: cada tarea pertenece a un proyecto específico.
- **Priorización**: niveles *High, Medium, Low*.
- **Asignación de responsables**: soporte multi-usuario.
- **Etiquetas (Tags)**: clasificación flexible de tareas.
- **Flujo de trabajo**: estados *Not Started, In Progress, Done*.
- **Interfaz visual**: tabla central con acciones rápidas.


## Beneficios
- Organización clara de tareas por proyecto.
- Priorización efectiva y asignación de responsables.
- Transparencia y seguimiento del progreso en equipo.
- Base para integrar metodologías ágiles (Scrum, Kanban).


## Características técnicas
- **Backend**
  - **Framework:** Spring Boot 3.5.0 con arquitectura RESTful.
  - **Persistencia:** Spring JDBC + MySQL con relaciones Many-to-Many (tareas ↔ asignados, tareas ↔ etiquetas).
  - **Consultas SQL avanzadas:** uso de `JSON_ARRAYAGG` y `JSON_OBJECT` para exponer datos jerárquicos (tarea con asignados y etiquetas).
  - **Identificadores eficientes:** manejo de `UUID` en formato binario para optimizar índices y referencias.
  - **Arquitectura limpia:** separación en capas Controller → Service → Repository.
  - **DTOs y proyecciones** para respuestas optimizadas.
  - **Manejo de errores:** centralizado con `@ControllerAdvice`.
  - **Documentación de API:** OpenAPI/Swagger.
  - **Testing:** JUnit + Testcontainers (base de datos aislada en Docker para pruebas).

- **Frontend**
  - **Tecnologías utilizadas:** 
    - **jQuery** para manipulación del DOM y consumo de la API REST.
    - **HTML5** para estructura semántica.
    - **CSS3** para estilos y diseño responsive.
    - **JavaScript** para interactividad y validaciones.
  - **Diseño enfocado en simplicidad:** UI limpia y minimalista para resaltar la lógica de negocio.
  - **Integración directa con REST API**: render dinámico de tareas, proyectos, asignados y etiquetas.


## Componentes
El **Demo TaskMngr Project** (`demo-taskmngr-project`) distribuye un archivo `docker-compose.yml` que orquesta los siguientes servicios:

- **Aplicación Web** (`demo-taskmngr-app`)  
  Construida con **Java 17** y **Spring Boot 3.5.0**.
  
- **Base de Datos** (`demo-taskmngr-db`)  
  Una instancia de **MySQL 8.0.24** para persistencia de datos relacionales.


## Propósito
El proyecto tiene un fin exclusivamente demostrativo, orientado a mostrar:

- Cómo estructurar una aplicación Java + Spring Boot con persistencia en MySQL.
- Cómo realizar despliegues rápidos con Docker Compose.
- Buenas prácticas de arquitectura en un microservicio básico.
- Cómo conectar un **frontend ligero con jQuery y CSS** hacia un **backend Spring Boot REST API**.
