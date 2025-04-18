<il><h1><a href="./content/chapter-4/chapter-4.md">Capítulo IV: Solution Software Design</a></h1></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.1. Strategic-Level Domain-Driven Design</a></h2></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1. EventStorming</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.1. Candidate Context Discovery</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.2. Domain Message Flows Modeling</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.1.3. Bounded Context Canvases</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.2. Context Mapping</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3. Software Architecture</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.1. Software Architecture Context Level Diagrams</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.2. Software Architecture Container Level Diagrams</a></h3></il>

<il><h3><a href="./content/chapter-4/chapter-4.md">4.1.3.3. Software Architecture Deployment Diagrams</a></h3></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.2. Tactical-Level Domain-Driven Design</a></h2></il>

<il><h2><a href="./content/chapter-4/chapter-4.md">4.2.X. Bounded Context: Chat</a></h2></il>

Este Bounded Context (BC) encapsula la funcionalidad de mensajería directa entre médicos y pacientes dentro de la aplicación oncológica. Su responsabilidad principal es gestionar las conversaciones, los mensajes, los participantes y las notificaciones relacionadas, asegurando una comunicación fluida y registrada como soporte al seguimiento del tratamiento y la coordinación de cuidados.


<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.X.1. Domain Layer</a></h3></il>

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
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.X.2. Interface Layer</a></h3></il>


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
<il><h3><a href="./content/chapter-4/chapter-4.md">4.2.X.3. Application Layer</a></h3></il>

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

