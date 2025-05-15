<il><h1><a href="./content/chapter-3/chapter-3.md">Capítulo III: Requirements Specification</a></h1></il>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.1. To-Be Scenario Mapping</a></h3></il>

**Segmento:Paciente**

<img src="https://github.com/user-attachments/assets/722f6143-5adc-4082-9710-0d25b0de0ee0"/>

**Segmento:Doctor Oncólogo**

<img src="https://github.com/user-attachments/assets/80fc1295-1436-41cd-ad5f-8fed75e4695e"/>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.2. User Stories</a></h3></il>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>StoryID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Criterios de aceptación</th>
      <th>Epic ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>US01</td>
      <td>Registrar cuenta</td>
      <td>Como usuario general<br>Quiero registrarme<br>Para acceder a la aplicación OnControl</td>
      <td><strong>E01 – Registro exitoso:</strong> Dado que el usuario está en el formulario de registro Cuando completa todos los campos obligatorios con datos válidos Entonces el sistema crea su cuenta y lo redirige al dashboard.<br><br><strong>E02 – Datos inválidos:</strong> Dado que el usuario está en el formulario de registro Cuando falta algún campo obligatorio o el formato es incorrecto Entonces el sistema muestra un mensaje de validación y no crea la cuenta.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>US02</td>
      <td>Configurar pagos</td>
      <td>Como usuario general<br>Quiero añadir métodos de pago<br>Para acceder a servicios adicionales</td>
      <td><strong>E01 – Añadir método válido:</strong> Dado que el usuario está en la sección de pagos Cuando ingresa los datos de tarjeta válidos Entonces el sistema registra el método y lo muestra en la lista.<br><br><strong>E02 – Método inválido:</strong> Dado que el usuario intenta añadir un método Cuando los datos son incorrectos o caducados Entonces el sistema muestra un error y no guarda el método.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>US03</td>
      <td>Iniciar sesión</td>
      <td>Como usuario general<br>Quiero iniciar sesión<br>Para acceder a las funciones de la app</td>
      <td><strong>E01 – Autenticación exitosa:</strong> Dado que el usuario está en la pantalla de login Cuando ingresa credenciales válidas Entonces el sistema lo autentica y muestra el dashboard.<br><br><strong>E02 – Credenciales inválidas:</strong> Dado que el usuario está en la pantalla de login Cuando ingresa credenciales incorrectas Entonces el sistema muestra un mensaje de error.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>US04</td>
      <td>Cerrar sesión</td>
      <td>Como usuario general<br>Quiero cerrar mi sesión<br>Para proteger mi cuenta tras usar la app</td>
      <td><strong>E01 – Cierre exitoso:</strong> Dado que el usuario está autenticado Cuando selecciona “Cerrar sesión” Entonces el sistema lo redirige a la landing page.<br><br><strong>E02 – Prevención de acceso:</strong> Dado que el usuario cierra sesión Cuando intenta navegar con la sesión cerrada Entonces el sistema lo obliga a loguearse de nuevo.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>US05</td>
      <td>Recuperación de cuenta</td>
      <td>Como usuario general<br>Quiero recuperar mi cuenta<br>Para no perder mis datos registrados</td>
      <td><strong>E01 – Recuperación por email:</strong> Dado que el usuario no recuerda su contraseña Cuando elige “Recuperar por email” Entonces el sistema envía un enlace de restablecimiento.<br><br><strong>E02 – Recuperación por SMS:</strong> Dado que el usuario no recuerda su contraseña Cuando elige “Recuperar por SMS” Entonces el sistema envía un código de verificación al móvil.</td>
      <td>EP01</td>
    </tr>
    <tr>
      <td>US06</td>
      <td>Cambio de número telefónico</td>
      <td>Como usuario general<br>Quiero actualizar mi número de teléfono<br>Para recibir notificaciones correctamente</td>
      <td><strong>E01 – Cambio exitoso:</strong> Dado que el usuario está en su perfil Cuando ingresa un número válido Entonces el sistema actualiza el teléfono.<br><br><strong>E02 – Número inválido:</strong> Dado que el usuario ingresa un formato incorrecto Cuando guarda cambios Entonces el sistema muestra un error y no lo actualiza.</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>US07</td>
      <td>Cambio de contraseña</td>
      <td>Como usuario general<br>Quiero cambiar mi contraseña<br>Para mantener segura mi cuenta</td>
      <td><strong>E01 – Contraseña actualizada:</strong> Dado que el usuario está en su perfil Cuando ingresa la contraseña actual y una nueva válida Entonces el sistema la actualiza y confirma el cambio.<br><br><strong>E02 – Parámetros no cumplidos:</strong> Dado que la nueva contraseña no cumple requisitos Cuando intenta guardarla Entonces el sistema muestra un mensaje de error.</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>US08</td>
      <td>Actualizar foto de perfil</td>
      <td>Como usuario general<br>Quiero cambiar mi foto de perfil<br>Para mantener mi información al día</td>
      <td><strong>E01 – Subida exitosa:</strong> Dado que el usuario selecciona una imagen válida Cuando la sube Entonces el sistema la guarda como avatar.<br><br><strong>E02 – Formato no permitido:</strong> Dado que el archivo no cumple el formato Cuando intenta subirlo Entonces el sistema muestra un error.</td>
      <td>EP02</td>
    </tr>
    <tr>
      <td>US09</td>
      <td>Mandar solicitud de cita</td>
      <td>Como médico<br>Quiero registrar fecha y hora de cita<br>Para coordinar atención con mis pacientes</td>
      <td><strong>E01 – Solicitud registrada:</strong> Dado que el médico elige fecha y hora válidas Cuando envía la petición Entonces la cita queda en el calendario y el paciente recibe notificación.<br><br><strong>E02 – Datos incompletos:</strong> Dado que falta fecha u hora Cuando intenta enviar Entonces el sistema muestra un error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US10</td>
      <td>Aceptar cita</td>
      <td>Como paciente<br>Quiero aceptar una cita<br>Para confirmar mi disponibilidad</td>
      <td><strong>E01 – Cita confirmada:</strong> Dado que el paciente recibe la solicitud Cuando pulsa “Aceptar” Entonces la cita se añade a su calendario.<br><br><strong>E02 – Cita expirada:</strong> Dado que la fecha ya pasó Cuando intenta aceptar Entonces el sistema informa que no es posible.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US11</td>
      <td>Cancelar cita</td>
      <td>Como paciente<br>Quiero cancelar una cita confirmada<br>Para reorganizar mi agenda</td>
      <td><strong>E01 – Cancelación exitosa:</strong> Dado que la cita está activa Cuando pulsa “Cancelar” Entonces se elimina y el médico recibe notificación.<br><br><strong>E02 – Cita no cancelable:</strong> Dado que la cita ya fue atendida o cancelada Cuando intenta cancelarla de nuevo Entonces el sistema muestra un mensaje de error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US12</td>
      <td>Reprogramar cita</td>
      <td>Como paciente<br>Quiero reprogramar una cita<br>Para ajustarla a mi disponibilidad</td>
      <td><strong>E01 – Nueva fecha válida:</strong> Dado que hay disponibilidad en la fecha elegida Cuando selecciona y guarda Entonces se actualiza la cita y notifica al médico.<br><br><strong>E02 – Sin disponibilidad:</strong> Dado que no hay huecos en esa fecha Cuando intenta reprogramar Entonces el sistema sugiere otras fechas.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US13</td>
      <td>Mandar solicitud de tratamiento</td>
      <td>Como médico<br>Quiero enviar una solicitud de tratamiento<br>Para iniciar o modificar el plan del paciente</td>
      <td><strong>E01 – Solicitud enviada:</strong> Dado que el médico completa el formulario Cuando pulsa “Enviar” Entonces el paciente recibe notificación con detalles.<br><br><strong>E02 – Campos vacíos:</strong> Dado que faltan datos obligatorios Cuando intenta enviar Entonces el sistema bloquea la acción y muestra error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US14</td>
      <td>Aceptar/Rechazar cambios en tratamiento</td>
      <td>Como paciente<br>Quiero decidir sobre cambios en mi tratamiento<br>Para mantener control de mi plan</td>
      <td><strong>E01 – Aceptar cambio:</strong> Dado que recibe la solicitud Cuando pulsa “Aceptar” Entonces el cambio se aplica y notifica al médico.<br><br><strong>E02 – Rechazar cambio:</strong> Dado que revisa la solicitud Cuando pulsa “Rechazar” Entonces el cambio no se aplica y el médico recibe notificación.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US15</td>
      <td>Personalizar fecha de inicio</td>
      <td>Como paciente<br>Quiero definir la fecha de inicio de mi tratamiento<br>Para adaptarlo a mi rutina</td>
      <td><strong>E01 – Fecha válida:</strong> Dado que el paciente elige una fecha futura Cuando guarda Entonces el sistema actualiza el inicio y genera recordatorios.<br><br><strong>E02 – Fecha inválida:</strong> Dado que elige una fecha pasada Cuando intenta guardar Entonces muestra un mensaje de error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US16</td>
      <td>Marcar cumplimiento de tratamiento</td>
      <td>Como paciente<br>Quiero marcar mi cumplimiento diario<br>Para llevar seguimiento de mi progreso</td>
      <td><strong>E01 – Registro diario:</strong> Dado que sigue su tratamiento Cuando marca el día Entonces el sistema guarda el progreso.<br><br><strong>E02 – Registro retroactivo:</strong> Dado que olvida marcar un día Cuando lo hace después Entonces el sistema permite la fecha pasada y actualiza su historial.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US17</td>
      <td>Asignar especialista</td>
      <td>Como médico<br>Quiero derivar a un paciente a un especialista<br>Para asegurar la mejor atención</td>
      <td><strong>E01 – Especialista existente:</strong> Dado que el médico elige un especialista del listado Cuando asigna Entonces el paciente recibe notificación para agendar cita.<br><br><strong>E02 – Especialista no listado:</strong> Dado que no encuentra al especialista Cuando ingresa nombre y contacto Entonces el sistema guarda la referencia y notifica al paciente.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US18</td>
      <td>Enviar síntomas</td>
      <td>Como paciente<br>Quiero reportar mis síntomas<br>Para que el doctor haga seguimiento clínico</td>
      <td><strong>E01 – Reporte exitoso:</strong> Dado que el paciente completa el formulario Cuando envía Entonces el síntoma queda registrado en el panel del médico.<br><br><strong>E02 – Sin tratamiento activo:</strong> Dado que no hay tratamiento asociado Cuando intenta reportar Entonces el sistema muestra un mensaje para seleccionar uno.</td>
      <td>EP06</td>
    </tr>
    <tr>
      <td>US19</td>
      <td>Revisar síntomas</td>
      <td>Como doctor<br>Quiero ver los síntomas reportados<br>Para evaluar la evolución del tratamiento</td>
      <td><strong>E01 – Síntomas disponibles:</strong> Dado que el paciente ha reportado síntomas Cuando el doctor accede al historial Entonces ve la lista ordenada por fecha.<br><br><strong>E02 – Sin reportes:</strong> Dado que no hay registros Cuando el doctor accede Entonces el sistema muestra un mensaje indicándolo.</td>
      <td>EP06</td>
    </tr>
    <tr>
      <td>US20</td>
      <td>Consultar medicamento</td>
      <td>Como paciente<br>Quiero consultar composición y reacciones<br>Para identificar efectos adversos</td>
      <td><strong>E01 – Detalles mostrados:</strong> Dado que el paciente selecciona un medicamento asignado Cuando abre su ficha Entonces ve ingredientes, dosis y advertencias.<br><br><strong>E02 – Reportar reacción:</strong> Dado que detecta un efecto adverso Cuando pulsa “Reportar” Entonces el sistema notifica al médico con detalles.</td>
      <td>EP06</td>
    </tr>
    <tr>
      <td>US21</td>
      <td>Notificaciones de cambios en tratamiento</td>
      <td>Como paciente<br>Quiero recibir avisos de cambios<br>Para estar siempre informado</td>
      <td><strong>E01 – Cambio propuesto:</strong> Dado que el médico envía una modificación Cuando el paciente abre la app Entonces recibe notificación con los detalles.<br><br><strong>E02 – Historial de cambios:</strong> Dado que hay notificaciones previas Cuando accede a notificaciones Entonces puede revisar todas las propuestas anteriores.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US22</td>
      <td>Notificación de fin de tratamiento</td>
      <td>Como doctor<br>Quiero recibir aviso de finalización<br>Para agendar cita de cierre</td>
      <td><strong>E01 – Marcado completado:</strong> Dado que el paciente marca el fin de tratamiento Cuando eso ocurre Entonces el sistema notifica al doctor.<br><br><strong>E02 – Agendar post-tratamiento:</strong> Dado que el doctor recibe la notificación Cuando accede al perfil del paciente Entonces puede programar la cita de evaluación.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US23</td>
      <td>Consulta a doctor</td>
      <td>Como paciente<br>Quiero hacer consultas via chat<br>Para resolver dudas sobre mi tratamiento</td>
      <td><strong>E01 – Envío de mensaje:</strong> Dado que el paciente redactor un mensaje Cuando pulsa “Enviar” Entonces el doctor recibe la consulta y queda registrada.<br><br><strong>E02 – Respuesta en tiempo real:</strong> Dado que el doctor responde Cuando publica la respuesta Entonces el paciente la ve inmediatamente.</td>
      <td>EP05</td>
    </tr>
    <tr>
      <td>US24</td>
      <td>Adjuntar archivos</td>
      <td>Como usuario general<br>Quiero enviar archivos por chat<br>Para compartir imágenes o resultados médicos</td>
      <td><strong>E01 – Archivo válido:</strong> Dado que el usuario elige un archivo permitido Cuando lo envía Entonces aparece en la conversación.<br><br><strong>E02 – Formato no admitido:</strong> Dado que el archivo no cumple extensiones permitidas Cuando intenta adjuntarlo Entonces el sistema muestra un error.</td>
      <td>EP05</td>
    </tr>
    <tr>
      <td>US25</td>
      <td>Agregar paciente</td>
      <td>Como doctor<br>Quiero invitar a un paciente por usuario<br>Para añadirlo a mi lista y asignarle tratamiento</td>
      <td><strong>E01 – Usuario válido:</strong> Dado que el doctor introduce un username existente Cuando envía la invitación Entonces el paciente recibe notificación y puede aceptar.<br><br><strong>E02 – Usuario inexistente:</strong> Dado que el username no está registrado Cuando intenta enviar Entonces el sistema muestra un mensaje de error.</td>
      <td>EP05</td>
    </tr>
    <tr>
      <td>US26</td>
      <td>Crear procedimiento</td>
      <td>Como doctor<br>Quiero definir procedimientos médicos<br>Para estructurar el plan de tratamiento</td>
      <td><strong>E01 – Procedimiento guardado:</strong> Dado que el doctor completa todos los datos Cuando guarda Entonces el procedimiento queda asociado al tratamiento.<br><br><strong>E02 – Campos obligatorios vacíos:</strong> Dado que falta información Cuando intenta guardar Entonces el sistema advierte y no registra.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US27</td>
      <td>Resumen de tratamiento</td>
      <td>Como paciente<br>Quiero ver un resumen de mi tratamiento<br>Para conocer fechas, medicación y procedimientos</td>
      <td><strong>E01 – Vista previa completa:</strong> Dado que el paciente accede antes de aceptar Cuando abre el resumen Entonces ve todos los detalles del plan.<br><br><strong>E02 – Aceptar desde resumen:</strong> Dado que revisa el contenido Cuando pulsa “Aceptar” Entonces el tratamiento se activa en su cuenta.</td>
      <td>EP06</td>
    </tr>
    <tr>
      <td>US28</td>
      <td>Configurar procedimiento</td>
      <td>Como doctor<br>Quiero ajustar duración y frecuencia<br>Para adaptar cada procedimiento al caso</td>
      <td><strong>E01 – Parámetros válidos:</strong> Dado que define duración y repeticiones dentro de rango Cuando guarda Entonces el sistema los registra correctamente.<br><br><strong>E02 – Valores fuera de rango:</strong> Dado que ingresa datos inválidos Cuando intenta guardar Entonces se bloquea la operación y muestra error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US29</td>
      <td>Modificar fecha de inicio</td>
      <td>Como paciente<br>Quiero cambiar la fecha de inicio<br>Para disponer de tiempo para prepararme</td>
      <td><strong>E01 – Cambio válido:</strong> Dado que selecciona una fecha futura Cuando guarda Entonces la fecha se actualiza y notifica al doctor.<br><br><strong>E02 – Fecha pasada:</strong> Dado que elige un día anterior Cuando intenta guardar Entonces el sistema muestra un error.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US30</td>
      <td>Configurar recordatorios</td>
      <td>Como usuario general<br>Quiero personalizar mis notificaciones<br>Para adaptarlas a mi rutina diaria</td>
      <td><strong>E01 – Ajuste exitoso:</strong> Dado que modifica tono y frecuencia Cuando guarda Entonces los recordatorios se actualizan.<br><br><strong>E02 – Horario no seleccionado:</strong> Dado que no define hora alguna Cuando intenta guardar Entonces el sistema indica que debe elegir al menos un horario.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US31</td>
      <td>Aviso de cambios en el sistema</td>
      <td>Como usuario general<br>Quiero recibir notificaciones de cambios<br>Para estar al tanto de reprogramaciones y ajustes</td>
      <td><strong>E01 – Notificación inmediata:</strong> Dado que se reprograma o cancela una cita Cuando ocurre el cambio Entonces el usuario recibe alerta en la app.<br><br><strong>E02 – Historial de avisos:</strong> Dado que hay varios cambios Cuando consulta el buzón de notificaciones Entonces ve el listado cronológico.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US32</td>
      <td>Eliminar paciente</td>
      <td>Como médico<br>Quiero eliminar pacientes finalizados<br>Para mantener organizada mi lista</td>
      <td><strong>E01 – Eliminación exitosa:</strong> Dado que el paciente marcó tratamiento como completo Cuando el doctor pulsa “Eliminar” Entonces se remueve de su lista.<br><br><strong>E02 – Paciente activo:</strong> Dado que aún hay un tratamiento en curso Cuando intenta eliminar Entonces el sistema deniega la acción.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US33</td>
      <td>Contactar con soporte</td>
      <td>Como usuario general<br>Quiero contactar con el equipo de soporte<br>Para resolver dudas o reportar errores</td>
      <td><strong>E01 – Mensaje enviado:</strong> Dado que completa el formulario de contacto Cuando pulsa “Enviar” Entonces llega al equipo y el usuario recibe confirmación.<br><br><strong>E02 – Campos vacíos:</strong> Dado que faltan datos obligatorios Cuando intenta enviar Entonces el sistema muestra error y bloquea envío.</td>
      <td>EP05</td>
    </tr>
    <tr>
      <td>US34</td>
      <td>Lista de pacientes</td>
      <td>Como médico<br>Quiero ver mi lista de pacientes<br>Para acceder a sus tratamientos y progreso</td>
      <td><strong>E01 – Lista poblada:</strong> Dado que hay pacientes asignados Cuando el doctor accede Entonces ve la lista con nombres y estado de tratamiento.<br><br><strong>E02 – Lista vacía:</strong> Dado que no tiene pacientes aún Cuando accede Entonces se muestra un mensaje indicándolo.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US35</td>
      <td>Revisar historial de tratamientos</td>
      <td>Como médico<br>Quiero ver el historial de tratamientos<br>Para tener visión cronológica de la evolución</td>
      <td><strong>E01 – Historial disponible:</strong> Dado que el paciente tiene registros anteriores Cuando el doctor abre su perfil Entonces ve la lista ordenada cronológicamente.<br><br><strong>E02 – Sin historial:</strong> Dado que no hay registros Cuando intenta ver el historial Entonces el sistema muestra un mensaje de ausencia de datos.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US36</td>
      <td>Lista de procedimientos</td>
      <td>Como paciente<br>Quiero ver los procedimientos del día<br>Para cumplir correctamente mi tratamiento</td>
      <td><strong>E01 – Procedimientos mostrados:</strong> Dado que hay procedimientos asignados hoy Cuando el paciente accede Entonces ve la lista detallada.<br><br><strong>E02 – Ninguno asignado:</strong> Dado que no hay procedimientos para la fecha Cuando consulta Entonces el sistema informa que no hay tareas.</td>
      <td>EP03</td>
    </tr>
    <tr>
      <td>US37</td>
      <td>Visualizar landing page</td>
      <td>Como usuario general<br>Quiero ver la landing page<br>Para entender la propuesta de valor</td>
      <td><strong>E01 – Contenido cargado:</strong> Dado que accede al sitio Cuando entra en la landing Entonces ve descripción clara y beneficios.<br><br><strong>E02 – Error de carga:</strong> Dado que falla el servidor Cuando entra Entonces el sistema muestra mensaje de indisponibilidad.</td>
      <td>EP07</td>
    </tr>
    <tr>
      <td>US38</td>
      <td>Acceso a la app</td>
      <td>Como usuario<br>Quiero ser redirigido a la tienda de apps<br>Para descargar fácilmente OnControl</td>
      <td><strong>E01 – Redirección válida:</strong> Dado que pulsa el botón de descarga Cuando está en la landing Entonces va a App Store o Play Store según dispositivo.<br><br><strong>E02 – Enlace roto:</strong> Dado que el enlace falla Cuando pulsa el botón Entonces el sistema muestra un error y ofrece contacto con soporte.</td>
      <td>EP07</td>
    </tr>
    <tr>
      <td>US39</td>
      <td>Recibir información por correo</td>
      <td>Como usuario general<br>Quiero recibir mis registros por email<br>Para conservar un respaldo de mis actividades</td>
      <td><strong>E01 – Envío exitoso:</strong> Dado que introduce un correo válido Cuando solicita el envío Entonces el sistema envía el resumen de actividad.<br><br><strong>E02 – Correo inválido:</strong> Dado que el formato no es correcto Cuando confirma Entonces el sistema muestra un error y no envía el email.</td>
      <td>EP07</td>
    </tr>
  </tbody>
</table>

<il><h3><a href="./content/chapter-3/chapter-3.md">3.3. Impact Mapping</a></h3></il>
  
En esta sección, se ha llevado a cabo la creación del impact mapping, partiendo de las metas comerciales establecidas para cada user persona. Se han identificado los impactos deseados, los entregables necesarios y se han relacionado con las historias de usuario correspondientes.

Segmento objetivo: Pacientes y familiares

<img src="https://github.com/user-attachments/assets/3aa5f839-07f7-4c58-80f3-f4f6b9d007b7" >


Segmento objetivo: Oncólogos


<img src="https://github.com/user-attachments/assets/59b450d1-59c0-4f12-9870-d5696374a1b0" >

<il><h3><a href="./content/chapter-3/chapter-3.md">3.4. Product Backlog</a></h3></il>

<table border="1">
    <tr>
        <th>#Orden</th>
        <th>User Story Id</th>
        <th>Título</th>
        <th>Description</th>
        <th>Story Points (1/2/3/5/8)</th>
    </tr>
    <tr>
        <td>1</td>
        <td>EP01-US01</td>
        <td>Registrar Cuenta</td>
        <td>Como usuario general<br>Quiero registrar una cuenta<br>Para acceder a la aplicación OnControl</td>
        <td>5</td>
    </tr>
    <tr>
        <td>2</td>
        <td>EP01-US02</td>
        <td>Configurar pagos</td>
        <td>Como usuario general<br>Quiero configurar mis métodos de pago<br>Para poder acceder a servicios adicionales ofrecidos por OnControl</td>
        <td>3</td>
    </tr>
    <tr>
        <td>3</td>
        <td>EP01-US03</td>
        <td>Iniciar sesion</td>
        <td>Como usuario general<br>Quiero iniciar sesión en mi cuenta<br>Para acceder a las funciones de la aplicación</td>
        <td>3</td>
    </tr>
    <tr>
        <td>4</td>
        <td>EP01-US04</td>
        <td>Cierre de sesión</td>
        <td>Como usuario general<br>Quiero cerrar mi cuenta al terminar de usar el aplicativo<br>Para evitar que otras personas accedan a mi cuenta</td>
        <td>2</td>
    </tr>
    <tr>
        <td>5</td>
        <td>EP01-US05</td>
        <td>Recuperación de cuenta</td>
        <td>Como usuario general<br>Quiero tener la opción de recuperar mi cuenta<br>Para no perder mis datos ya registrados</td>
        <td>1</td>
    </tr>
    <tr>
        <td>6</td>
        <td>EP02-US06</td>
        <td>Cambio de número telefónico</td>
        <td>Como usuario general<br>Quiero cambiar el número de teléfono asociado a mi cuenta<br>Para que puedan contactarse conmigo</td>
        <td>1</td>
    </tr>
    <tr>
        <td>7</td>
        <td>EP02-US07</td>
        <td>Cambio de contraseña</td>
        <td>Como usuario general<br>Quiero cambiar la contraseña asociada a mi cuenta<br>Para mantener la seguridad de mi cuenta</td>
        <td>1</td>
    </tr>
    <tr>
        <td>8</td>
        <td>EP02-US08</td>
        <td>Actualizar foto de perfil</td>
        <td>Como usuario general<br>Quiero cambiar mi foto de perfil<br>Para mantener mi perfil actualizado</td>
        <td>1</td>
    </tr>
    <tr>
        <td>9</td>
        <td>EP03-US09</td>
        <td>Mandar solciitud cita</td>
        <td>Como médico<br>Quiero registrar una fecha y hora de cita en calendario<br>Para coordinar la atención con mis pacientes</td>
        <td>5</td>
    </tr>
    <tr>
        <td>10</td>
        <td>EP03-US10</td>
        <td>Aceptar cita</td>
        <td>Como paciente<br>Quiero aceptar citas en la aplicación<br>Para confirmar mi disponibilidad y asistir al encuentro con el doctor</td>
        <td>5</td>
    </tr>
    <tr>
        <td>11</td>
        <td>EP03-US11</td>
        <td>Cancelar cita</td>
        <td>Como paciente<br>Quiero cancelar una cita previamente confirmada<br>Para reorganizar mi disponibilidad o reagendar con el doctor</td>
        <td>3</td>
    </tr>
    <tr>
        <td>12</td>
        <td>EP03-US12</td>
        <td>Reprogramar cita</td>
        <td>Como paciente<br>Quiero reprogramar una cita médica<br>Para ajustarla a mi disponibilidad y continuar con mi tratamiento sin interrupciones</td>
        <td>3</td>
    </tr>
    <tr>
        <td>13</td>
        <td>EP03-US13</td>
        <td>Mandar solicitud de tratamiento</td>
        <td>Como usuario médico<br>Quiero enviar una solicitud de tratamiento a un paciente<br>Para iniciar o modificar su plan de atención médica de forma clara y registrada</td>
        <td>5</td>
    </tr>
    <tr>
        <td>14</td>
        <td>EP03-US14</td>
        <td>Aceptar solicitud de cambios en tratamiento</td>
        <td>Como paciente<br>Quiero aceptar o rechazar una solicitud de cambios en mi tratamiento<br>Para tener control y conocimiento sobre las decisiones médicas que me afectan</td>
        <td>2</td>
    </tr>
    <tr>
        <td>15</td>
        <td>EP03-US15</td>
        <td>Personalizar fecha de inicio tratamiento</td>
        <td>Como paciente <br>Quiero definir la fecha de inicio de mi tratamiento<br>Para ajustarla a mi disponibilidad y plan personal de salud</td>
        <td>3</td>
    </tr>
    <tr>
        <td>16</td>
        <td>EP03-US16</td>
        <td>Marcar cumplimiento de tratamiento</td>
        <td>Como paciente<br>Quiero marcar el cumplimiento diario de mi tratamiento<br>Para llevar un seguimiento adecuado de mi progreso médico</td>
        <td>3</td>
    </tr>
    <tr>
        <td>17</td>
        <td>EP03-US17</td>
        <td>Asignar especialista</td>
        <td>Como médico<br>Quiero tratar mi paciente con un médico especializado<br>Para mantener correctamente la salud del paciente</td>
        <td>3</td>
    </tr>
    <tr>
        <td>18</td>
        <td>EP06-US18</td>
        <td>Enviar sintomas</td>
        <td>Como paciente<br>Quiero enviar síntomas registrados en un tratamiento<br>Para que el doctor tenga un registro del estado de salud durante el tratamiento y pueda hacer seguimiento clínico</td>
        <td>3</td>
    </tr>
    <tr>
        <td>19</td>
        <td>EP06-US19</td>
        <td>Revisar sintomas</td>
        <td>Como doctor<br>Quiero ver la lista de síntomas reportados por el paciente<br>Para evaluar la evolución del tratamiento y tomar decisiones médicas informadas</td>
        <td>3</td>
    </tr>
    <tr>
        <td>20</td>
        <td>EP06-US20</td>
        <td>Consultar medicamento</td>
        <td>Como paciente<br>Quiero consultar la composición de medicamentos y posibles reaccioneso<br>Para identificar efectos adversos, comparar con síntomas graves y enviar información al doctor para su evaluación</td>
        <td>5</td>
    </tr>
    <tr>
        <td>21</td>
        <td>EP03-US21</td>
        <td>Recibir notificaciones de cambios en tratamiento</td>
        <td>Como paciente<br>Quiero recibir notificación sobre solicitudes de cambios en el tratamiento<br>Para estar informado y tomar decisiones sobre la continuidad o modificación del plan terapéutico</td>
        <td>2</td>
    </tr>
    <tr>
        <td>22</td>
        <td>EP03-US22</td>
        <td>Recibir notificacion de culminacion de tratamiento</td>
        <td>Como doctor<br>Quiero recibir notificación de finalización de tratamiento de los pacientes<br>Para agendar una cita de cierre, evaluar el progreso del paciente y definir próximos pasos si son necesarios</td>
        <td>2</td>
    </tr>
    <tr>
        <td>23</td>
        <td>EP05-US23</td>
        <td>Consulta a doctor</td>
        <td>Como paciente<br>Quiero realizar consultas generales al doctor a través del chat<br>Para resolver dudas sobre mi tratamiento o estado de salud</td>
        <td>5</td>
    </tr>
    <tr>
        <td>24</td>
        <td>EP05-US24</td>
        <td>Adjuntar archivos</td>
        <td>Como usuario general<br>Quiero poder adjuntar archivos para enviarlos por chat<br>Para compartir imágenes, recetas o resultados médicos con el doctor</td>
        <td>2</td>
    </tr>
    <tr>
        <td>25</td>
        <td>EP05-US25</td>
        <td>Agregar paciente</td>
        <td>Como doctor<br>Quiero enviar una solicitud de atención a paciente usando su nombre de usuario<br>Para agregarlo a mi lista de pacientes y asignarle un tratamiento</td>
        <td>5</td>
    </tr>
    <tr>
        <td>26</td>
        <td>EP03-US26</td>
        <td>Crear procedimiento</td>
        <td>Como doctor<br>Quiero agregar procedimientos que debe realizar el paciente<br>Para definir los pasos del tratamiento, asignar tareas específicas y hacer seguimiento de su cumplimiento</td>
        <td>8</td>
    </tr>
    <tr>
        <td>27</td>
        <td>EP06-US27</td>
        <td>Resumen de tratamiento</td>
        <td>Como paciente<br>Quiero ver un resumen del tratamiento que voy a seguir<br>Para tener una vista general antes de aceptarlo, incluyendo fechas, medicamentos, procedimientos y duración</td>
        <td>8</td>
    </tr>
    <tr>
        <td>28</td>
        <td>EP03-US28</td>
        <td>Configurar procedimiento</td>
        <td>Como doctor<br>Quiero tener control sobre el tipo de procedimiento que se asignará<br>Para definir su duración, frecuencia y condiciones específicas según cada caso</td>
        <td>5</td>
    </tr>
    <tr>
        <td>29</td>
        <td>EP03-US29</td>
        <td>Modificar la fecha de inicio</td>
        <td>Como paciente<br>Quiero modificar la fecha de inicio del tratamiento<br>Para tener un margen de tiempo para conseguir los medicamentos o programar citas con especialistas</td>
        <td>2</td>
    </tr>
    <tr>
        <td>30</td>
        <td>EP03-US30</td>
        <td>Configuracion de recordatorios</td>
        <td>Descripción:<br>Como usuario en general<br>Quiero personalizar las notificaciones, tonos, duración y repetición de los recordatorios<br>Para adaptarlos a mi rutina diaria y no olvidar mis actividades médicas</td>
        <td>1</td>
    </tr>
    <tr>
        <td>31</td>
        <td>EP03-US31</td>
        <td>Aviso de cambios en el sistema</td>
        <td>Como usuario en general<br>Quiero ser notificado si se ha realizado algún cambio en el calendario<br>Para estar al tanto de citas reprogramadas, cancelaciones o ajustes en mi tratamiento</td>
        <td>1</td>
    </tr>
    <tr>
        <td>32</td>
        <td>EP03-US32</td>
        <td>Eliminar paciente</td>
        <td>Como doctor<br>Quiero eliminar pacientes que ya cumplieron con su tratamiento<br>Para mantener organizada mi lista de pacientes activos</td>
        <td>2</td>
    </tr>
    <tr>
        <td>33</td>
        <td>EP05-US33</td>
        <td>Contactar con OnControl</td>
        <td>Como usuario general<br>Quiero contactar con el equipo de soporte de OnControl<br>Para resolver dudas, reportar errores o recibir ayuda técnica</td>
        <td>5</td>
    </tr>
    <tr>
        <td>34</td>
        <td>EP03-US34</td>
        <td>Lista de pacientes</td>
        <td>Como doctor<br>Quiero ver la lista de mis pacientes<br>Para acceder rápidamente a sus tratamientos y consultar su progreso</td>
        <td>5</td>
    </tr>
    <tr>
        <td>35</td>
        <td>EP03-US35</td>
        <td>Revisar historial de tratamientos</td>
        <td>Como doctor<br>Quiero ver el historial completo de los tratamientos realizados por el paciente desde que empezó a usar la aplicación<br>Para tener una visión cronológica de su evolución médica</td>
        <td>5</td>
    </tr>
    <tr>
        <td>36</td>
        <td>EP03-US36</td>
        <td>Lista de procedimientos</td>
        <td>Como paciente<br>Quiero ver la lista de procedimientos a seguir el día de hoy y de forma detallada<br>Para asegurarme de cumplir con mi tratamiento correctamente</td>
        <td>5</td>
    </tr>
    <tr>
        <td>37</td>
        <td>EP07-US37</td>
        <td>Visualizar landing page</td>
        <td>Como usuario en general<br>Quiero dar un primer vistazo a la aplicación y conocer en qué consiste<br>Para entender su funcionalidad mediante una landing page clara y atractiva</td>
        <td>8</td>
    </tr>
    <tr>
        <td>38</td>
        <td>EP07-US38</td>
        <td>Acceso a la app</td>
        <td>Como usuario<br>Quiero ser redirigido a la tienda donde puedo descargar la app<br>Para instalarla fácilmente y comenzar a usarla</td>
        <td>5</td>
    </tr>
    <tr>
        <td>39</td>
        <td>EP07-US39</td>
        <td>Recibir informacion</td>
        <td>Como usuario general<br>Quiero recibir información completa al correo electrónico<br>Para tener una copia detallada de mis registros o actividades realizadas en la app</td>
        <td>2</td>
    </tr>
</table>
