<il><h1><a href="./content/chapter-4/chapter-4.md">Capítulo IV: Solution Software Design</a></h1></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.1. Strategic-Level Domain-Driven Design</a></h2></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1. EventStorming</a></h3></il>

Mediante la tecnica del event storming definimos los siguientes bounded context los cuales son principales dentro del proyecto:
El diagrama completo se encuentra en el siguiente enlace:
[Enlace](https://miro.com/welcomeonboard/RENPaXdVZVRsdU1xOTNOYXFVcmY4ZzBpKzFwb2Y4cUN1TmdLZkQvQ0pudVZsNWZKaG5DL1poeU0wV2ptem55SWtSVStLOXpBZ3J3cVN1MUswRjIzQW9XTkpIa2ROOTk0TEVTM21kR29MOWdSVnBaUFd1SFpWdEpJOHZ3Z3ZGc2h3VHhHVHd5UWtSM1BidUtUYmxycDRnPT0hdjE=?share_link_id=994329467841)

### Account Managed
![Image](https://github.com/user-attachments/assets/e8c31e5f-ddf1-4f51-8720-32d5cc9e9bb4)

### Treatment Managed
![Image](https://github.com/user-attachments/assets/5417e257-4acc-466d-b7d8-509a1f600e26)

### Comunication Managed
![Image](https://github.com/user-attachments/assets/67954401-a663-456e-8722-e1dc9c94fec4)

### Calendar Managed
![Image](https://github.com/user-attachments/assets/44e2a840-14dd-4aeb-8d7d-dda4fc9c9da8)

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.1. Candidate Context Discovery</a></h3></il>
![Image](https://github.com/user-attachments/assets/da3b2c4d-c1e2-4145-b18d-00eb8eabea3c)
![Image](https://github.com/user-attachments/assets/3b42a571-4390-4384-8248-5f6669ed6baa)
![Image](https://github.com/user-attachments/assets/2345dc02-02de-470a-ac7e-c9bf62284858)
![Image](https://github.com/user-attachments/assets/61c191c6-c639-4453-97fe-4839723c4f1b)
![Image](https://github.com/user-attachments/assets/b5e97564-f933-4e30-8d8d-f5f1601215e9)
![Image](https://github.com/user-attachments/assets/3df6939c-074c-4d7a-a1b3-59d2e10491ca)
![Image](https://github.com/user-attachments/assets/7db7c4c1-3db6-44a2-82c7-7b5431bcc452)
![Image](https://github.com/user-attachments/assets/9d7ffc30-46f7-4b4b-a758-49bd589379dd)
![Image](https://github.com/user-attachments/assets/8728d14a-62d4-41df-b90c-56659314a272)
![Image](https://github.com/user-attachments/assets/9b205f02-f2c5-43eb-a142-6ae2f5966fbb)


<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.2. Domain Message Flows Modeling</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.3. Bounded Context Canvases</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.2. Context Mapping</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3. Software Architecture</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.1. Software Architecture Context Level Diagrams</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.2. Software Architecture Container Level Diagrams</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.3. Software Architecture Deployment Diagrams</a></h3></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.2. Tactical-Level Domain-Driven Design</a></h2></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.2.1. Bounded Context: Chat</a></h2></il>

Este Bounded Context (BC) encapsula la funcionalidad de mensajería directa entre médicos y pacientes dentro de la aplicación oncológica. Su responsabilidad principal es gestionar las conversaciones, los mensajes, los participantes y las notificaciones relacionadas, asegurando una comunicación fluida y registrada como soporte al seguimiento del tratamiento y la coordinación de cuidados.


<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.1. Domain Layer</a></h3></il>

Esta capa contiene el núcleo del modelo de negocio y las reglas específicas del dominio de Chat. Se compone de las siguientes clases y abstracciones:

### Aggregates (Agregados) / Aggregate Roots

* **`Conversation`** (Actúa como Aggregate Root)
    * **Propósito:** Representa una única conversación entre un médico y un paciente. Es el punto de entrada principal para operaciones dentro de una conversación y asegura la consistencia.

### Entities (Entidades)

* **`Conversation`**
    * **Propósito:** Representa una única conversación entre un médico y un paciente. Actúa como Aggregate Root.
    * **Atributos:**
        * `id` (UUID): Identificador único de la conversación. (PK)
        * `doctorId` (UUID): Identificador del médico participante.
        * `patientId` (UUID): Identificador del paciente participante.
        * `createdAt` (DateTime): Fecha y hora de creación.
        * `lastMessageAt` (DateTime): Fecha y hora del último mensaje enviado.
        * `isActive` (Boolean): Indica si la conversación está activa o archivada.
        * `patientUnreadCount` (Integer): Contador de mensajes no leídos por el paciente.
        * `doctorUnreadCount` (Integer): Contador de mensajes no leídos por el médico.
    * **Métodos:**
        * `addMessage(message: Message)`: Añade un mensaje, actualiza `lastMessageAt` y contadores.
        * `markAsReadBy(userId: UUID)`: Reinicia el contador de no leídos y actualiza mensajes.
        * `archive()`: Marca la conversación como inactiva.
        * `reactivate()`: Marca la conversación como activa.
        * `canParticipate(userId: UUID)`: Verifica si un usuario es parte de esta conversación.

* **`Message`**
    * **Propósito:** Representa un único mensaje dentro de una `Conversation`.
    * **Atributos:**
        * `id` (UUID): Identificador único del mensaje. (PK)
        * `conversationId` (UUID): ID de la `Conversation` a la que pertenece. (FK)
        * `senderId` (UUID): ID del usuario (médico o paciente) que envió el mensaje.
        * `content` (String): Contenido textual del mensaje.
        * `sentAt` (DateTime): Fecha y hora de envío.
        * `messageType` (MessageType): Tipo de mensaje (TEXT, IMAGE, DOCUMENT, etc.).
        * `attachment` (Attachment?): Referencia opcional a un archivo adjunto.
        * `readByPatient` (Boolean): Indica si el paciente ha leído el mensaje.
        * `readByDoctor` (Boolean): Indica si el médico ha leído el mensaje.
    * **Métodos:**
        * `markAsReadBy(userId: UUID)`: Marca el mensaje como leído por el participante específico.
        * `attachFile(attachment: Attachment)`: Asocia un archivo adjunto al mensaje.

* **`Attachment`**
    * **Propósito:** Representa un archivo adjunto a un `Message`.
    * **Atributos:**
        * `id` (UUID): Identificador único del adjunto. (PK)
        * `messageId` (UUID): ID del `Message` al que está asociado. (FK)
        * `fileName` (String): Nombre original del archivo.
        * `fileType` (String): Tipo MIME del archivo (e.g., 'image/jpeg', 'application/pdf').
        * `fileSize` (Long): Tamaño del archivo en bytes.
        * `storageUrl` (String): URL o identificador para acceder al archivo en el sistema de almacenamiento.
    * **Métodos:**
        * `isImage()`: Devuelve true si el `fileType` corresponde a una imagen.
        * `isDocument()`: Devuelve true si el `fileType` corresponde a un documento común.

### Value Objects (Objetos de Valor)

* **`MessageType`** (Enumeration)
    * **Propósito:** Define los tipos posibles de mensajes para categorización y procesamiento diferencial.
    * **Valores:** `TEXT`, `IMAGE`, `DOCUMENT`, `SYSTEM_INFO`, `TREATMENT_RELATED`, `APPOINTMENT_RELATED`, `URGENT`.

### Domain Services (Servicios de Dominio)

* **`ChatNotificationService`**
    * **Propósito:** Orquesta la lógica de cuándo y cómo enviar notificaciones basadas en eventos del dominio, respetando reglas de negocio. Depende de interfaces de infraestructura para el envío real.
* **`ConversationPolicy`**
    * **Propósito:** Centraliza reglas de negocio complejas (ej. determinar urgencia, permitir inicio de conversación).

### Repositories (Interfaces de Repositorios)

* **`IConversationRepository`**
    * **Propósito:** Define el contrato para la persistencia de entidades `Conversation`.
    * **Métodos:** `save(conversation)`, `findById(id)`, `findByParticipantId(userId)`, `findActiveByParticipantId(userId)`.
* **`IMessageRepository`**
    * **Propósito:** Define el contrato para la persistencia de entidades `Message`.
    * **Métodos:** `save(message)`, `findById(id)`, `findByConversationId(conversationId, page, limit)`, `markMessagesAsRead(messageIds, userId)`.
* **`IAttachmentRepository`**
    * **Propósito:** Define el contrato para la persistencia de entidades `Attachment`.
    * **Métodos:** `save(attachment)`, `findById(id)`, `findByMessageId(messageId)`.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.2. Interface Layer</a></h3></il>


Esta capa expone la funcionalidad del Bounded Context al exterior, ya sea a través de APIs o consumiendo eventos de otros contextos.

### Controllers (Controladores - para API REST)

* **`ChatController`**
    * **Propósito:** Maneja las solicitudes HTTP entrantes relacionadas con conversaciones y mensajes.
    * **Métodos (Endpoints):**
        * `GET /conversations`: Obtiene la lista de conversaciones para el usuario autenticado.
        * `GET /conversations/{conversationId}/messages`: Obtiene los mensajes de una conversación específica (paginado).
        * `POST /conversations/{conversationId}/messages`: Envía un nuevo mensaje.
        * `POST /conversations/{conversationId}/messages/read`: Marca mensajes como leídos.
        * `POST /conversations`: (Opcional) Inicia una nueva conversación.
        * `POST /conversations/{conversationId}/archive`: Archiva una conversación.
* **`AttachmentController`**
    * **Propósito:** Maneja las solicitudes HTTP para la carga y descarga de archivos adjuntos.
    * **Métodos (Endpoints):**
        * `POST /messages/{messageId}/attachments`: Sube un archivo adjunto.
        * `GET /attachments/{attachmentId}`: Descarga un archivo adjunto.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.3. Application Layer</a></h3></il>

Esta capa orquesta los casos de uso y flujos de trabajo, conectando la Interface Layer con el Domain Layer.

### Command Handlers (Manejadores de Comandos)

* **`SendMessageCommandHandler`**
    * **Propósito:** Procesa el comando para enviar un mensaje.
    * **Lógica:** Valida, crea `Message`, actualiza `Conversation`, guarda, publica `MessageSentEvent`.
* **`MarkMessagesAsReadCommandHandler`**
    * **Propósito:** Procesa el comando para marcar mensajes como leídos.
    * **Lógica:** Actualiza `Message` y `Conversation`, guarda, publica `MessagesReadEvent`.
* **`UploadAttachmentCommandHandler`**
    * **Propósito:** Procesa el comando para adjuntar un archivo.
    * **Lógica:** Guarda archivo (vía Infra), crea/actualiza `Attachment`, guarda.
* **`ArchiveConversationCommandHandler`**
    * **Propósito:** Procesa el comando para archivar una conversación.
    * **Lógica:** Llama a `conversation.archive()`, guarda, publica `ConversationArchivedEvent`.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.4. Infrastructure Layer</a></h3></il>

Esta capa contiene las implementaciones concretas para interactuar con tecnologías externas (bases de datos, servicios de almacenamiento, colas de mensajes, etc.).

### Repository Implementations (Implementaciones de Repositorios)

* **`SqlConversationRepository`**: Implementa `IConversationRepository`.
* **`SqlMessageRepository`**: Implementa `IMessageRepository`.
* **`SqlAttachmentRepository`**: Implementa `IAttachmentRepository`.

### External Service Implementations (Implementaciones de Servicios Externos)

* **`DatabaseClient`**: Implementacion del cliente de BD.
* **`FirebasePushNotificationSender` / `EmailNotificationSender`**: Implementa `INotificationSender`.
* **`S3FileStorageService` / `LocalStorageFileStorageService`**: Implementa `IFileStorageService`.
* **`KafkaEventConsumer` / `RabbitMqEventConsumer`**: Implementa lógica de suscripción y despacho de eventos externos.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.5. Bounded Context Software Architecture Component Level Diagrams</a></h3></il> 

Este diagrama ilustra la descomposición del Container del Chat en sus componentes principales y sus interacciones.

![Component Level Diagrams](https://github.com/user-attachments/assets/3f0b6f9b-8b3b-4733-92d4-1178d683199e)

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.6. Bounded Context Software Architecture Code Level Diagrams</a></h3></il> 

Esta sección presenta diagramas que ofrecen un mayor nivel de detalle sobre la implementación de los componentes del Bounded Context de Chat.

<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.6.1. Bounded Context Domain Layer Class Diagrams</a></h3></il>

Este diagrama de clases del dominio proporciona una vista detallada de los elementos clave del modelo de negocio del Chat. Se representan las entidades con sus atributos y comportamientos, el objeto de valor `MessageType`, y las interfaces de los repositorios.

![ClassDiagram_Chat](https://github.com/user-attachments/assets/571f6a04-45ae-4003-b36c-6fb4ab2c1db5)

<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.6.2. Bounded Context Database Design Diagram</a></h3></il>

Este diagrama de diseño de la base de datos detalla el esquema de persistencia para el Bounded Context de Chat. Se especifican las tablas requeridas para almacenar las conversaciones, los mensajes y los archivos adjuntos, así como sus columnas, tipos de datos, restricciones y las relaciones entre ellas.

![BasedeDatos_Chat](https://github.com/user-attachments/assets/57870fa2-19ec-4bba-9042-682d30ee31fb)


<il><h2><a href="./content/chapter-4/chapter-4.md">4.2.2. Bounded Context: Usuario</a></h2></il>

Este Bounded Context (BC) encapsula la funcionalidad relacionada con la gestión de usuarios dentro de la aplicación OnContigo. Su responsabilidad principal es representar a los actores principales del sistema (médicos y pacientes), registrar sus datos personales y especializaciones, manejar su autenticación, y permitir funcionalidades clave como el registro de pacientes o la asignación de tratamientos por parte de los médicos. Este contexto también permite a los pacientes acceder y revisar su información médica.

<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.1. Domain Layer</a></h3></il>


### Aggregates / Aggregate Roots

* **Usuario** (Aggregate Root)
    * **Propósito:** Representa un usuario del sistema (médico o paciente). Contiene información común y opera como entrada principal de operaciones.

### Entities

* **Usuario**
    * **Atributos:**
        * `nombre` (String) - Nombre del usuario.
        * `apellido` (String) - Apellido del usuario.
        * `contrasenha` (String) - Contraseña encriptada del usuario.
        * `numeroTelefono` (String) - Número de teléfono.
        * `email` (String) - Correo electrónico del usuario.
    * **Métodos:**
        * `registrarCita(cita, nombre, apellido)`

* **Paciente** (hereda de Usuario)
    * **Métodos:**
        * `revisarHistorial(historialMedico)`
        * `agregarMedicamento(nombreMedicamento)`

* **Medico** (hereda de Usuario)
    * **Atributos:**
        * `especializacion` (String)
    * **Métodos:**
        * `revisarHistorialPaciente(nombre, apellido)`
        * `registrarPaciente(nombre, apellido)`
        * `asignarMedicamentoPaciente(...)`
        * `asignarTratamientoPaciente(...)`
        * `asignarProcedimientoPaciente(...)`

### Domain Services

* **UsuarioPolicy**
    * **Propósito:** Encapsular reglas de negocio como validación de identidad de usuario, rol o permisos de acceso.

### Repositories

* **IUsuarioRepository**
    * `findById(id)`
    * `add(usuario)`
    * `update(usuario)`
    * `remove(id)`

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.2. Interface Layer</a></h3></il>

### Controllers

* **UsuarioController**
    * **Propósito:** Exponer la lógica relacionada al registro y administración de usuarios.
    * **Endpoints:**
        * `GET /usuarios`: Obtener lista de usuarios.
        * `POST /usuarios`: Registrar nuevo usuario.
        * `PUT /usuarios/{id}`: Actualizar datos de un usuario.
        * `DELETE /usuarios/{id}`: Eliminar un usuario.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.1.3. Application Layer</a></h3></il>

### Command Handlers

* **RegisterUsuarioCommandHandler**
    * Procesa el registro de un usuario nuevo.

* **LoginUsuarioCommandHandler**
    * Procesa el inicio de sesión del usuario.

* **LogoutUsuarioCommandHandler**
    * Procesa el cierre de sesión del usuario.

### Event Handlers

* **UsuarioRegistradoEventHandler**
    * Maneja el evento luego del registro de usuario.

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.4. Infrastructure Layer</a></h3></il>

### Repository Implementations

* **UsuarioRepository**: Implementación concreta de `IUsuarioRepository`.
    * `ListByIdAsync()`
    * `AddAsync()`
    * `Update()`
    * `Remove()`

### External Infrastructure

* **AppDbContext**
    * `DbSet<Usuario>`: Tabla de usuarios.



<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.5. Bounded Context Software Architecture Component Level Diagrams</a></h3></il> 

![ComponentLevelDiagrams_usuario](https://github.com/user-attachments/assets/bbc7d312-aa98-43d9-a7cf-5a51f72e617a)

<br>
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.6. Bounded Context Software Architecture Code Level Diagrams</a></h3></il> 

Esta sección presenta diagramas que ofrecen un mayor nivel de detalle sobre la implementación de los componentes del Bounded Context de Usuario.

<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.6.1. Bounded Context Domain Layer Class Diagrams</a></h3></il>
![ClassDiagram_Usuario](https://github.com/user-attachments/assets/00a20a71-d7a5-4b45-97b2-83e9d05d69f9)

<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.2.6.2. Bounded Context Database Design Diagram</a></h3></il>

![BasedeDatos_Usuario](https://github.com/user-attachments/assets/70f2f5ec-2309-4da6-91ba-8131fe0853ce)