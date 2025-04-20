<il><h1><a href="./content/chapter-3/chapter-3.md">Capítulo III: Requirements Specification</a></h1></il>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.1. To-Be Scenario Mapping</a></h3></il>

**Segmento:Paciente**

<img src="https://github.com/user-attachments/assets/722f6143-5adc-4082-9710-0d25b0de0ee0"/>

**Segmento:Doctor Oncólogo**

<img src="https://github.com/user-attachments/assets/80fc1295-1436-41cd-ad5f-8fed75e4695e"/>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.2. User Stories</a></h3></il>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.2. User Stories</a></h3></il>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.2. User Stories</a></h3></il>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>Epic/StoryID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Criterios de aceptación</th>
      <th>Epic ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>EP01</td>
      <td>Gestión de cuenta de usuarios</td>
      <td>Como usuario general Quiero acceder con mi cuenta Para ingresar a la plataforma</td>
      <td>Acceso a la Cuenta: El usuario debe poder acceder a su cuenta utilizando sus credenciales de inicio de sesión.<br>Autenticación Exitosa: Tras ingresar las credenciales correctas, el sistema debe autenticar al usuario de manera exitosa y redirigirlo a la página principal o a la sección correspondiente.<br>Credenciales Válidas: Si el usuario ingresa credenciales inválidas, el sistema debe mostrar un mensaje de error claro indicando que las credenciales son incorrectas.<br>Validación de Campos: El sistema debe validar el formato correcto de la dirección de correo electrónico y verificar la existencia del usuario en la base de datos si se utiliza como método de inicio de sesión.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>EP02</td>
      <td>Gestión de perfil</td>
      <td>Como usuario general Quiero realizar cambios en mi perfil Para actualizar mis datos personales</td>
      <td>Edición de Datos: El usuario debe poder editar sus datos personales, como nombre, dirección de correo electrónico y contraseña.<br>Validación de Datos: El sistema debe validar los nuevos datos para asegurar que cumplen con los formatos y restricciones necesarios.<br>Confirmación de Cambios: El sistema debe proporcionar una confirmación visual o mensaje cuando los cambios en el perfil se hayan guardado correctamente.</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>EP03</td>
      <td>Herramientas organizativas</td>
      <td>Como usuario general Quiero acceder a las herramientas organizativas de OnContigo Para mantener un orden con los tratamientos y medicamentos.</td>
      <td>Acceso a Herramientas: El usuario debe tener acceso a herramientas que le permitan organizar sus tratamientos y medicamentos.<br>Interfaz Intuitiva: Las herramientas deben ser fáciles de usar y acceder, con una interfaz clara y comprensible.<br>Funcionalidad Completa: Las herramientas deben permitir al usuario añadir, editar y eliminar información de tratamientos y medicamentos de manera eficiente.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>EP04</td>
      <td>Contacto para usuarios mediante la Landing Page</td>
      <td>Como usuario general Quiero que la Landing Page me muestre una forma de contacto Para poder contactar con OnContigo</td>
      <td>Visibilidad del Contacto: La información de contacto debe ser claramente visible en la landing page.<br>Formulario de Contacto Funcional: Un formulario de contacto debe estar disponible y funcionar correctamente, enviando las consultas de los usuarios al equipo de soporte o administrativo.<br>Respuesta Automática: Tras enviar una consulta, el usuario debe recibir una respuesta automática confirmando la recepción de su mensaje.</td>
      <td>EP04</td>
    </tr>
    <tr>
      <td>EP05</td>
      <td>Contacto entre médico y paciente mediante la App</td>
      <td>Como usuario general Quiero formas de comunicarme con mi paciente o médico Para poder establecer una buena comunicación</td>
      <td>Acceso a Comunicación: Médicos y pacientes deben poder comunicarse entre sí mediante la plataforma.<br>Funciones de Mensajería: Deben existir funciones de mensajería directa, preferiblemente con soporte para adjuntos y registros médicos.<br>Notificaciones: Ambos, médicos y pacientes, deben recibir notificaciones de nuevos mensajes o respuestas.</td>
      <td>EP05</td>
    </tr>
    <tr>
      <td>EP07</td>
      <td>Acceso a información médica relevante para el paciente</td>
      <td>Como paciente Quiero acceder fácilmente a la información médica que se me ha proporcionado Para consultar mis consultas, medicamentos y tratamientos cuando lo necesite.</td>
      <td>Acceso a Información Médica Relevante: Los pacientes deben poder acceder a los detalles de sus consultas, medicamentos y tratamientos desde la aplicación, en cualquier momento.<br>Consulta de Medicamentos: Los pacientes deben visualizar los medicamentos que les han sido indicados, incluyendo nombre, dosis y frecuencia.<br>Revisión de Tratamientos: Los pacientes deben poder revisar los tratamientos que han recibido, con información clara sobre su propósito y duración.</td>
      <td>EP07</td>
    </tr>
    <tr>
      <td>EP08</td>
      <td>Visualización de la Landing Page</td>
      <td>Como paciente Quiero visualizar la landing page Para tener una primera impresión de la aplicación</td>
      <td>Diseño Atractivo: La landing page debe tener un diseño atractivo y profesional que ofrezca una buena primera impresión.<br>Información Clave Visible: La landing page debe contener información clave sobre la aplicación, incluyendo características y beneficios para los usuarios.<br>Facilidad de Navegación: Los usuarios deben poder navegar fácilmente por la landing page para encontrar la información que necesitan.</td>
      <td>EP08</td>
    </tr>
    <tr>
      <td>us01</td>
      <td>Registrar cuenta</td>
      <td>Como usuario general<br>Quiero registrar una cuenta <br>Para acceder a la aplicación OnContigo</td>
      <td>E01: Ingreso correcto de datos<br>Dado que el usuario se encuentra en el formulario <br>de registro<br>Cuando ingresa su nombre, apellidos, correo, <br>edad, número de celular y contraseña correctamente<br>Entonces se registra su nueva cuenta<br><br>E02: Ingreso incorrecto de datos<br>Dado que el usuario se encuentra en el formulario <br>de registro<br>Cuando ingresa su nombre, apellidos, correo, edad, <br>número de celular y contraseña incorrectamente<br>Entonces el sistema rechazará la solicitud de registro <br>y pedirá completar los datos correctamente.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us02</td>
      <td>Configurar pagos</td>
      <td>Como usuario general<br>Quiero configurar mis métodos de pago<br>Para poder acceder a servicios adicionales ofrecidos por OnContigo</td>
      <td>E01: Doctor no realiza pago y no puede agregar pacientes<br>E02: Doctor realiza pago y puede agregar pacientes y tiene acceso completo a la app<br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us03</td>
      <td>Iniciar sesion igual US02</td>
      <td>Como usuario general<br>Quiero iniciar sesión en mi cuenta<br>Para acceder a las funciones de la aplicación</td>
      <td>E01: Inicio de sesión satisfactorio<br>Dado que el usuario se encuentra en el inicio de sesión.<br>Cuando ingrese sus credenciales correctas.<br>Entonces inicia sesión en su cuenta.<br><br>E02: Inicio de sesión sin registrar<br>Dado que el usuario se encuentra en el inicio de sesión.<br>Cuando ingrese las credenciales incorrectas.<br>Entonces le aparece un mensaje indicando que la cuenta no existe.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us04</td>
      <td>Cierre de sesión</td>
      <td>Como usuario general<br>Quiero cerrar mi cuenta al terminar de usar el aplicativo<br>Para evitar que otras personas accedan a mi cuenta</td>
      <td>E01: Cerrar sesión<br>Dado que el usuario está dentro de la aplicación.<br>Y selecciona el menú de la barra de navegación.<br>Cuando presione la opción “Sign out”.<br>Y confirme la acción.<br>Entonces será dirigido a la landing page.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us05</td>
      <td>Recuperación de cuenta</td>
      <td>Como usuario general<br>Quiero tener la opción de recuperar mi cuenta<br>Para no perder mis datos ya registrados</td>
      <td>E01: Envío de mensaje a correo<br>Dado que el usuario no pueda acceder a su cuenta<br>Cuando elige la opción “Recuperar cuenta” y la <br>opción “Por email”<br>Entonces el sistema envía un mensaje con una <br>opción de recuperación al correo electrónico <br>asociado a la cuenta<br><br>E02: Envío de mensaje de texto<br>Dado que el usuario no pueda acceder a su cuenta<br>Cuando elige la opción “Recuperar cuenta” y la <br>opción “Por mensaje de texto”<br>Entonces el sistema envía un mensaje con una opción <br>de recuperación al número asociado a la cuenta</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us06</td>
      <td>Cambio de número telefónico</td>
      <td>Como usuario general<br>Quiero cambiar el número de teléfono asociado a mi cuenta<br>Para que puedan contactarse conmigo</td>
      <td>E01: Ingreso correcto de datos<br>Dado que el usuario se encuentra en su perfil <br>de usuario<br>Cuando presiona la opción de modificar número <br>telefónico e ingresa un número correcto<br>Entonces se cambió el número de usuario<br><br>E02: Ingreso incorrecto de datos<br>Dado que el usuario se encuentra en su perfil <br>de usuario<br>Cuando presiona la opción de modificar número <br>telefónico e ingresa caracteres no permitidos <br>o inexistente<br>Entonces sale un mensaje que advierta que se <br>ingresó un número incorrecto.</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>us08</td>
      <td>Cambio de contraseña</td>
      <td>Como usuario general<br>Quiero cambiar la contraseña asociada a mi cuenta<br>Para mantener la seguridad de mi cuenta</td>
      <td>E01: Cambio de contraseña exitoso<br>Dado que el usuario se encuentra en su perfil de <br>usuario<br>Cuando presiona la opción de modificar la contraseña<br>Y escribe una nueva contraseña y la confirma<br>Entonces la contraseña se actualiza con éxito<br><br>E02: Cambio de contraseña erróneo<br>Dado que el usuario se encuentra en su perfil de <br>usuario<br>Cuando presiona la opción de modificar la contraseña<br>Y escribe una nueva contraseña, pero no cumple con <br>los parámetros de seguridad<br>Entonces la contraseña no se actualiza</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>us09</td>
      <td>Actualizar foto de perfil</td>
      <td>Como usuario general<br>Quiero cambiar mi foto de perfil<br>Para mantener mi perfil actualizado</td>
      <td>E01: Subir nueva foto de perfil<br>Dado que el usuario ha iniciado sesión<br>Cuando selecciona una nueva imagen y la sube<br>Entonces la imagen se guarda como su nueva foto de perfil<br><br>E02: Intentar subir imagen no compatible<br>Dado que el usuario intenta cambiar su foto<br>Cuando selecciona un archivo en formato no admitido<br>Entonces el sistema muestra un mensaje de error<br>Y no permite cargar la imagen</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>us10</td>
      <td>Mandar solciitud cita</td>
      <td>Como doctor<br>Quiero registrar una fecha y hora de cita en calendario<br>Para coordinar la atención con mis pacientes</td>
      <td>E01: Registrar solicitud de cita correctamente<br>Dado que el doctor ha iniciado sesión<br>Cuando selecciona una fecha y hora válidas<br>Entonces la cita se guarda en el calendario<br>Y el paciente recibe una notificación<br><br>E02: No seleccionar fecha u hora<br>Dado que el doctor intenta crear una cita<br>Cuando no elige fecha u hora<br>Entonces el sistema muestra un mensaje de error<br>Y no permite enviar la solicitud<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us11</td>
      <td>Aceptar cita</td>
      <td>Como paciente<br>Acepto cita<br>Para confirmar mi disponibilidad y asistir al encuentro con el doctor</td>
      <td>E01: Confirmar cita pendiente<br>Dado que el paciente ha recibido una solicitud de cita<br>Cuando accede a la notificación y presiona “Aceptar”<br>Entonces la cita se confirma y se registra en su calendario<br><br>E02: Intentar aceptar cita ya expirada<br>Dado que la fecha de la cita ya ha pasado<br>Cuando el paciente intenta aceptarla<br>Entonces el sistema muestra un mensaje indicando que la cita expiró</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us12</td>
      <td>Cancelar cita</td>
      <td>Como paciente<br>Quiero cancelar una cita previamente confirmada<br>Para reorganizar mi disponibilidad o reagendar con el doctor</td>
      <td>E01: Cancelar cita confirmada<br>Dado que el paciente tiene una cita activa<br>Cuando presiona “Cancelar”<br>Entonces la cita se elimina del calendario<br>Y el doctor es notificado<br><br>E02: Intentar cancelar una cita que ya fue cancelada o finalizada<br>Dado que el paciente ya canceló o asistió a una cita<br>Cuando intenta cancelarla nuevamente<br>Entonces el sistema muestra un mensaje indicando que no se puede realizar la acción</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us13</td>
      <td>Reprogramar cita</td>
      <td>Como paciente<br>Quiero reprogramar una cita médica<br>Para ajustarla a mi disponibilidad y continuar con mi tratamiento sin interrupciones</td>
      <td>E01: Reprogramar una cita con disponibilidad<br>Dado que el paciente tiene una cita registrada<br>Cuando accede a la sección de citas y selecciona "Reprogramar"<br>Y elige una nueva fecha y hora disponibles<br>Entonces la nueva cita queda registrada en el sistema<br>Y el paciente recibe una notificación de confirmación<br><br>E02: Intentar reprogramar una cita sin disponibilidad<br>Dado que el paciente intenta reprogramar una cita<br>Cuando no hay horarios disponibles en la fecha seleccionada<br>Entonces se muestra un mensaje indicando que no hay disponibilidad<br>Y se le sugiere elegir otra fecha</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us14</td>
      <td>Mandar solicitud de tratamiento</td>
      <td>Como médico<br>Quiero enviar una solicitud de tratamiento a un paciente<br>Para iniciar o modificar su plan de atención médica de forma clara y registrada</td>
      <td>E01: Enviar solicitud de tratamiento a un paciente<br>Dado que el médico ha completado el diagnóstico de un paciente<br>Cuando llena el formulario de tratamiento y presiona "Enviar"<br>Entonces la solicitud de tratamiento se registra en el sistema<br>Y el paciente recibe una notificación con los detalles<br><br>E02: Error al enviar solicitud sin campos obligatorios<br>Dado que el médico intenta enviar una solicitud de tratamiento<br>Cuando deja campos obligatorios vacíos<br>Entonces el sistema muestra un mensaje de error<br>Y no permite el envío hasta completar los datos requeridos</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us15</td>
      <td>Aceptar solicitud de cambios en tratamiento</td>
      <td>Como paciente<br>Quiero aceptar o rechazar una solicitud de cambios en mi tratamiento<br>Para tener control y conocimiento sobre las decisiones médicas que me afectan</td>
      <td>E01: Paciente acepta un cambio propuesto<br>Dado que el paciente recibe una solicitud de cambio en su tratamiento<br>Cuando revisa los detalles y selecciona "Aceptar"<br>Entonces el cambio se registra en el sistema<br>Y el médico es notificado de la aceptación<br><br>E02: Paciente rechaza el cambio propuesto<br>Dado que el paciente revisa una solicitud de cambio<br>Cuando selecciona "Rechazar"<br>Entonces el cambio no se aplica<br>Y el médico es notificado del rechazo</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us16</td>
      <td>Personalizar fecha de inicio tratamiento</td>
      <td>Como paciente<br>Quiero definir la fecha de inicio de mi tratamiento<br>Para ajustarla a mi disponibilidad y plan personal de salud</td>
      <td>E01: Seleccionar una fecha válida<br>Dado que el paciente ha aceptado un tratamiento<br>Cuando accede al calendario y selecciona una fecha válida para el inicio<br>Entonces la fecha queda registrada<br>Y se generan los recordatorios correspondientes<br><br>E02: Seleccionar una fecha anterior a la actual<br>Dado que el paciente intenta configurar una fecha de inicio<br>Cuando elige una fecha anterior al día actual<br>Entonces el sistema muestra un mensaje de error<br>Y no permite guardar la configuración</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us17</td>
      <td>Marcar cumplimiento de tratamiento</td>
      <td>Como paciente<br>Quiero marcar el cumplimiento diario de mi tratamiento<br>Para llevar un seguimiento adecuado de mi progreso médico</td>
      <td>E01: Paciente sigue tratamiento correctamente<br>Dado que el paciente ha recibido indicaciones de tratamiento<br>Cuando accede al sistema y marca el cumplimiento diario<br>Entonces se registra correctamente su seguimiento<br>Y el sistema actualiza el historial de tratamiento<br><br>E02: Paciente olvida marcar cumplimiento, pero cumple tratamiento<br>Dado que el paciente ha seguido el tratamiento<br>Cuando accede días después y marca cumplimiento retroactivo<br>Entonces el sistema permite registrar la información con fecha pasada<br>Y actualiza su progreso acumulado correctamente<br><br>E03: Paciente no cumple con el tratamiento ni marca cumplimiento<br>Dado que el paciente no realiza el tratamiento indicado<br>Cuando no marca el cumplimiento<br>Entonces el sistema mantiene el registro vacío<br>Y notifica al paciente sobre la importancia de mantener el seguimiento activo</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us18</td>
      <td>Asignar especialista</td>
      <td>Como médico<br>Quiero tratar mi paciente con un médico especializado<br>Para mantener correctamente la salud del paciente</td>
      <td>E01: El médico asigna un especialista para un tema específico del paciente, lo que le permite a este tomar una cita con el especialista<br>E02: El médico no encuentra un especialista, pero asigna el nombre y una forma de contacto de forma que el paciente puede revisarla</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us19</td>
      <td>Enviar sintomas</td>
      <td>Como paciente<br>Quiero enviar síntomas registrados en un tratamiento<br>Para que el doctor tenga un registro del estado de salud durante el tratamiento y pueda hacer seguimiento clínico</td>
      <td>E01: Enviar síntoma con éxito<br>Dado que el paciente está siguiendo un tratamiento activo<br>Cuando accede a la opción de registrar síntomas<br>Y completa los campos requeridos<br>Entonces el síntoma se registra exitosamente<br>Y el doctor puede visualizarlo en su panel<br><br>E02: Intentar enviar síntoma sin seleccionar tratamiento<br>Dado que el paciente no ha asociado un tratamiento<br>Cuando intenta registrar un síntoma<br>Entonces el sistema muestra un mensaje indicando que debe seleccionar un tratamiento activo<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us20</td>
      <td>Revisar sintomas</td>
      <td>Como doctor<br>Quiero ver la lista de síntomas reportados por el paciente<br>Para evaluar la evolución del tratamiento y tomar decisiones médicas informadas</td>
      <td>E01: Visualizar lista de síntomas de un paciente con tratamiento activo<br>Dado que el doctor accede al perfil de un paciente<br>Cuando selecciona un tratamiento específico<br>Entonces se muestra la lista de síntomas registrados durante ese tratamiento<br><br>E02: No hay síntomas registrados<br>Dado que el paciente aún no ha reportado síntomas<br>Cuando el doctor revisa la sección de síntomas<br>Entonces el sistema muestra un mensaje indicando que no hay registros disponibles<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us21</td>
      <td>Consultar medicamento</td>
      <td>Como paciente<br>Quiero consultar la composición de medicamentos y posibles reacciones<br>Para identificar efectos adversos, comparar con síntomas graves y enviar información al doctor para su evaluación</td>
      <td>E01: Consultar detalles de un medicamento asignado<br>Dado que el paciente tiene medicamentos asignados<br>Cuando accede a la sección de medicamentos<br>Y selecciona uno<br>Entonces puede ver su composición, efectos secundarios y advertencias<br><br>E02: Reportar reacción adversa desde la vista del medicamento<br>Dado que el paciente consulta un medicamento<br>Cuando detecta una posible reacción<br>Y presiona “Reportar reacción”<br>Entonces el sistema envía el reporte al doctor correspondiente</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us22</td>
      <td>Recibir notificaciones de cambios en tratamiento</td>
      <td>Como paciente<br>Quiero recibir notificación sobre solicitudes de cambios en el tratamiento<br>Para estar informado y tomar decisiones sobre la continuidad o modificación del plan terapéutico</td>
      <td>E01: Recibir notificación de cambio propuesto<br>Dado que el médico ha enviado una solicitud de cambio en el tratamiento<br>Cuando el paciente inicia sesión o abre la app<br>Entonces recibe una notificación con los detalles del cambio<br><br>E02: Ver historial de cambios propuestos<br>Dado que el paciente ha recibido notificaciones anteriores<br>Cuando accede a su sección de notificaciones<br>Entonces puede revisar el historial de cambios en su tratamiento<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us23</td>
      <td>Recibir notificacion de culminacion de tratamiento</td>
      <td>Como doctor<br>Quiero recibir notificación de finalización de tratamiento de los pacientes<br>Para agendar una cita de cierre, evaluar el progreso del paciente y definir próximos pasos si son necesarios</td>
      <td>E01: Doctor recibe notificación al completarse un tratamiento<br>Dado que un tratamiento ha llegado a su fecha final<br>Cuando el paciente marca el tratamiento como completado<br>Entonces el sistema notifica al doctor asociado<br><br>E02: Agendar evaluación post-tratamiento<br>Dado que el doctor ha sido notificado de la culminación de un tratamiento<br>Cuando accede al perfil del paciente<br>Entonces puede programar una cita de seguimiento desde la misma vista</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us24</td>
      <td>Consulta a doctor</td>
      <td>Como paciente<br>Quiero realizar consultas generales al doctor a través del chat<br>Para resolver dudas sobre mi tratamiento o estado de salud</td>
      <td>E01: Paciente envía mensaje por el chat<br>Dado que el paciente está autenticado<br>Cuando accede al chat y redacta una consulta<br>Entonces el mensaje se envía al doctor<br>Y queda registrado en la conversación<br><br>E02: Doctor responde consulta en el chat<br>Dado que el doctor recibe una consulta por chat<br>Cuando responde al mensaje<br>Entonces el paciente visualiza la respuesta en tiempo real<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us25</td>
      <td>Adjuntar archivos</td>
      <td>Como usuario general<br>Quiero poder adjuntar archivos para enviarlos por chat<br>Para compartir imágenes, recetas o resultados médicos con el doctor</td>
      <td>E01: Adjuntar imagen y enviarla por chat<br>Dado que el usuario está en una conversación activa<br>Cuando selecciona un archivo e imagen válida<br>Entonces el archivo se adjunta y se envía al chat<br><br>E02: Intentar adjuntar archivo no permitido<br>Dado que el usuario quiere enviar un archivo<br>Cuando selecciona un formato no admitido<br>Entonces el sistema muestra un mensaje de error<br>Y no permite el envío<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us26</td>
      <td>Agregar paciente</td>
      <td>Como doctor<br>Quiero enviar una solicitud de atención a paciente usando su username<br>Para agregarlo a mi lista de pacientes y asignarle un tratamiento</td>
      <td>E01: Agregar paciente con username válido<br>Dado que el doctor accede a la función de agregar paciente<br>Cuando introduce un username válido<br>Entonces se envía una solicitud al paciente<br>Y este puede aceptarla o rechazarla<br><br>E02: Username no existe en la plataforma<br>Dado que el doctor intenta agregar un paciente<br>Cuando introduce un username inválido<br>Entonces el sistema muestra un mensaje de error<br>Y no permite enviar la solicitud<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us27</td>
      <td>Crear procedimiento</td>
      <td>Como doctor<br>Quiero agregar procedimientos que debe realizar el paciente<br>Para definir los pasos del tratamiento, asignar tareas específicas y hacer seguimiento de su cumplimiento</td>
      <td>E01: Crear procedimiento con datos completos<br>Dado que el doctor accede a la sección de creación de procedimiento<br>Cuando llena los campos requeridos y guarda<br>Entonces el procedimiento se asocia al tratamiento del paciente<br><br>E02: No se permiten guardar procedimientos incompletos<br>Dado que el doctor no llena todos los campos requeridos<br>Cuando intenta guardar el procedimiento<br>Entonces el sistema muestra un mensaje de advertencia<br>Y no guarda el registro</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us28</td>
      <td>Resumen de tratamiento</td>
      <td>Como paciente<br>Quiero ver un resumen del tratamiento que voy a seguir<br>Para tener una vista general antes de aceptarlo, incluyendo fechas, medicamentos, procedimientos y duración</td>
      <td>E01: Ver resumen antes de aceptar tratamiento<br>Dado que el paciente ha recibido una propuesta de tratamiento<br>Cuando accede a la vista de resumen<br>Entonces se muestran todos los detalles del tratamiento<br><br>E02: Aceptar tratamiento desde resumen<br>Dado que el paciente revisó el resumen<br>Cuando selecciona “Aceptar tratamiento”<br>Entonces el tratamiento se activa en su cuenta<br>Y se configuran los recordatorios<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us29</td>
      <td>Configurar procedimiento</td>
      <td>Como doctor<br>Quiero tener control sobre el tipo de procedimiento que se asignará<br>Para definir su duración, frecuencia y condiciones específicas según cada caso</td>
      <td>E01: Asignar procedimiento con frecuencia personalizada<br>Dado que el doctor crea un procedimiento<br>Cuando define duración y número de repeticiones<br>Entonces el procedimiento queda configurado correctamente<br>Y se registra en el tratamiento del paciente<br><br>E02: Configuración inválida de repetición<br>Dado que el doctor configura un procedimiento<br>Cuando asigna valores fuera del rango permitido<br>Entonces el sistema bloquea el guardado<br>Y muestra un mensaje de validación<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us30</td>
      <td>Modificar la fecha de inicio</td>
      <td>Como paciente<br>Quiero modificar la fecha de inicio del tratamiento<br>Para tener un margen de tiempo para conseguir los medicamentos o programar citas con especialistas</td>
      <td>E01: Cambiar fecha de inicio con éxito<br>Dado que el paciente tiene un tratamiento próximo a iniciar<br>Cuando selecciona una nueva fecha válida<br>Entonces la fecha se actualiza<br>Y se reprograman los recordatorios<br><br>E02: Seleccionar fecha inválida (anterior al día actual)<br>Dado que el paciente accede a la configuración del tratamiento<br>Cuando intenta seleccionar una fecha anterior al presente<br>Entonces el sistema muestra un mensaje de error<br>Y no guarda el cambio<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us31</td>
      <td>Configuracion de recordatorios</td>
      <td>Descripción:<br>Como usuario en general<br>Quiero personalizar las notificaciones, tonos, duración y repetición de los recordatorios<br>Para adaptarlos a mi rutina diaria y no olvidar mis actividades médicas</td>
      <td>E01: Cambiar configuración de tono y frecuencia<br>Dado que el usuario accede a la configuración de recordatorios<br>Cuando selecciona un nuevo tono y ajusta la frecuencia<br>Entonces los cambios se guardan correctamente<br>Y se aplican a sus tratamientos activos<br><br>E02: Configurar recordatorios sin seleccionar horario<br>Dado que el usuario deja los campos de hora vacíos<br>Cuando intenta guardar<br>Entonces el sistema muestra un mensaje indicando que debe seleccionar al menos un horario</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us32</td>
      <td>Aviso de cambios en el sistema</td>
      <td>Como usuario en general<br>Quiero ser notificado si se ha realizado algún cambio en el calendario<br>Para estar al tanto de citas reprogramadas, cancelaciones o ajustes en mi tratamiento</td>
      <td>E01: Recibir notificación por reprogramación de cita<br>Dado que una cita ha sido reprogramada por el doctor<br>Cuando se actualiza la información<br>Entonces el paciente recibe una notificación inmediata<br>Y puede revisar la nueva fecha<br><br>E02: Notificación de cambios en el tratamiento<br>Dado que el tratamiento ha sido ajustado<br>Cuando se modifica la duración o procedimiento<br>Entonces el paciente recibe una alerta<br>Y puede consultar los cambios en su perfil<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us33</td>
      <td>Eliminar paciente</td>
      <td>Como doctor<br>Quiero eliminar pacientes que ya cumplieron con su tratamiento<br>Para mantener organizada mi lista de pacientes activos</td>
      <td>E01: Eliminar paciente que finalizó tratamiento<br>Dado que el paciente ha completado su tratamiento<br>Cuando el doctor selecciona la opción “Eliminar paciente”<br>Entonces el paciente se elimina de su lista<br>Y el sistema confirma la acción<br><br>E02: Intentar eliminar paciente con tratamiento activo<br>Dado que el paciente aún tiene tratamiento en curso<br>Cuando el doctor intenta eliminarlo<br>Entonces el sistema muestra una advertencia<br>Y no permite completar la eliminación</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us34</td>
      <td>Contactar con OnControl</td>
      <td>Como usuario general<br>Quiero contactar con el equipo de soporte de OnContigo<br>Para resolver dudas, reportar errores o recibir ayuda técnica</td>
      <td>E01: Enviar mensaje al soporte correctamente<br>Dado que el usuario accede a la sección de contacto<br>Cuando llena el formulario y presiona “Enviar”<br>Entonces el mensaje se envía al equipo de soporte<br>Y el usuario recibe confirmación<br><br>E02: Formulario con campos vacíos<br>Dado que el usuario intenta contactar con soporte<br>Cuando deja campos obligatorios vacíos<br>Entonces el sistema muestra un mensaje de error<br>Y no permite enviar el mensaje</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us35</td>
      <td>Lista de pacientes</td>
      <td>Como doctor<br>Quiero ver la lista de mis pacientes<br>Para acceder rápidamente a sus tratamientos y consultar su progreso</td>
      <td>E01: Visualizar lista completa de pacientes asignados<br>Dado que el doctor ha iniciado sesión<br>Cuando accede a la sección “Mis pacientes”<br>Entonces se muestra una lista con sus datos y estado de tratamiento<br><br>E02: Lista vacía si aún no tiene pacientes<br>Dado que el doctor no tiene pacientes registrados<br>Cuando accede a la sección<br>Entonces el sistema muestra un mensaje indicando que no hay pacientes asignados<br>E02: Lista vacía si aún no tiene pacientes<br>Dado que el doctor no tiene pacientes registrados<br>Cuando accede a la sección<br>Entonces el sistema muestra un mensaje indicando que no hay pacientes asignados</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us36</td>
      <td>Revisar historial de tratamientos</td>
      <td>Como doctor<br>Quiero ver el historial completo de los tratamientos realizados por el paciente desde que empezó a usar la aplicación<br>Para tener una visión cronológica de su evolución médica</td>
      <td>E01: Consultar historial cronológico de tratamientos<br>Dado que el doctor selecciona un paciente<br>Cuando accede a su historial<br>Entonces se muestra una lista ordenada cronológicamente de todos los tratamientos realizados<br><br>E02: No hay historial disponible<br>Dado que el paciente no tiene tratamientos anteriores<br>Cuando el doctor intenta ver el historial<br>Entonces el sistema muestra un mensaje indicando que no hay registros disponibles<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us37</td>
      <td>Lista de procedimientos</td>
      <td>Como paciente<br>Quiero ver la lista de procedimientos a seguir el día de hoy y de forma detallada<br>Para asegurarme de cumplir con mi tratamiento correctamente</td>
      <td>E01: Visualizar procedimientos programados para hoy<br>Dado que el paciente tiene procedimientos asignados<br>Cuando accede a la sección de procedimientos<br>Entonces se muestran los pasos a seguir para la fecha actual<br><br>E02: Sin procedimientos asignados para hoy<br>Dado que el paciente no tiene procedimientos activos para el día<br>Cuando accede a la sección<br>Entonces el sistema muestra un mensaje informativo<br><br></td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>us38</td>
      <td>Visualizar landing</td>
      <td>Como usuario en general<br>Quiero dar un primer vistazo a la aplicación y conocer en qué consiste<br>Para entender su funcionalidad mediante una landing page clara y atractiva</td>
      <td>E01: Acceder a la landing correctamente<br>Dado que el usuario accede al sitio web<br>Cuando ingresa a la landing page<br>Entonces se muestra una descripción general clara y los beneficios de la app<br><br>E02: Landing sin contenido disponible<br>Dado que hay un error de carga<br>Cuando el usuario accede a la landing<br>Entonces el sistema muestra un mensaje indicando que la información no está disponible por el momento<br><br></td>
      <td>EP08</td>
    </tr>
    <tr>
      <td>us39</td>
      <td>Acceso a la app</td>
      <td>Como usuario<br>Quiero ser redirigido a la tienda donde puedo descargar la app<br>Para instalarla fácilmente y comenzar a usarla</td>
      <td>E01: Redirección exitosa a tienda de apps<br>Dado que el usuario presiona el botón de descarga<br>Cuando está en la landing page<br>Entonces el sistema lo redirige correctamente a la tienda correspondiente (App Store o Play Store)<br><br>E02: Error en enlace de redirección<br>Dado que el enlace de redirección está roto<br>Cuando el usuario intenta descargar<br>Entonces se muestra un mensaje de error<br>Y se ofrece alternativa de contacto con soporte</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>us40</td>
      <td>Recibir informacion</td>
      <td>Como usuario general<br>Quiero recibir información completa al correo electrónico<br>Para tener una copia detallada de mis registros o actividades realizadas en la app</td>
      <td>E01: Solicitar envío de información por correo<br>Dado que el usuario accede a la opción de exportar información<br>Cuando introduce su correo electrónico y confirma<br>Entonces el sistema envía un resumen completo de su actividad<br><br>E02: Correo no válido<br>Dado que el usuario introduce un correo con formato incorrecto<br>Cuando intenta confirmar<br>Entonces el sistema muestra un mensaje de error<br>Y no envía la información<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS01</td>
      <td>Crear Endpoint para el registro de usuario</td>
      <td>Como desarrollador de la aplicación<br>Quiero tener un endpoint de tipo POST<br>Para registrar usuarios nuevos en la aplicación</td>
      <td>E01: Creación de usuario nuevo<br>Dado que el usuario se encuentra en la pantalla de crear cuenta<br>Cuando ingrese sus datos de forma correcta Y seleccione el botón "registrarse"<br>Entonces su cuenta será creada correctamente</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS02</td>
      <td>Implementación de la autenticación de usuario</td>
      <td>Como desarrollador<br>Quiero utilizar autenticación en las cuentas de mis usuarios<br>Para garantizar la seguridad de ellos</td>
      <td>E01: Iniciar sesión con credenciales válidas<br>Dado que el usuario se encuentre en la pantalla de inicio de sesión<br>Cuando ingrese correctamente sus datos Y seleccione el botón "iniciar sesión"<br>Entonces podrá ingresar a la aplicación con su usuario<br><br>E02: Credenciales no válidas<br>Dado que el usuario se encuentre en la pantalla de inicio de sesión<br>Cuando ingrese incorrectamente sus datos Y seleccione el botón "iniciar sesión"<br>Entonces aparecerá un mensaje de que los datos son incorrectos</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS03</td>
      <td>Creación de methods para el registro de procedmientos</td>
      <td>Como desarrollador<br>Quiero implementar los métodos necesarios para registrar procedimientos médicos<br>Para que puedan ser almacenados, visualizados y gestionados por médicos y pacientes</td>
      <td>E01: Registrar procedimiento exitosamente<br>Dado que se recibe un objeto con los datos del procedimiento<br>Cuando se llama al método de registro<br>Entonces el procedimiento se guarda correctamente en la base de datos<br><br>E02: Error al registrar procedimiento sin campos requeridos<br>Dado que se recibe un objeto incompleto<br>Cuando se llama al método de registro<br>Entonces el sistema lanza una excepción o mensaje de error por validación fallida</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS04</td>
      <td>Creacion de methods para registro de recordatorios</td>
      <td>Como desarrollador<br>Quiero implementar métodos para registrar recordatorios personalizados<br>Para que los usuarios puedan recibir alertas sobre citas, tratamientos y procedimientos</td>
      <td>E01: Guardar recordatorio con fecha y hora válidas<br>Dado que se proporciona un recordatorio con fecha y hora futuras<br>Cuando se ejecuta el método<br>Entonces el recordatorio se guarda correctamente en el sistema<br><br>E02: No permitir guardar recordatorio con fecha pasada<br>Dado que se recibe un recordatorio con fecha anterior a la actual<br>Cuando se intenta registrar<br>Entonces el sistema muestra un mensaje de error y no guarda el recordatorio</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS05</td>
      <td>Creacion de methods para registro de citas</td>
      <td>Como desarrollador<br>Quiero desarrollar los métodos necesarios para registrar citas entre médicos y pacientes<br>Para agendar encuentros de forma segura y estructurada</td>
      <td>E01: Registrar cita correctamente<br>Dado que se recibe información válida de la cita (paciente, doctor, fecha y hora)<br>Cuando se invoca el método<br>Entonces la cita se almacena correctamente y queda activa en el calendario<br><br>E02: No registrar cita con datos faltantes<br>Dado que se omite alguno de los campos obligatorios<br>Cuando se llama al método<br>Entonces el sistema responde con error de validación<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS06</td>
      <td>Creacion de methods para registro de tratamientos</td>
      <td>Como desarrollador<br>Quiero implementar los métodos necesarios para guardar tratamientos médicos<br>Para que puedan ser consultados y gestionados por los usuarios según corresponda</td>
      <td>E01: Guardar tratamiento con datos válidos<br>Dado que el sistema recibe un tratamiento completo (medicación, duración, procedimientos)<br>Cuando se invoca el método<br>Entonces el tratamiento se registra correctamente en la base de datos<br><br>E02: Fallo al guardar tratamiento sin duración<br>Dado que el tratamiento recibido no incluye duración<br>Cuando se intenta guardar<br>Entonces el sistema devuelve un mensaje de error y no registra la entrada<br><br></td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>TS07</td>
      <td>Creacion de methods para registro de mensajes</td>
      <td>Como desarrollador<br>Quiero implementar los métodos necesarios para registrar mensajes enviados por chat<br>Para facilitar la comunicación entre doctores y pacientes dentro de la app</td>
      <td>E01: Registrar mensaje enviado por un usuario<br>Dado que un usuario envía un mensaje por el chat<br>Cuando el método de registro es llamado con datos correctos<br>Entonces el mensaje se almacena con timestamp y emisor<br><br>E02: Rechazar mensaje vacío o inválido<br>Dado que se intenta enviar un mensaje vacío o sin contenido<br>Cuando se invoca el método<br>Entonces el sistema rechaza la operación con un mensaje de error</td>
      <td>EP01</td>
    </tr>
  </tbody>
</table>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.3. Impact Mapping</a></h3></il>
  
En esta sección, se ha llevado a cabo la creación del impact mapping, partiendo de las metas comerciales establecidas para cada user persona. Se han identificado los impactos deseados, los entregables necesarios y se han relacionado con las historias de usuario correspondientes.

Segmento objetivo: Pacientes y familiares

Link de UXPressia: 
<img src="https://github.com/user-attachments/assets/a5693c02-41cf-43e6-9949-0bb374206a59" >

Segmento objetivo: Oncólogos

Link de UXPressia: 
<img src="https://github.com/user-attachments/assets/9f8d931c-e961-44a3-b477-06c71facff47" >
