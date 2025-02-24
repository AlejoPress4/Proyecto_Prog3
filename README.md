# Proyecto_Prog3

## Entidades

### Entidad: Departamento (Ente departamental)
- **Descripción** : Representa el ente gubernamental encargado de la gestión y asignación de recursos en los municipios.
- **Atributos** : 
  - `id` : Identificador único del departamento.
  - `nombre` : Nombre del departamento.
  - `ubicacion` : Ubicación geográfica del departamento.

---

### Entidad: Usuario
- **Descripción** : Representa a las personas que interactúan con el sistema, como administradores, operarios y alcaldes.
- **Atributos** : 
  - `id` : Identificador único del usuario.
  - `nombre` : Nombre completo del usuario.
  - `email` : Correo electrónico para inicio de sesión.
  - `password` : Contraseña cifrada.
  - `estado` : Estado del usuario (activo/inactivo).
  - `rol_id` : Identificador del rol asignado.

---

### Entidad: Municipio
- **Descripción** : Representa una unidad territorial bajo la administración de un alcalde.
- **Atributos** : 
  - `id` : Identificador único del municipio.
  - `nombre` : Nombre del municipio.
  - `departamento_id` : Identificador del departamento al que pertenece.

---

### Entidad: Maquinaria
- **Descripción** : Representa los equipos utilizados para la ejecución de servicios.
- **Atributos** : 
  - `id` : Identificador único de la maquinaria.
  - `tipo` : Tipo de maquinaria (excavadora, cargadora, etc.).
  - `estado` : Estado de la maquinaria (disponible, en uso, en mantenimiento).
  - `ubicacion` : Ubicación actual de la maquinaria.
  - `especialidad_id` : Especialidades compatibles con la maquinaria.

---

### Entidad: Alcalde
- **Descripción** : Representa al líder político de un municipio.
- **Atributos** : 
  - `id` : Identificador único del alcalde.
  - `nombre` : Nombre completo del alcalde.
  - `municipio_id` : Municipio al que está asignado.
  - `periodo` : Período de gobierno.

---

### Entidad: Operario
- **Descripción** : Representa a los trabajadores que manejan la maquinaria.
- **Atributos** : 
  - `id` : Identificador único del operario.
  - `nombre` : Nombre completo del operario.
  - `nivel_experiencia` : Nivel de experiencia del operario.
  - `especialidad_id` : Especialidades que posee el operario.

---

### Entidad: Ejecución
- **Descripción** : Representa la ejecución de un servicio solicitado.
- **Atributos** : 
  - `id` : Identificador único de la ejecución.
  - `fecha_inicio` : Fecha de inicio de la ejecución.
  - `fecha_fin` : Fecha de finalización.
  - `estado` : Estado de la ejecución (en progreso, finalizado).
  - `servicio_id` : Identificador del servicio asociado.

---

### Entidad: Servicio (Proyectos)
- **Descripción** : Representa un servicio de obra pública solicitado por un municipio.
- **Atributos** : 
  - `id` : Identificador único del servicio.
  - `municipio_id` : Municipio que solicita el servicio.
  - `fecha_solicitud` : Fecha en la que se realiza la solicitud.
  - `estado` : Estado del servicio (pendiente, aprobado, en ejecución).
  - `maquinaria_id` : Maquinarias asignadas al servicio.

---

### Entidad: Mantenimiento
- **Descripción** : Representa las reparaciones y revisiones periódicas de la maquinaria.
- **Atributos** : 
  - `id` : Identificador único del mantenimiento.
  - `fecha` : Fecha del mantenimiento.
  - `estado` : Estado del mantenimiento (pendiente, en proceso, finalizado).
  - `responsable` : Nombre del responsable del mantenimiento.
  - `maquinaria_id` : Identificador de la maquinaria asociada.

---

### Entidad: Factura
- **Descripción** : Representa el documento generado por un servicio ejecutado.
- **Atributos** : 
  - `id` : Identificador único de la factura.
  - `fecha_emision` : Fecha de emisión de la factura.
  - `monto` : Monto total a pagar.
  - `estado` : Estado del pago (pendiente, pagado).
  - `servicio_id` : Servicio relacionado con la factura.

---

### Entidad: Pago
- **Descripción** : Representa el pago realizado por un servicio facturado.
- **Atributos** : 
  - `id` : Identificador único del pago.
  - `metodo_pago` : Método de pago utilizado (tarjeta, transferencia, etc.).
  - `fecha` : Fecha del pago.
  - `factura_id` : Factura asociada al pago.

---

### Entidad: Notificación
- **Descripción** : Representa los avisos enviados a los usuarios.
- **Atributos** : 
  - `id` : Identificador único de la notificación.
  - `mensaje` : Contenido de la notificación.
  - `fecha_envio` : Fecha en la que se envió la notificación.
  - `usuario_id` : Usuario destinatario de la notificación.

---

### Entidad: Novedad
- **Descripción** : Representa cualquier incidencia o reporte registrado durante un turno de trabajo.
- **Atributos** : 
  - `id` : Identificador único de la novedad.
  - `tipo` : Tipo de novedad (daño, retraso, incidente).
  - `descripcion` : Descripción de la novedad.
  - `evidencia` : Documentos o imágenes adjuntas.
  - `gravedad` : Nivel de gravedad de la novedad.
  - `turno_id` : Turno en el que se registró la novedad.

---

### Entidad: Chat
- **Descripción** : Representa un canal de comunicación entre usuarios del sistema.
- **Atributos** : 
  - `id` : Identificador único del chat.
  - `fecha_creacion` : Fecha de creación del chat.

---

### Entidad: Mensaje
- **Descripción** : Representa los mensajes intercambiados en un chat.
- **Atributos** : 
  - `id` : Identificador único del mensaje.
  - `contenido` : Contenido del mensaje.
  - `fecha_envio` : Fecha de envío del mensaje.
  - `chat_id` : Identificador del chat al que pertenece el mensaje.

---

### Entidad: Turno
- **Descripción** : Representa el horario de trabajo de un operario en la ejecución de un servicio.
- **Atributos** : 
  - `id` : Identificador único del turno.
  - `fecha` : Fecha del turno.
  - `hora_inicio` : Hora de inicio del turno.
  - `hora_fin` : Hora de finalización del turno.
  - `operario_id` : Identificador del operario asignado.
  - `ejecucion_id` : Identificador de la ejecución asociada.



### Entidad: Logística
- **Descripción** : Representa la gestión del transporte y distribución de maquinaria y operarios para la ejecución de servicios.
- **Atributos** : 
  - `id` : Identificador único de la logística.
  - `fecha` : Fecha de la operación logística.
  - `responsable` : Nombre del encargado de la logística.
  - `estado` : Estado de la operación (pendiente, en proceso, completada).
  - `maquinaria_id` : Identificador de la maquinaria transportada.
  - `operario_id` : Identificador del operario asignado al transporte.
  - `servicio_id` : Servicio al que pertenece la logística.


## Diagrama de Clases

![Diagrama de Clases](ruta/al/diagrama.png)