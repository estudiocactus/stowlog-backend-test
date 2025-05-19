# Prueba Técnica Backend - Sistema de Gestión de Tareas
## Descripción
Esta prueba técnica está diseñada para evaluar tus habilidades en desarrollo backend. La tarea consiste en construir un sistema de gestión de tareas con notificaciones, utilizando patrones de diseño clave como **Repository**, **Factory**, y **Strategy**, si crees que es preciso implementar cualquier otro tipo de patrón, adelante. El sistema debe permitir a los usuarios crear, actualizar y eliminar tareas, y notificar a los usuarios sobre eventos importantes relacionados con las tareas.
### Duración estimada: 3-4 días
## Requisitos
### Funcionalidad
1. **Gestión de Tareas**
   - Los usuarios deben poder crear, actualizar y eliminar tareas (CRUD).
   - Cada tarea tendrá los siguientes campos:
     - `id`: Identificador único.
     - `title`: Título de la tarea.
     - `description`: Descripción de la tarea.
     - `createdAt`: Fecha de creación.
     - `updatedAt`: Fecha de última actualización.
     - `completed`: Booleano que indica si la tarea está completada.
Las tareas no deben ser eliminadas por completo, si no que se debe de utilizar una técnica de **soft delete**.
2. **Notificaciones**
   - El sistema debe enviar una notificación cuando:
     - Se cree una nueva tarea.
     - Se actualice el estado de una tarea (por ejemplo, marcarla como completada).
   - Las notificaciones pueden ser simuladas mediante logs en consola o como un correo electrónico simulado.
3. **Eventos**
   - Debes implementar un sistema de eventos que maneje los cambios en el estado de las tareas. Por ejemplo:
     - Cuando se cree una tarea, se emite un evento de creación de tarea.
     - Cuando se actualice una tarea, se emite un evento de actualización de tarea.
   - Los eventos deben estar desacoplados de la lógica principal de negocio.
4. **Patrón Strategy**
   - Implementa el **Patrón Strategy** para la gestión de las notificaciones. Dependiendo del tipo de evento, las notificaciones deben comportarse de manera diferente. Por ejemplo:
     - Para una nueva tarea, la notificación se enviará por correo electrónico.
     - Para una actualización de tarea, la notificación se enviará como un mensaje interno.
   - Crea una interfaz `NotificationStrategy` con implementaciones como `EmailNotificationStrategy` e `InternalMessageNotificationStrategy`.
### [Patrones de Diseño](https://refactoring.guru/design-patterns/typescript)
1. [**Repository Pattern**](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30):
   - Implementa un repositorio para las tareas que maneje la persistencia de datos.
   - Los métodos básicos del repositorio deben incluir `create`, `update`, `delete`, y `findById`.
2. [**Factory Pattern**](https://refactoring.guru/design-patterns/factory-method):
   - Crea una factoría que se encargue de la creación de tareas, centralizando la creación y facilitando futuras modificaciones o validaciones adicionales.
3. [**Strategy Pattern**](https://refactoring.guru/design-patterns/strategy):
   - Implementa este patrón para cambiar dinámicamente el comportamiento de las notificaciones según el tipo de evento (creación, actualización, etc.).
## Requisitos Técnicos
- **Tecnologías recomendadas**:
  - Node.js con Express.js o NestJS (elige la que prefieras).
  - Si decides utilizar una base de datos, puedes usar Mongoose para MongoDB o TypeORM para bases de datos SQL.
  - Las notificaciones pueden ser simuladas con logs en consola o utilizando una librería para enviar correos electrónicos (como `nodemailer`).
  - Utiliza **Jest** o cualquier otra herramienta de pruebas para asegurarte de que tu código funciona correctamente.
## Evaluación
- **Calidad del Código**: La claridad, organización y calidad de la implementación, así como el uso de los patrones de diseño.
- **Uso Correcto de los Patrones**: La correcta implementación de los patrones de diseño **Repository**, **Factory**, y **Strategy**.
- **Pruebas**: La cobertura de las pruebas unitarias y de integración, y la efectividad de las mismas.
- **Funcionalidad**: Verificación de que el sistema de eventos, las notificaciones y el patrón Strategy funcionan correctamente y de manera coherente.
## Entregables
- Código fuente del proyecto.
- Pruebas unitarias.
- Documentación básica sobre cómo ejecutar el proyecto y la estructura del código.
## Instrucciones para Enviar la Prueba
1. Subir el código a un repositorio en GitHub, GitLab o cualquier otra plataforma similar.
2. Incluir un archivo `README.md` con instrucciones claras para la ejecución del proyecto, cualquier configuración adicional y detalles relevantes.
3. Enviar el enlace del repositorio al correo electrónico indicado.
¡Buena suerte y esperamos ver tu solución!
