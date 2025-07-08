## Capitulo VI: Product Implementation, Validation & Deployment

### 6.1 Software Configuration Management

#### 6.1.1. Software Development Environment Configuration.

##### Product UX/UI Design

- Uxpressia: Herramienta en línea para mapeo de trayectoria del cliente, creación de mapas de impacto y personas.  


- Figma: Pizarra digital colaborativa en línea para investigación, ideación, lluvias de ideas y mapas mentales.  
[https://www.figma.com/file/9fLXXyhFtxOwF2iFs8gBdM/Oncontigo-Mockups?type=design&node-id=0-1&mode=design&t=HkEWLTZnf3N6FtXp-0](https://www.figma.com/file/9fLXXyhFtxOwF2iFs8gBdM/Oncontigo-Mockups?type=design&node-id=0-1&mode=design&t=HkEWLTZnf3N6FtXp-0)

- Structurizr: Herramienta de diseño que soporta el modelo C4 para visualizar arquitecturas de software.  
[https://structurizr.com/](https://structurizr.com/)

- Lucid Chart: Herramienta de diagramación en línea para la colaboración en tiempo real para el desarrollo de nuestros esquemas.  
[https://lucid.app/lucidchart/84ff4b37-35d8-4d28-96f5-8e7fc2ef6c93/edit?viewport_loc=-10%2C-10%2C1813%2C789%2C0_0&invitationId=inv_f86e0e0e-cfe1-48c8-a60d-869b7a147a57](https://lucid.app/lucidchart/84ff4b37-35d8-4d28-96f5-8e7fc2ef6c93/edit?viewport_loc=-10%2C-10%2C1813%2C789%2C0_0&invitationId=inv_f86e0e0e-cfe1-48c8-a60d-869b7a147a57)

- MIRO: Pizarra digital colaborativa en línea para diversas actividades colaborativas.  
[https://miro.com/app/dashboard/](https://miro.com/app/dashboard/)

##### Software Development

Estructura aplicada al desarrollo de un producto de software.

- Github: Repositorio comunitario para almacenar avances de proyectos colaborativos.  
[https://github.com/OnControlUPC](https://github.com/OnControlUPC)

- Visual Studio Code: Editor de código que ofrece extensiones y funcionalidades para el desarrollo eficiente, utilizado para construir backend de aplicaciones web.  
[https://code.visualstudio.com/](https://code.visualstudio.com/)

- HTML: Lenguaje para el desarrollo de plataformas web, será utilizado para el desarrollo de la landing page.  
[https://www.jetbrains.com/help/webstorm/editing-html-files.html](https://www.jetbrains.com/help/webstorm/editing-html-files.html)

- CSS: Lenguaje de diseño gráfico para la elaboración de interfaces de usuario.  
[https://www.jetbrains.com/help/webstorm/style-sheets.html#ws_css_completion](https://www.jetbrains.com/help/webstorm/style-sheets.html#ws_css_completion)

- Kotlin: Lenguaje de programación principal para aplicaciones android, utilizada para nuestro proyecto.
[https://kotlinlang.org/](https://kotlinlang.org/)

##### Software Deployment

- Github pages: Servicio para alojar páginas web estáticas y aplicaciones web.  
[https://pages.github.com/](https://pages.github.com/)

#### 6.1.2. Source Code Management.

##### Enlaces Importantes

- **Organización en GitHub**: [OnControl](https://github.com/OnControlUPC)
- **Repositorio del Landing Page**: [OnControl Landing Page](https://github.com/OnControlUPC/landingprueba)

###### GitFlow

GitFlow es un flujo de trabajo de control de versiones que facilita la gestión de ramas durante el desarrollo:

###### Main Branches

- `main`: Rama principal que contiene el historial de publicación oficial y todas las versiones.
- `develop`: Rama creada desde `main`, integra todas las funciones estables y prepara la próxima versión.

###### Support Branches

Estas ramas son temporales y se eliminan después de integrarse en sus ramas principales.

###### Feature

- **Origen**: `develop`
- **Destino**: `develop`
- Se utilizan para el desarrollo de nuevas funcionalidades, existen mientras están en desarrollo y luego se integran a `develop`.

###### Release

- **Origen**: `develop`
- **Destino**: `develop` / `main`
- Preparan la nueva versión de producción, corrigen errores menores y preparan metadatos para el lanzamiento.

###### Motivos para usar Gitflow

- Adecuado para proyectos con lanzamientos programados.
- Combina los beneficios de un flujo centralizado y descentralizado.
- Permite trabajo individual, ideal cuando el equipo tiene horarios diferentes.
- Requiere actualización constante en el repositorio central.

Cada miembro del equipo debe mantener su trabajo al día con el repositorio central en GitHub para garantizar la cohesión y el progreso del proyecto.

#### 6.1.3. Source Code Style Guide & Conventions.

##### Nomenclatura General

- Utilizaremos términos en inglés para nombrar variables, objetos, elementos y funciones que describan claramente su propósito.
- No se utilizarán mayúsculas arbitrarias para mantener la legibilidad del código.

Ejemplo de nomenclatura estándar:
```css
Calendar.kt 
getMedication(){}
.login {}
```

#### Sangria
- En HTML, CSS y JavaScript, aplicaremos espacios antes de cada línea dentro de un bloque.
- Se recomienda usar dos espacios y evitar la tecla “Tabulación”.
- Ejemplo de sangría en HTML:
    ```css
    <table>
    <tr>
        <th>Name</th>
        <th>Description</th>
    </tr>
    </table>
    ```
- Ejemplo de sangría en CSS:
    ```css
    html {
    background: #fff;
    color: #404;
    }
    ```
- Ejemplo de sangría en JavaScript:
    ```css
    function toCelsius(fahrenheit) {
        return (5 / 9) * (fahrenheit - 32);
    }
    ```

###### HTML

- Declare Document Type: Siempre declare el tipo de documento como HTML5 con <!DOCTYPE html>.
- Blank Lines: Deje líneas en blanco después de bloques de gran longitud.
- Quote Attribute Values: Utilice comillas dobles alrededor de los valores de los atributos.
- Multimedia Fallback: Asegure acceso alternativo para multimedia y añada dimensiones a los elementos.
- Never Skip the <tittle> Element: El título de la página es crucial para SEO y se muestra en los resultados de búsqueda.
- HTML Line-Wrapping: Evite líneas de código extensas. Utilice espacios para diferenciar elementos hijos.
###### CSS
- Shorthand Properties: Utilice la menor cantidad de líneas posibles para declarar propiedades.
- Declaration Stops: Ponga un punto y coma después de cada declaración.
- Property Name Stops: Incluya un espacio después de los dos puntos en una declaración de propiedad.
- Declaration Block Separation: Separe el nombre de un selector y el inicio de un bloque con un espacio.
- CSS Quotation Marks: Utilice comillas simples para valores de atributos y selectores.
###### JavaScript
- Spaces around operators: Incluya un espacio alrededor de los operadores.
- Simple Statement’s End: Finalice las declaraciones simples con un punto y coma.
- Beginning and End of a Function: Coloque una llave al final de la primera línea de una función y la llave de cierre sola en la última línea.
###### Gherkin
- Discernible Given-When-Then Blocks: Utilice la sangría para identificar fácilmente los pasos de un escenario.
- Step with Tables: Para los pasos que requieran valores, utilice tablas.
- Reducing Noise: Use valores por defecto en los pasos y coloque valores "estándar" entre comillas simples.
- Scenarios Separator: Separe escenarios con saltos de línea y comentarios para facilitar la visualización.
###### Kotlin

- UpperCamelCase para Clases y Objetos: Nombra clases, objetos, interfaces y tipos usando mayúscula inicial en cada palabra (por ejemplo, UserProfile, MainActivity).

- lowerCamelCase para Variables y Funciones: Usa minúscula inicial seguida de mayúsculas para palabras intermedias (por ejemplo, userName, calculateTotal).

- Constantes con UPPER_SNAKE_CASE: Declara constantes con letras mayúsculas y guiones bajos para separar palabras (por ejemplo, MAX_COUNT, API_BASE_URL).

- Funciones Cortas con Expresión Única: Si la función contiene una sola expresión, omite las llaves y usa la sintaxis = (por ejemplo, fun sum(a: Int, b: Int) = a + b).

- Uso de val por defecto: Prefiere val sobre var siempre que sea posible para garantizar inmutabilidad.

- Visibilidad Explícita: Declara explícitamente la visibilidad (private, internal, public) en miembros no públicos.

- Imports Organizados: No se utiliza import *, solo se importa lo necesario y organizado alfabéticamente.

- Clases de Datos (data class): Utiliza data class para estructuras que almacenan datos, incluye todos los campos clave en el constructor primario..

#### 6.1.4. Software Deployment Configuration.

- Como ya se ha mencionado, la gestión de nuestro código fuente se realizará a través de GitHub. Asimismo, se utilizará GitHub Pages para la publicación y despliegue de la página. Cada sección del Landing Page que se ha creado deberá aparecer en el siguiente vínculo:
https://oncontrolupc.github.io/landingprueba/
- Para el desarrollo del Landing Page de OnControl se han utilizado las siguientes herramientas:
    - Html: Es el lenguaje de marcado que estructuro nuestro Landing Page.
      Evidencia: Archivos HTML, el principal es index.html donde todos los integrantes juntaron el contenido realizado en su rama individual.
    - Css: Es aquel que nos ayudó con el diseño gráfico para que el Landing Page sea agradable e interactúable.
      Evidencia: Se presenta el file styles.css, donde el grupo implemento el diseño de toda la estructura realizada con html.
    - JS: Nos ayudó a desarrollar la lógica necesaria para el Landing Page.
      Evidencia: Se muestra el documento main.js.

- El despliegue del Landing Page de OnControl no pudo ser posible sin utilizar las siguientes tecnologías:
    - Git: Sistema de control de versiones que está pensado en la eficiencia y compatibilidad de versiones, el cual nos ayudó a trabajar en equipo durante el desarrollo del Landing Page
    - Github: Plataforma de desarrollo colaborativo
    - Git Flow: Nos permitió controlar el avance de cada uno de nuestros integrantes con respecto al desarrollo del Landing Page
    -  Git Hub Pages: Servicio de Github que nos permitió alojar nuestra Landing page.
- Asimismo, se han realizado los siguientes pasos:
    - Dirigirse al repositorio de la página: Dado que se ha empleado Github, debemos ir al repositorio creado en este sitio web para publicar el Landing Page que ha desarrollado el equipo. Desde aquí, se podrá iniciar la configuración del vínculo de la página dirigiéndonos al apartado de Settings.
    - Ir a la opción de páginas: Una vez presentes la configuración del repositorio, debemos dirigirnos a la sección de Pages. Esto se debe a que ahí se encuentran todas las opciones de configuración de publicación de la página en un link o vínculo

    -   Elección de rama y carpeta de guardado: Dentro de pages, se debe seleccionar la rama o branch que se va a publicar en el vínculo. De la misma manera, se tiene que elegir la carpeta donde se localizará esta publicación a realizar. Finalmente podremos acceder a nuestra página con el link que aparece en la parte superior de este apartado de configuración

-   Siguiendo los pasos, obtenemos el siguiente enlace:
https://oncontrolupc.github.io/landingprueba/
   </ul>

### 6.2.1. Sprint 1

En esta sección se expone el avance correspondiente al Sprint 1, planificando el desarrollo y despliegue del Landing Page de la startup. Adicionalmente, durante este sprint se sentaron las bases para el backend de la aplicación, se definieron los procesos de despliegue iniciales y se realizó una primera aproximación al desarrollo de la app móvil. Se incorporan el Sprint Planning, el Sprint Backlog, evidencias del desarrollo y ejecución para la Sprint Review

### 6.2.1.1. Sprint Planning 1


<table>
    <tr>
        <th>Sprint 1</th>
        <td>Sprint 1</td>
    </tr>
    <tr>
        <th>Sprint Planning Date</th>
        <td>2025-05-05</td>
    </tr>
    <tr>
        <th>Time</th>
        <td>03:00 PM</td>
    </tr>
    <tr>
        <th>Location</th>
        <td>Meet</td>
    </tr>
    <tr>
        <th>Prepared By</th>
        <td>Quique Vladimir Jara Benites</td>
    </tr>
    <tr>
        <th>Attendees</th>
        <td>Williams Góngora / Oscar Garayar / Juan Ramos / Michael Quispe / Williams Góngora</td>
    </tr>
    <tr>
        <th>Sprint Goal</th>
        <td>Entregar Landing Page funcional, desarrollo del Backend y estructura inicial con funcionalidades para la app móvil.</td>
    </tr>
    <tr>
        <th>Sprint Velocity</th>
        <td>5</td>
    </tr>
    <tr>
        <th>Sum of Story Points</th>
        <td>18</td>
    </tr>
</table>

<br>


### 6.2.1.2. Sprint Backlog 1

Esta primera iteración se centró en el desarrollo y despliegue completo de nuestra Landing Page, junto con la creación y el despliegue de la arquitectura del backend principal y la implementación de la primera versión de nuestra aplicación móvil.

<br>

<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Título</th>
            <th>Épica</th>
            <th>Responsable</th>
            <th>Puntos</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>US37</td>
            <td>Visualizar landing page</td>
            <td>Landing Page</td>
            <td>Williams Gongora</td>
            <td>8</td>
        </tr>
        <tr>
            <td>US38</td>
            <td>Acceso a la app</td>
            <td>Landing Page</td>
            <td>Williams Gongora</td>
            <td>3</td>
        </tr>
        <tr>
            <td>US01</td>
            <td>Registrar cuenta</td>
            <td>Autenticación (Backend & App)</td>
            <td>Vladimir Jara</td>
            <td>5</td>
        </tr>
        <tr>
            <td>US03</td>
            <td>Iniciar sesión</td>
            <td>Autenticación (Backend & App)</td>
            <td>Vladimir Jara</td>
            <td>5</td>
        </tr>
        <tr>
            <td>US04</td>
            <td>Cerrar sesión</td>
            <td>Autenticación (Backend & App)</td>
            <td>Vladimir Jara</td>
            <td>5</td>
        </tr>
        <tr>
            <td>US05</td>
            <td>Recuperación de cuenta</td>
            <td>Autenticación (Backend & App)</td>
            <td>Vladimir Jara</td>
            <td>5</td>
        </tr>
    </tbody>
</table>


   <table border="1">
    <tr>
        <th>Sprint #</th>
        <th>User Story</th>
        <th>Work-item/Task</th>
        <th>Id</th>
        <th>Title</th>
        <th>Description</th>
        <th>Estimation (Hours)</th>
        <th>Assigned To</th>
        <th>Status</th>
    </tr>
    <tr>
        <td rowspan="3">Sprint 1</td>
        <td rowspan="3">US37: Visualizar landing page</td>
        <td>TA01</td>
        <td>#182062301</td>
        <td>Diseño UI/UX landing</td>
        <td>Crear prototipo Figma con estructura básica y elementos visuales</td>
        <td>8</td>
        <td>Williams Góngora</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>TA02</td>
        <td>#182062302</td>
        <td>Desarrollo frontend básico</td>
        <td>Implementar estructura HTML/CSS con responsive design</td>
        <td>12</td>
        <td>Williams Góngora</td>
        <td>Dones</td>
    </tr>
    <tr>
        <td>TA03</td>
        <td>#182062303</td>
        <td>Integración con redes sociales</td>
        <td>Agregar botones sociales y enlaces funcionales</td>
        <td>4</td>
        <td>Williams Góngora</td>
        <td>Done</td>
    </tr>
    <tr>
        <td rowspan="2">Sprint 1</td>
        <td rowspan="2">US01: Registrar cuenta</td>
        <td>TA04</td>
        <td>#182062304</td>
        <td>API de registro</td>
        <td>Desarrollar endpoint POST /register con validación básica</td>
        <td>6</td>
        <td>Vladimir Jara</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>TA05</td>
        <td>#182062305</td>
        <td>Formulario de registro</td>
        <td>Crear componente React con validación de campos para registro</td>
        <td>8</td>
        <td>Vladimir Jara</td>
        <td>Done</td>
    </tr>
    <tr>
        <td rowspan="2">Sprint 1</td>
        <td rowspan="2">US01: Registrar cuenta</td>
        <td>TA08</td>
        <td>#182062308</td>
        <td>UI Registro App Móvil</td>
        <td>Diseñar interfaz de usuario para el registro en la app móvil (React Native)</td>
        <td>8</td>
        <td>Vladimir Jara</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>TA09</td>
        <td>#182062309</td>
        <td>Integración API Registro (App Móvil)</td>
        <td>Conectar el formulario de registro móvil con la API /register</td>
        <td>6</td>
        <td>Juan Ramos</td>
        <td>Done</td>
    </tr>
    <tr>
        <td rowspan="2">Sprint 1</td>
        <td rowspan="2">US03: Iniciar sesión</td>
        <td>TA10</td>
        <td>#182062310</td>
        <td>API de inicio de sesión</td>
        <td>Desarrollar endpoint POST /login con autenticación</td>
        <td>6</td>
        <td>Juan Ramos</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>TA11</td>
        <td>#182062311</td>
        <td>Formulario de inicio de sesión (Frontend)</td>
        <td>Crear componente React para el inicio de sesión</td>
        <td>6</td>
        <td>Williams Góngora</td>
        <td>To Do</td>
    </tr>
    <tr>
        <td rowspan="2">Sprint 1</td>
        <td rowspan="2">US03: Iniciar sesión</td>
        <td>TA12</td>
        <td>#182062312</td>
        <td>UI Inicio de Sesión App Móvil</td>
        <td>Diseñar interfaz de usuario para el inicio de sesión en la app móvil (React Native)</td>
        <td>6</td>
        <td>Vladimir Jara</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>TA13</td>
        <td>#182062313</td>
        <td>Integración API Login (App Móvil)</td>
        <td>Conectar el formulario de inicio de sesión móvil con la API /login</td>
        <td>4</td>
        <td>Vladimir Jara</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>Sprint 1</td>
        <td>US09: Mandar solicitud de cita</td>
        <td>TA06</td>
        <td>#182062306</td>
        <td>Componente calendario</td>
        <td>Implementar selector de fechas básico en React Native</td>
        <td>10</td>
        <td>Quique Vladimir Jara Benites</td>
        <td>In Progress</td>
    </tr>
    <tr>
        <td>Sprint 1</td>
        <td>US09: Mandar solicitud de cita</td>
        <td>TA07</td>
        <td>#182062307</td>
        <td>Integración backend (Citas - Mock o MVP)</td>
        <td>Conectar con API de citas (implementación básica o mock para MVP)</td>
        <td>6</td>
        <td>Oscar Garayar</td>
        <td>To Do</td>
    </tr>
</table>


### 6.2.1.3. Development Evidence for Sprint Review

 <table border="1">
      <tr>
        <th>Repository</th>
        <th>Branch</th>
        <th>Commit Id</th>
        <th>Commit Message</th>
        <th>Commit Message Body</th>
        <th>Committed on</th>
      </tr>
      <tr>
        <td>frontend/landing-page</td>
        <td>feature/header</td>
        <td>a1b2c3d</td>
        <td>feat: main header component</td>
        <td>Added responsive navbar</td>
        <td>2025-05-07</td>
      </tr>
      <tr>
        <td>backend/auth-service</td>
        <td>feature/register</td>
        <td>e4f5g6h</td>
        <td>feat: registration endpoint</td>
        <td>Implemented JWT validation</td>
        <td>2025-05-10</td>
      </tr>
      <tr>
        <td>mobile-app</td>
        <td>feature/calendar</td>
        <td>i7j8k9l</td>
        <td>feat: date picker component</td>
        <td>Added calendar UI with day selection</td>
        <td>2025-05-12</td>
      </tr>
      <tr>
        <td>frontend/landing-page</td>
        <td>develop</td>
        <td>m0n1o2p</td>
        <td>fix: mobile responsiveness</td>
        <td>Adjusted breakpoints for tablets</td>
        <td>2025-05-13</td>
      </tr>
    </table>

### 6.2.1.4. Execution Evidence for Sprint Review

En este primer Sprint del proyecto, hemos logrado implementar y desplegar una Landing Page operativa que comunica la propuesta de valor, dirige a las tiendas de aplicaciones y permite la suscripción por correo electrónico. Adicionalmente, se completó la creación y el despliegue del backend, incluyendo las APIs necesarias para la gestión de usuarios y la autenticación. Finalmente, se desarrolló e implementó la primera versión de nuestra aplicación móvil, permitiendo a los usuarios registrarse e iniciar sesión en la plataforma.

* **Landing Page:**

#### Header

 <img src="https://github.com/user-attachments/assets/91ca2728-48b9-4d08-a8fe-82af82e5d5f7"/>
 
#### Desktop Web Browser

<img src="https://github.com/user-attachments/assets/bbf1b3bc-7ec9-4c73-af17-e22bdce32bc2"/>

 #### Benefits
 <img src="https://github.com/user-attachments/assets/408e9c84-b197-4ad5-84aa-c3cbc1e502d1"/>

 #### The problem
 <img src="https://github.com/user-attachments/assets/173cb90d-e7ca-4e8f-866f-902bb645b985"/>

 #### What our users say
 <img src="https://github.com/user-attachments/assets/ebf0be4f-5531-4d57-a379-836b59a9a741"/>

 #### Download Our App
 <img src="https://github.com/user-attachments/assets/2b116bc0-1f1e-4170-9e69-e4a48545e05a"/>

  #### Footer

  <img src="https://github.com/user-attachments/assets/dbcaf820-268d-40fd-896c-da0eaad6ce1b"/>

<br>

* **Aplicacion Movil:**

#### Pantalla de pacientes

![](https://github.com/user-attachments/assets/3f8cf6f8-49a9-476d-8a92-ebb72a953c65)

#### Pantalla de mensajes

![](https://github.com/user-attachments/assets/7a01ef77-ce5d-4b2a-b900-9e4feb3a4140)

#### Pantalla de chat

![](https://github.com/user-attachments/assets/fe32361d-0e7a-4ebe-94e6-84d3ae9a3506)

#### Pantalla de calendario
![](https://github.com/user-attachments/assets/2882c4a1-47ac-403d-8451-929d4de42eb8)

#### Pantalla de notificaciones
![](https://github.com/user-attachments/assets/0e2e0e4f-2559-420c-a9eb-42aa7d3948fd)

#### Pantalla de solicitudes
![](https://github.com/user-attachments/assets/8606afc0-b30d-4b63-aa6c-3feddaf66547)



### 6.2.1.5. Services Documentation Evidence for Sprint Review

Durante el presente Sprint, se desarrollaron y documentaron diversos endpoints que forman parte de los servicios backend de la aplicación. Estos endpoints permiten la interacción entre el cliente la aplicación.

![Api](https://github.com/user-attachments/assets/9dc5be2b-ce4b-4920-a21b-61ce14b29ef3)

* **Authentication**

![image](https://github.com/user-attachments/assets/3f901c32-255d-4ee8-8bc5-bc0613bd3dc4)

* **Doctors**
  
![image](https://github.com/user-attachments/assets/5ae02994-d80c-4315-84c0-cf5d7589e696)

* **Medicines**
  
![image](https://github.com/user-attachments/assets/0389a48c-0f59-48a2-939d-cf97b04d448b)

* **PatientFollowUp**
  
![image](https://github.com/user-attachments/assets/6b9d4c13-946b-4e2b-801e-fe0d5014bc13)

* **Patients**
  
![image](https://github.com/user-attachments/assets/ee0170c4-438a-49ce-bcc7-de74c74f4e91)

* **Profiles**
  
![image](https://github.com/user-attachments/assets/afe4ed71-3b92-4699-ad5c-0736756956fa)

* **Users**
  
![image](https://github.com/user-attachments/assets/0c21b990-0c01-43ed-8021-f3934ae356f9)


#### 6.2.1.6. Software Deployment Evidence for Sprint Review


##### Secciones implementadas en el Landing Page
Puedes visualizar todas las funcionalidades en el siguiente enlace:  
https://oncontrolupc.github.io/landingprueba/



##### Herramientas de desarrollo utilizadas
- **HTML**: Lenguaje base para estructura web  
  *Evidencia:*  
  `index.html` (archivo principal con integración de todas las secciones)  
  `contact.html` (formulario de contacto funcional)

- **CSS**: Estilos y diseño responsive  
  *Evidencia:*  
  `styles/main.css` (estilos globales)  
  `styles/sections.css` (diseño por componentes)

- **JavaScript**: Interactividad y validaciones  
  *Evidencia:*  
  `js/form-validation.js` (validación de formularios)  
  `js/animations.js` (efectos de scroll)


##### Tecnologías clave para el despliegue
1. **Git**  
   Control de versiones para trabajo colaborativo
2. **GitHub**  
   Plataforma de hosting para repositorio principal
3. **Git Flow**  
   Flujo de trabajo con ramas:  
   - `develop` (integración continua)  
   - `feature/*` (desarrollo por secciones)
4. **GitHub Pages**  
   Servicio de hosting estático para el despliegue final



##### Proceso de despliegue
1. **Configuración del repositorio**  
   - Creación del repo en GitHub: `OnControl-UPC/Landing-Page`
2. **Publicación en GitHub Pages**  
   - Settings → Pages → Branch: `gh-pages` → Folder: `/root`
3. **Integración continua**  
   - Merge de ramas a `main` mediante Pull Requests
4. **Despliegue automático**  
   - Configuración de GitHub Actions para build automático



##### Enlace de despliegue final
▶️ **Landing Page en producción:**  
https://oncontrolupc.github.io/landingprueba/




##### Estructura técnica verificable
```bash
├── index.html          # Página principal
├── styles/
│   ├── main.css        # Estilos globales
│   └── sections.css    # Estilos por sección
├── js/
│   ├── main.js         # Lógica principal
│   └── animations.js   # Efectos visuales
└── assets/             # Multimedia
    ├── images/
    └── videos/

```
### Despliegue del Landing Page

Para el despliegue de nuestro landing page, utilizamos GitHub Pages, una plataforma que nos permite publicar sitios web estáticos directamente desde un repositorio de GitHub. Esto nos facilitó compartir el proyecto en línea de manera gratuita, rápida y sin necesidad de configurar un servidor adicional.

* Estructura del Repositorio

La estructura del repositorio está organizada de forma clara y modular. Incluye carpetas separadas para los estilos (/css), imágenes (/imgs) y scripts (/scripts), así como el archivo principal index.html. Esta organización favorece el mantenimiento del código y la colaboración en equipo.

![image](https://github.com/user-attachments/assets/a1e5ec6d-efe5-4643-974f-48dd911644e2)

* Github Page

Una vez completado el desarrollo, configuramos la rama principal del repositorio para que GitHub Pages sirviera automáticamente el contenido. Esto generó una URL pública desde la cual cualquier usuario puede acceder al sitio web.

![image](https://github.com/user-attachments/assets/b974c55e-1d03-4fca-b18e-a45790073539)

### Despliegue del Backend

##### 1. Creación de aplicación web + base de datos
- **Contenido**: Formulario de configuración de App Service y base de datos.
- **Pasos clave**:
  1. Elegir **Sistema operativo** (Windows/Linux) y **Región** (ej. East US 2).
  2. Configurar **Plan de App Service** con tamaño (SKU) y memoria.
  3. Crear base de datos **MySQL** con opciones como almacenamiento y versión.
  
 <img src="https://github.com/user-attachments/assets/0def481f-dadc-4807-ae38-32384f48182b5"/>

##### 2. Detalles de implementación en curso
- **Contenido**: Nombre de implementación, grupo de recursos y fecha de inicio.
- **Pasos clave**:
  1. Verificar el **Nombre de implementación**: `Microsoft.Web-WebAppDatabase-Portal-i623e2b4-b638`.
  2. Confirmar el **Grupo de recursos asociado**: `orecipital`.
  3. Revisar el estado **"La implementación está en curso"** y logs en **Detalles de la operación**.
     
  <img src="https://github.com/user-attachments/assets/0fd86907-a034-47a6-9a6c-12d0558aac1d"/>

##### 3. Progreso de la implementación
- **Contenido**: Lista de verificación con elementos completados (✓) y pendientes ( ).
- **Pasos clave**:
  1. Configurar **Grupo de recursos** y **Vnet** para la infraestructura.
  2. Habilitar **Microsoft Defender for Cloud** para seguridad.
  3. Definir alertas de costos para evitar sobrecargos.
  4. Enlazar recursos con **Asociación** y **Identificación de implementación**.
  
 <img src="https://github.com/user-attachments/assets/fccdebe8-7c4c-458a-a9dc-94ac30b6f223"/>

##### 4. Configuración de red privada y DNS
- **Contenido**: Lista de recursos de red (VNet, zonas DNS privadas).
- **Pasos clave**:
  1. Vincular **Red virtual (VNet)** con la aplicación.
  2. Crear **Zonas DNS privadas** para servicios como MySQL (`privatelink.mysql.database.azure.com`).
  3. Establecer **Vínculos de red virtual** para acceso seguro a recursos.
     
 <img src="https://github.com/user-attachments/assets/8ad2d4b5-3017-41a4-a76a-f94aa9fb448d"/>

##### 5. Configuración de variables de entorno y conexión a MySQL
- **Contexto**: Sección de **Environment variables** en Azure App Service.
- **Pasos clave**:
  1. **Agregar variables de entorno**:
     - Nombre: `ADJAE_UHTML_CONNECTIONSTRING`.
     - Valor: Cadena de conexión a la base de datos MySQL (`Server=mi-servidor.mysql.database.stan.com;Database=oncontrol-database`).
  2. **Configurar tipo y origen**:
     - **Type**: MySQL (indica el motor de base de datos).
     - **Source**: App Service (origen de la configuración).
  3. **Acciones adicionales**:
     - Opciones para edición avanzada o referencia completa de valores
       
 <img src="https://github.com/user-attachments/assets/0133e82c-857d-4675-ab72-31a6e1a07791"/>

 ##### 6. Configuración de GitHub Actions para CI/CD
- **Contexto**: Integración de Azure con GitHub Actions en **Deployment Center**.
- **Pasos clave**:
  1. **Vincular repositorio de GitHub**:
     - **Organization**: `OnControlUPC`.
     - **Repository**: `oncontrol-platform`.
     - **Branch**: `main`.
  2. **Definir workflow**:
     - Crear un nuevo archivo YAML (`main_oncontrol.yml`) o usar uno existente.
     - **Runtime stack**: .NET 8.0 (entorno de ejecución).
  3. **Autenticación**:
     - Elegir entre:
       - **User-assigned identity**: Federación con Azure AD para permisos automatizados.
       - **Basic authentication**: Credenciales manuales (menos seguro).
     - **Suscripción asociada**: `Azure for Students`.
  4. **Advertencias**:
     - Evitar configurar CI/CD directamente en el **production slot** (no recomendado).
     - Requiere permisos de escritura en el repositorio de GitHub.

<img src="https://github.com/user-attachments/assets/c603dc47-5146-41b6-8f77-7f30868e4a65"/>

##### 7. Deployment Center y flujo de GitHub Actions
- **Contexto**: Configuración de automatización de despliegues en **Deployment Center**.
- **Pasos clave**:
  1. **Seleccionar origen**:
     - Proveedor: **GitHub**.
     - **Building with GitHub Actions**: Automatiza builds y despliegues.
  2. **Detalles del workflow**:
     - **Trigger**: Se activa con commits en la rama `main`.
     - **Permisos**: Habilitar permisos adicionales en GitHub si es necesario.
  3. **Configuración de seguridad**:
     - **Microsoft Defender for Cloud**: Protege la infraestructura.
     - **Alertas**: Monitorear eventos y costos.
  4. **Advertencias clave**:
     - **No usar el slot de producción para CI/CD**: Usar slots de staging para pruebas.
     - **Validar archivo YAML**: Asegurar que el workflow no tenga errores de sintaxis.
    
<img src="https://github.com/user-attachments/assets/82ec9c77-539f-4e09-9278-05440a8c6fba"/>

##### 8. Resultado de implementación exitosa
- **Contenido**: Logs de ejecución y advertencias.
- **Pasos clave**:
  1. Verificar **Estado: Success** y duración (`20s`).
  2. Revisar **Annotations** para resolver errores (ej: propiedades no nulas en código).
  3. Acceder a enlaces de logs (`http://executor.buildbrackleapp.eu/index`).

<img src="https://github.com/user-attachments/assets/bc945708-86ea-42f5-8d2a-c88c24030044"/>
 
#### 6.2.1.7. Team Collaboration Insights during Sprint

Se proporcionará información detallada sobre la colaboración y comunicación entre los miembros del equipo de desarrollo durante el sprint. Esto incluirá la coordinación de actividades, la gestión de tareas asignadas y la resolución de inconvenientes surgidos en el proceso. Las responsabilidades se distribuyeron equitativamente entre los integrantes del equipo. 

![image](https://github.com/user-attachments/assets/d395fe20-1590-4fe0-b113-e980cabad875)

![image](https://github.com/user-attachments/assets/787368a5-9062-4133-993e-36e0f1578a81)

![image](https://github.com/user-attachments/assets/21012ebd-cd4d-40d8-b492-1207f410e2c2)

### 6.2.2. Sprint 2

En esta sección se expone el avance correspondiente al Sprint 2, planificando el desarrollo de las funcionalidades core del sistema OnControl, enfocándose en la implementación completa del módulo de médicos y las correcciones identificadas en la primera entrega, junto con la funcionalidad básica de autenticación para pacientes.

### 6.2.2.1. Sprint Planning 2


| **Campo** | **Detalle** |
|-----------|-------------|
| **Sprint** | Sprint 2 |
| **Sprint Planning Date** | 2025-06-18 |
| **Time** | 03:00 PM |
| **Location** | Meet |
| **Prepared By** | Quique Vladimir Jara Benites |
| **Attendees** | Williams Góngora / Oscar Garayar / Juan Ramos / Michael Quispe / Williams Góngora |
| **Sprint Goal** | Implementar funcionalidades completas del módulo médico, login de pacientes y correcciones del Sprint 1 para la aplicación móvil OnControl. |
| **Sprint Velocity** | 7 |
| **Sum of Story Points** | 25 |



### 6.2.2.2. Sprint Backlog 2

| User Story | Work-Item / Task Id | ID | Title | Description | Estimation (Hours) | Assigned To | Status
|-----|-----|-----|-----|-----|-----|-----|-----
| US03 | WI-001 | SB2-001 | Implementar login de paciente | Desarrollar pantalla de login para pacientes con validación de credenciales | 8 | TBD | To-do
| US03 | WI-002 | SB2-002 | Integrar autenticación backend paciente | Conectar frontend de login con API de autenticación | 6 | TBD | To-do
| US04 | WI-003 | SB2-003 | Implementar logout de paciente | Desarrollar funcionalidad de cierre de sesión para pacientes | 4 | TBD | To-do
| US01 | WI-004 | SB2-004 | Registro completo de doctor | Implementar formulario de registro para médicos con validaciones | 12 | TBD | To-do
| US03 | WI-005 | SB2-005 | Login completo de doctor | Desarrollar sistema de autenticación completo para médicos | 8 | TBD | To-do
| US04 | WI-006 | SB2-006 | Logout de doctor | Implementar cierre de sesión para médicos | 4 | TBD | To-do
| US05 | WI-007 | SB2-007 | Recuperación de cuenta doctor | Desarrollar sistema de recuperación por email y SMS para médicos | 10 | TBD | To-do
| US06 | WI-008 | SB2-008 | Cambio de teléfono doctor | Implementar actualización de número telefónico para médicos | 6 | TBD | To-do
| US07 | WI-009 | SB2-009 | Cambio de contraseña doctor | Desarrollar funcionalidad de cambio de contraseña para médicos | 6 | TBD | To-do
| US08 | WI-010 | SB2-010 | Actualizar foto perfil doctor | Implementar subida y actualización de foto de perfil para médicos | 8 | TBD | To-do
| US09 | WI-011 | SB2-011 | Solicitud de cita por doctor | Desarrollar formulario para que médicos envíen solicitudes de cita | 10 | TBD | To-do
| US13 | WI-012 | SB2-012 | Solicitud de tratamiento | Implementar formulario para médicos envíen solicitudes de tratamiento | 12 | TBD | To-do
| US17 | WI-013 | SB2-013 | Asignar especialista | Desarrollar funcionalidad para que médicos asignen especialistas | 8 | TBD | To-do
| US19 | WI-014 | SB2-014 | Revisar síntomas reportados | Implementar panel para que médicos revisen síntomas de pacientes | 10 | TBD | To-do
| US22 | WI-015 | SB2-015 | Notificación fin de tratamiento | Desarrollar sistema de notificaciones para médicos sobre fin de tratamiento | 8 | TBD | To-do
| US25 | WI-016 | SB2-016 | Agregar paciente por username | Implementar funcionalidad para médicos inviten pacientes por usuario | 10 | TBD | To-do
| US26 | WI-017 | SB2-017 | Crear procedimiento médico | Desarrollar formulario para médicos creen procedimientos médicos | 12 | TBD | To-do
| US28 | WI-018 | SB2-018 | Configurar procedimiento | Implementar ajustes de duración y frecuencia de procedimientos | 8 | TBD | To-do
| US32 | WI-019 | SB2-019 | Eliminar paciente | Desarrollar funcionalidad para médicos eliminen pacientes finalizados | 6 | TBD | To-do
| US34 | WI-020 | SB2-020 | Lista de pacientes | Implementar vista de lista de pacientes para médicos | 10 | TBD | To-do
| US35 | WI-021 | SB2-021 | Historial de tratamientos | Desarrollar vista de historial cronológico de tratamientos | 12 | TBD | To-do
| US30 | WI-022 | SB2-022 | Configurar recordatorios doctor | Implementar personalización de notificaciones para médicos | 8 | TBD | To-do
| US31 | WI-023 | SB2-023 | Avisos de cambios sistema doctor | Desarrollar sistema de notificaciones de cambios para médicos | 10 | TBD | To-do
| US33 | WI-024 | SB2-024 | Contactar soporte doctor | Implementar formulario de contacto con soporte para médicos | 6 | TBD | To-do
| US02 | WI-025 | SB2-025 | Configurar pagos doctor | Desarrollar sistema de configuración de métodos de pago para médicos | 10 | TBD | To-do


**Total Estimation: 212 hours**

**Sprint Goals:**

- Completar funcionalidad básica de login para pacientes
- Implementar todas las funcionalidades core para médicos (excepto chat)
- Establecer base sólida para gestión de tratamientos y procedimientos
- Corregir issues identificados en Sprint 1


**Notes:**

- Las tareas están priorizadas por dependencias técnicas
- Se excluyen funcionalidades de chat (US23, US24) según especificaciones
- Se incluye solo login básico para pacientes, no funcionalidades completas
- Estimaciones basadas en complejidad técnica y correcciones del Sprint 1

### 6.2.2.3. Development Evidence for Sprint Review

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on
|-----|-----|-----|-----|-----|-----
| OnControlUPC/OnControl-flutter | main | 515cd95 | profile tab added in home, plus logout | Added profile navigation tab to home screen and implemented logout functionality for user session management | Jun 18, 2025
| OnControlUPC/OnControl-flutter | main | b235434 | feat: auth finished, and profile too | Completed authentication system implementation and finalized user profile management features | Jun 18, 2025
| OnControlUPC/OnControl-flutter | main | 33ea435 | feat: auth almost finished | Authentication flow nearly complete, pending final validations and error handling | Jun 17, 2025
| OnControlUPC/OnControl-flutter | main | f79c791 | feat: auth almost finished | Continued work on authentication system, implemented login/register forms and validation | Jun 17, 2025
| OnControlUPC/OnControl-flutter | main | c71c9ca | feat: auth almost finished | Authentication services and UI components development in progress | Jun 17, 2025
| OnControlUPC/OnControl-flutter | main | 4bd5192 | feat: creacion de la rama auth | Created authentication branch and set up initial structure for user authentication features | Jun 14, 2025
| OnControlUPC/OnControl-flutter | main | c74cd9a | the project is created | Initial Flutter project setup with basic structure and dependencies configuration | Jun 13, 2025

### 6.2.2.4. Execution Evidence for Sprint Review

En este segundo sprint se realizo la aplicacion movil en kotlin y flutter. La aplicacion en kotlin esta casi culminada, agregamos y completamos las vistas como chat, calendario, etc. En el caso de flutter hemos hecho lo basico es decir el inicio de sesion, ingreso y registro del usuario, y la vista basica del home.

* **Aplicacion movil kotlin:**
  

* **Aplicacion movil flutter:**

#### Pantalla de inicio de sesion 

![](https://github.com/user-attachments/assets/9a5db1bb-a71b-4da4-8d4a-4eb584333e5e)

#### Pantalla de creacion de cuenta

![](https://github.com/user-attachments/assets/31775220-5eb4-456a-95c1-cc59633c0ca9)

#### Pantalla de creacion de perfil

![](https://github.com/user-attachments/assets/b7fcb221-19c7-4757-93f5-35562f80fd09)

#### Pantalla de home

![](https://github.com/user-attachments/assets/4548c3e1-76a5-4c29-9cd8-949145e4e385)


### 6.2.2.5. Services Documentation Evidence for Sprint Review

Durante el presente Sprint, se desarrollaron, mejoraron y documentaron diversos endpoints que forman parte de los servicios backend de la aplicación. Estos endpoints permiten la interacción entre el cliente y la aplicación.

* **Authentication**

![image](https://github.com/user-attachments/assets/3f901c32-255d-4ee8-8bc5-bc0613bd3dc4)

* **Doctors**
  
![image](https://github.com/user-attachments/assets/5ae02994-d80c-4315-84c0-cf5d7589e696)

* **Medicines**
  
![image](https://github.com/user-attachments/assets/0389a48c-0f59-48a2-939d-cf97b04d448b)

* **PatientFollowUp**
  
![image](https://github.com/user-attachments/assets/6b9d4c13-946b-4e2b-801e-fe0d5014bc13)

* **Patients**
  
![image](https://github.com/user-attachments/assets/ee0170c4-438a-49ce-bcc7-de74c74f4e91)

* **Profiles**
  
![image](https://github.com/user-attachments/assets/afe4ed71-3b92-4699-ad5c-0736756956fa)

* **Users**
  
![image](https://github.com/user-attachments/assets/0c21b990-0c01-43ed-8021-f3934ae356f9)

### 6.2.2.6. Software Deployment Evidence for Sprint Review

### Despliegue del Backend

##### 1. Creación de aplicación web + base de datos
- **Contenido**: Formulario de configuración de App Service y base de datos.
- **Pasos clave**:
  1. Elegir **Sistema operativo** (Windows/Linux) y **Región** (ej. East US 2).
  2. Configurar **Plan de App Service** con tamaño (SKU) y memoria.
  3. Crear base de datos **MySQL** con opciones como almacenamiento y versión.
  
 <img src="https://github.com/user-attachments/assets/0def481f-dadc-4807-ae38-32384f48182b5"/>

##### 2. Detalles de implementación en curso
- **Contenido**: Nombre de implementación, grupo de recursos y fecha de inicio.
- **Pasos clave**:
  1. Verificar el **Nombre de implementación**: `Microsoft.Web-WebAppDatabase-Portal-i623e2b4-b638`.
  2. Confirmar el **Grupo de recursos asociado**: `orecipital`.
  3. Revisar el estado **"La implementación está en curso"** y logs en **Detalles de la operación**.
     
  <img src="https://github.com/user-attachments/assets/0fd86907-a034-47a6-9a6c-12d0558aac1d"/>

##### 3. Progreso de la implementación
- **Contenido**: Lista de verificación con elementos completados (✓) y pendientes ( ).
- **Pasos clave**:
  1. Configurar **Grupo de recursos** y **Vnet** para la infraestructura.
  2. Habilitar **Microsoft Defender for Cloud** para seguridad.
  3. Definir alertas de costos para evitar sobrecargos.
  4. Enlazar recursos con **Asociación** y **Identificación de implementación**.
  
 <img src="https://github.com/user-attachments/assets/fccdebe8-7c4c-458a-a9dc-94ac30b6f223"/>

##### 4. Configuración de red privada y DNS
- **Contenido**: Lista de recursos de red (VNet, zonas DNS privadas).
- **Pasos clave**:
  1. Vincular **Red virtual (VNet)** con la aplicación.
  2. Crear **Zonas DNS privadas** para servicios como MySQL (`privatelink.mysql.database.azure.com`).
  3. Establecer **Vínculos de red virtual** para acceso seguro a recursos.
     
 <img src="https://github.com/user-attachments/assets/8ad2d4b5-3017-41a4-a76a-f94aa9fb448d"/>

##### 5. Configuración de variables de entorno y conexión a MySQL
- **Contexto**: Sección de **Environment variables** en Azure App Service.
- **Pasos clave**:
  1. **Agregar variables de entorno**:
     - Nombre: `ADJAE_UHTML_CONNECTIONSTRING`.
     - Valor: Cadena de conexión a la base de datos MySQL (`Server=mi-servidor.mysql.database.stan.com;Database=oncontrol-database`).
  2. **Configurar tipo y origen**:
     - **Type**: MySQL (indica el motor de base de datos).
     - **Source**: App Service (origen de la configuración).
  3. **Acciones adicionales**:
     - Opciones para edición avanzada o referencia completa de valores
       
 <img src="https://github.com/user-attachments/assets/0133e82c-857d-4675-ab72-31a6e1a07791"/>

 ##### 6. Configuración de GitHub Actions para CI/CD
- **Contexto**: Integración de Azure con GitHub Actions en **Deployment Center**.
- **Pasos clave**:
  1. **Vincular repositorio de GitHub**:
     - **Organization**: `OnControlUPC`.
     - **Repository**: `oncontrol-platform`.
     - **Branch**: `main`.
  2. **Definir workflow**:
     - Crear un nuevo archivo YAML (`main_oncontrol.yml`) o usar uno existente.
     - **Runtime stack**: .NET 8.0 (entorno de ejecución).
  3. **Autenticación**:
     - Elegir entre:
       - **User-assigned identity**: Federación con Azure AD para permisos automatizados.
       - **Basic authentication**: Credenciales manuales (menos seguro).
     - **Suscripción asociada**: `Azure for Students`.
  4. **Advertencias**:
     - Evitar configurar CI/CD directamente en el **production slot** (no recomendado).
     - Requiere permisos de escritura en el repositorio de GitHub.

<img src="https://github.com/user-attachments/assets/c603dc47-5146-41b6-8f77-7f30868e4a65"/>

##### 7. Deployment Center y flujo de GitHub Actions
- **Contexto**: Configuración de automatización de despliegues en **Deployment Center**.
- **Pasos clave**:
  1. **Seleccionar origen**:
     - Proveedor: **GitHub**.
     - **Building with GitHub Actions**: Automatiza builds y despliegues.
  2. **Detalles del workflow**:
     - **Trigger**: Se activa con commits en la rama `main`.
     - **Permisos**: Habilitar permisos adicionales en GitHub si es necesario.
  3. **Configuración de seguridad**:
     - **Microsoft Defender for Cloud**: Protege la infraestructura.
     - **Alertas**: Monitorear eventos y costos.
  4. **Advertencias clave**:
     - **No usar el slot de producción para CI/CD**: Usar slots de staging para pruebas.
     - **Validar archivo YAML**: Asegurar que el workflow no tenga errores de sintaxis.
    
<img src="https://github.com/user-attachments/assets/82ec9c77-539f-4e09-9278-05440a8c6fba"/>

##### 8. Resultado de implementación exitosa
- **Contenido**: Logs de ejecución y advertencias.
- **Pasos clave**:
  1. Verificar **Estado: Success** y duración (`20s`).
  2. Revisar **Annotations** para resolver errores (ej: propiedades no nulas en código).
  3. Acceder a enlaces de logs (`http://executor.buildbrackleapp.eu/index`).

<img src="https://github.com/user-attachments/assets/bc945708-86ea-42f5-8d2a-c88c24030044"/>
 
### 6.2.2.7. Team Collaboration Insights during Sprint

Se proporcionará información detallada sobre la colaboración y comunicación entre los miembros del equipo de desarrollo durante el sprint. Esto incluirá la coordinación de actividades, la gestión de tareas asignadas y la resolución de inconvenientes surgidos en el proceso. Las responsabilidades se distribuyeron equitativamente entre los integrantes del equipo. 

![image](https://github.com/user-attachments/assets/d395fe20-1590-4fe0-b113-e980cabad875)

![image](https://github.com/user-attachments/assets/787368a5-9062-4133-993e-36e0f1578a81)

![image](https://github.com/user-attachments/assets/21012ebd-cd4d-40d8-b492-1207f410e2c2)

### 6.2.3. Sprint 3

En esta sección se presenta el avance correspondiente al Sprint 3, centrado en el desarrollo integral de las funcionalidades clave del sistema OnControl. Durante este ciclo, se priorizó:

* La culminación del módulo de médicos, incluyendo mejoras y ajustes identificados en entregas anteriores.

* La implementación completa de las funcionalidades para la aplicación de pacientes, garantizando su operatividad y conexión efectiva con los médicos.

* El fortalecimiento del vínculo entre ambas aplicaciones (Flutter y Android), mediante el intercambio de datos clínicos, solicitudes y notificaciones.

Este sprint representa un hito importante en la consolidación de la arquitectura funcional del sistema, sentando las bases para próximas funcionalidades como mensajería, seguimiento de tratamientos y mejoras UX.

### 6.2.3.1. Sprint Planning 3

| **Campo** | **Detalle** |
|-----------|-------------|
| **Sprint** | Sprint 3 |
| **Sprint Planning Date** | 2025-07-02 |
| **Time** | 03:00 PM |
| **Location** | Meet |
| **Prepared By** | Quique Vladimir Jara Benites |
| **Attendees** | Williams Góngora / Oscar Garayar / Juan Ramos / Michael Quispe / Quique Vladimir Jara |
| **Sprint Goal** | Completar todas las funcionalidades del módulo de pacientes e integrarlo con el módulo médico. Este sprint marca la consolidación total de la plataforma OnControl en términos de autenticación, gestión de tratamientos, citas y notificaciones. |
| **Sprint Velocity** | 7 |
| **Sum of Story Points** | 34 |

### 6.2.3.2. Sprint Backlog 3

| User Story | Work-Item / Task Id | ID | Title | Description | Estimation (Hours) | Assigned To | Status |
|------------|---------------------|-----|--------|-------------|--------------------|--------------|--------|
| US01 | WI-026 | SB3-001 | Registro de usuario (Flutter) | Desarrollar formulario de registro para pacientes con validaciones y conexión a API | 10 | TBD | To-do |
| US07 | WI-030 | SB3-005 | Cambio de contraseña paciente | Agregar vista y lógica para actualización de contraseña con validaciones | 6 | TBD | To-do |
| US08 | WI-031 | SB3-006 | Actualizar foto de perfil paciente | Permitir a pacientes subir, previsualizar y guardar una imagen de perfil | 6 | TBD | To-do |
| US10 | WI-032 | SB3-007 | Aceptar cita | Desarrollar funcionalidad para que pacientes confirmen citas propuestas | 6 | TBD | To-do |
| US11 | WI-033 | SB3-008 | Cancelar cita | Permitir cancelación de citas activas con notificación al médico responsable | 6 | TBD | To-do |
| US12 | WI-034 | SB3-009 | Reprogramar cita | Implementar lógica de cambio de fecha para citas y notificación automática | 8 | TBD | To-do |
| US14 | WI-035 | SB3-010 | Responder cambios en tratamiento | Integrar opción para aceptar o rechazar modificaciones propuestas | 6 | TBD | To-do |
| US15 | WI-036 | SB3-011 | Personalizar fecha de inicio | Añadir selector para definir inicio de tratamiento según disponibilidad | 4 | TBD | To-do |
| US16 | WI-037 | SB3-012 | Marcar cumplimiento diario | Permitir seguimiento de cumplimiento por parte del paciente | 6 | TBD | To-do |
| US36 | WI-041 | SB3-016 | Ver procedimientos del día | Mostrar lista diaria de procedimientos activos asignados al paciente | 6 | TBD | To-do |
| US21 | WI-042 | SB3-017 | Notificaciones de cambio tratamiento | Mostrar alertas cuando se propongan cambios en el plan terapéutico | 6 | TBD | To-do |
| US20 | WI-043 | SB3-018 | Consultar medicamentos | Visualizar detalles de medicamentos activos, dosis y advertencias | 6 | TBD | To-do |
| US30 | WI-044 | SB3-019 | Configurar recordatorios paciente | Permitir personalización de notificaciones, tono y horario | 6 | TBD | To-do |
| US31 | WI-045 | SB3-020 | Avisos de cambios sistema paciente | Notificar a pacientes sobre reprogramaciones, nuevas versiones u otras actualizaciones | 6 | TBD | To-do |

**Total Estimation: 136 hours**


**Sprint Goals**

- Finalizar todas las funcionalidades del módulo de pacientes: autenticación, perfil, citas, tratamiento y configuración.
- Integrar completamente el módulo de pacientes con el módulo de médicos mediante flujos de comunicación y notificaciones.
- Consolidar la plataforma OnControl como sistema funcional y estable para ambas aplicaciones móviles.

### 6.2.3.3. Development Evidence for Sprint Review

* **OnControlUPC/OnControlDoctor**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on |
|------------|--------|-----------|----------------|----------------------|---------------|
| OnControlUPC/OnControlDoctor | master | fae3850 | Merge pull request #7 from OnControlUPC/develop | Integración de funcionalidades desde rama `develop` hacia `master`, consolidando avances para entrega final | Jul 7, 2025 |
| OnControlUPC/OnControlDoctor | master | 00e1751 | Merge pull request #6 from OnControlUPC/feature/home | Incorporación de interfaz principal (`home`) al proyecto de doctores con navegación y vista base | Jul 7, 2025 |
| OnControlUPC/OnControlDoctor | master | d70e8cd | feat: get history messages | Implementada función para recuperar historial de mensajes en contexto de comunicación clínica | Jul 7, 2025 |
| OnControlUPC/OnControlDoctor | master | 3abab4b3 | feat: add communication context | Añadido componente de contexto para manejar sesiones y flujos de comunicación entre doctor y paciente | Jul 5, 2025 |
| OnControlUPC/OnControlDoctor | master | 8619718 | Merge pull request #5 from OnControlUPC/develop | Consolidación de desarrollos previos al entorno `master` | Jul 5, 2025 |
| OnControlUPC/OnControlDoctor | master | a3a0216 | Merge pull request #4 from OnControlUPC/feature/home | Incorporación de vista inicial y navegación principal desde rama `feature/home` | Jul 5, 2025 |
| OnControlUPC/OnControlDoctor | master | ed15cb3 | feat: add communication context | Configuración inicial del contexto compartido para flujos de interacción en tiempo real | Jul 3, 2025 |

* **OnControlUPC/OnControl-flutter**

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on |
|------------|--------|-----------|----------------|----------------------|---------------|
| OnControlUPC/OnControl-flutter | main | b25f591 | calendar hot fixed | Ajuste crítico en la visualización y lógica del calendario de procedimientos y citas | Jul 6, 2025 |
| OnControlUPC/OnControl-flutter | main | ab96979 | appointments fixed | Corrección de flujo de asignación y visualización de citas agendadas | Jul 6, 2025 |
| OnControlUPC/OnControl-flutter | main | 098cda7 | procedures finished | Finalización de implementación de procedimientos asignados al paciente | Jul 6, 2025 |
| OnControlUPC/OnControl-flutter | main | db26d38 | the upload photo is created | Se habilita funcionalidad para subir y actualizar imagen de perfil | Jul 5, 2025 |
| OnControlUPC/OnControl-flutter | main | 8c8923d | Symptoms added | Registro de síntomas habilitado desde la aplicación del paciente | Jul 3, 2025 |
| OnControlUPC/OnControl-flutter | main | ec66c7f | logicas de varias secciones arreglada, chat tmb | Arreglos generales en navegación, validación de formularios y módulo de mensajería | Jul 1, 2025 |
| OnControlUPC/OnControl-flutter | main | 75d930e | feat: update design of calendar_page.dart | Rediseño visual del calendario con mejoras de UX | Jul 1, 2025 |
| OnControlUPC/OnControl-flutter | main | b8b4f6d | feat: update design of treatments_list_page.dart | Estética y estructura mejoradas para la vista de tratamientos del paciente | Jul 1, 2025 |

### 6.2.3.4. Execution Evidence for Sprint Review

Durante el tercer sprint se finalizó la implementación funcional de ambas aplicaciones móviles: una desarrollada en Kotlin para médicos y la otra en Flutter para pacientes, consolidando así la plataforma OnControl en su versión completa.

* En la aplicación de médicos (Kotlin), se concluyó el desarrollo e integración de componentes clave como el historial de mensajes, el contexto de comunicación, el calendario clínico y la navegación principal. Estos avances permiten una interacción fluida con pacientes y una gestión eficiente de citas, tratamientos y seguimiento clínico.

* En la aplicación de pacientes (Flutter), se completaron todas las funcionalidades esenciales: autenticación, registro, actualización de perfil, gestión de citas, notificaciones, visualización de tratamientos y procedimientos diarios, así como el envío de síntomas y configuración de recordatorios. Además, se mejoró la interfaz del calendario y se integraron los módulos de mensajería y seguimiento.

* **Aplicacion movil kotlin:**
  

* **Aplicacion movil flutter:**

#### Pantalla de inicio de sesion 

![](https://github.com/user-attachments/assets/9a5db1bb-a71b-4da4-8d4a-4eb584333e5e)

#### Pantalla de creacion de cuenta

![](https://github.com/user-attachments/assets/31775220-5eb4-456a-95c1-cc59633c0ca9)

#### Pantalla de creacion de perfil

![](https://github.com/user-attachments/assets/b7fcb221-19c7-4757-93f5-35562f80fd09)

#### Pantalla de home

![](https://github.com/user-attachments/assets/4548c3e1-76a5-4c29-9cd8-949145e4e385)


### 6.2.2.5. Services Documentation Evidence for Sprint Review

Durante el Sprint 3 se consolidó y mejoró la documentación de todos los servicios backend del sistema OnControl, utilizando OpenAPI Specification (OAS 3.1) como estándar para garantizar claridad, interoperabilidad y trazabilidad entre equipos. La documentación está disponible a través del endpoint:

Servidor de despliegue
* URL activa: https://oncontrolbackend-gtbdhpc9fgd2epdx.westus3-01.azurewebsites.net

* Entorno: Producción (Azure App Service, región West US 3)

<img width="1264" alt="image" src="https://github.com/user-attachments/assets/0a49d7a2-d9e3-4f5c-9302-4d431aa64c70" />

* Authentication: Gestiona el registro e inicio de sesión de usuarios, asegurando acceso seguro mediante endpoints de autenticación.

* User Management: Permite obtener la lista y detalles de usuarios registrados, facilitando su administración en el sistema.

* Patient & Doctor Profiles: Administra la información de perfil de pacientes y médicos, incluyendo edición, búsqueda y desactivación.

* Doctor-Patient Link: Controla la relación entre médicos y pacientes mediante solicitudes, activación, rechazo y consultas de estado.

* Treatment & Procedures: Maneja la creación, edición y seguimiento de tratamientos y procedimientos médicos asignados.

* Procedure Executions: Permite registrar y consultar la ejecución de procedimientos diarios por parte de pacientes o médicos.

* Appointments: Controla la creación, consulta, cancelación y seguimiento de citas agendadas entre médicos y pacientes.

* Symptoms & Logs: Registra síntomas reportados por pacientes y su visualización para seguimiento clínico.

* Messaging (Chat): Expone el historial conversacional entre paciente y doctor en sesiones clínicas o de tratamiento.

* Subscriptions & Payments: Administra planes, suscripciones, claves de activación, pagos, métodos de pago y su historial.

* Storage: Facilita la subida segura de archivos e imágenes mediante generación de URLs prefirmadas.

* Plans: Permite crear y modificar planes de suscripción que definen acceso y niveles de servicio para los usuarios.

**Evidencias**

* **Authentication**

<img width="910" alt="image" src="https://github.com/user-attachments/assets/8a8bc751-173d-4ea9-aebb-5b3966012148" />

* **Root**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/e11841f3-64d0-4b2b-812e-37a7fd0865cd" />

* **Users**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/9980e006-e6f2-410f-ad0c-63d357f59f0f" />

* **treatment-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a310d7cc-b404-4d6b-bf62-d127cf357f2d" />

* **subscription-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/39c5ab80-ec74-4457-a67d-d453394a5aea" />

* **subscription-key-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/7a5257ca-de25-4fbd-8efa-36039f9f14f9" />

* **storage-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/411f23ad-acfc-4bad-8190-894e00a76fb3" />

* **plan-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a81b9b85-359d-451b-a7fc-483e87bd0b89" />

* **payment-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/f92f9c34-ade4-493a-b2d9-9d5118a5e3b3" />

* **payment-method-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/4e9ec8f0-95f5-4e2a-95db-6b3aff2f1bce" />

* **patient-profile-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/4e8f9680-81cc-490b-ac5a-bcd50f65851a" />

* **doctor-profile-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/291ad3d6-01af-4319-afd0-b6de16388b31" />

* **doctor-patient-link-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/01f843f5-f892-451c-9669-313ffa85aa42" />

* **appointment-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a344ba80-bb23-422d-82d6-21876f2040cf" />

* **procedure-execution-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/d1ce3b2f-bec6-4077-b3c4-019b81cad82b" />

* **chat-message-query-controller**
  
<img width="910" alt="image" src="https://github.com/user-attachments/assets/6cce2dbb-179f-44dc-b7e9-e3487f2008ad" />

### 6.2.2.6. Software Deployment Evidence for Sprint Review

### Despliegue del Backend

##### 1. Creación de aplicación web + base de datos
- **Contenido**: Formulario de configuración de App Service y base de datos.
- **Pasos clave**:
  1. Elegir **Sistema operativo** (Windows/Linux) y **Región** (ej. East US 2).
  2. Configurar **Plan de App Service** con tamaño (SKU) y memoria.
  3. Crear base de datos **MySQL** con opciones como almacenamiento y versión.
  
 <img src="https://github.com/user-attachments/assets/0def481f-dadc-4807-ae38-32384f48182b5"/>

##### 2. Detalles de implementación en curso
- **Contenido**: Nombre de implementación, grupo de recursos y fecha de inicio.
- **Pasos clave**:
  1. Verificar el **Nombre de implementación**: `Microsoft.Web-WebAppDatabase-Portal-i623e2b4-b638`.
  2. Confirmar el **Grupo de recursos asociado**: `orecipital`.
  3. Revisar el estado **"La implementación está en curso"** y logs en **Detalles de la operación**.
     
  <img src="https://github.com/user-attachments/assets/0fd86907-a034-47a6-9a6c-12d0558aac1d"/>

##### 3. Progreso de la implementación
- **Contenido**: Lista de verificación con elementos completados (✓) y pendientes ( ).
- **Pasos clave**:
  1. Configurar **Grupo de recursos** y **Vnet** para la infraestructura.
  2. Habilitar **Microsoft Defender for Cloud** para seguridad.
  3. Definir alertas de costos para evitar sobrecargos.
  4. Enlazar recursos con **Asociación** y **Identificación de implementación**.
  
 <img src="https://github.com/user-attachments/assets/fccdebe8-7c4c-458a-a9dc-94ac30b6f223"/>

##### 4. Configuración de red privada y DNS
- **Contenido**: Lista de recursos de red (VNet, zonas DNS privadas).
- **Pasos clave**:
  1. Vincular **Red virtual (VNet)** con la aplicación.
  2. Crear **Zonas DNS privadas** para servicios como MySQL (`privatelink.mysql.database.azure.com`).
  3. Establecer **Vínculos de red virtual** para acceso seguro a recursos.
     
 <img src="https://github.com/user-attachments/assets/8ad2d4b5-3017-41a4-a76a-f94aa9fb448d"/>

##### 5. Configuración de variables de entorno y conexión a MySQL
- **Contexto**: Sección de **Environment variables** en Azure App Service.
- **Pasos clave**:
  1. **Agregar variables de entorno**:
     - Nombre: `ADJAE_UHTML_CONNECTIONSTRING`.
     - Valor: Cadena de conexión a la base de datos MySQL (`Server=mi-servidor.mysql.database.stan.com;Database=oncontrol-database`).
  2. **Configurar tipo y origen**:
     - **Type**: MySQL (indica el motor de base de datos).
     - **Source**: App Service (origen de la configuración).
  3. **Acciones adicionales**:
     - Opciones para edición avanzada o referencia completa de valores
       
 <img src="https://github.com/user-attachments/assets/0133e82c-857d-4675-ab72-31a6e1a07791"/>

 ##### 6. Configuración de GitHub Actions para CI/CD
- **Contexto**: Integración de Azure con GitHub Actions en **Deployment Center**.
- **Pasos clave**:
  1. **Vincular repositorio de GitHub**:
     - **Organization**: `OnControlUPC`.
     - **Repository**: `oncontrol-platform`.
     - **Branch**: `main`.
  2. **Definir workflow**:
     - Crear un nuevo archivo YAML (`main_oncontrol.yml`) o usar uno existente.
     - **Runtime stack**: .NET 8.0 (entorno de ejecución).
  3. **Autenticación**:
     - Elegir entre:
       - **User-assigned identity**: Federación con Azure AD para permisos automatizados.
       - **Basic authentication**: Credenciales manuales (menos seguro).
     - **Suscripción asociada**: `Azure for Students`.
  4. **Advertencias**:
     - Evitar configurar CI/CD directamente en el **production slot** (no recomendado).
     - Requiere permisos de escritura en el repositorio de GitHub.

<img src="https://github.com/user-attachments/assets/c603dc47-5146-41b6-8f77-7f30868e4a65"/>

##### 7. Deployment Center y flujo de GitHub Actions
- **Contexto**: Configuración de automatización de despliegues en **Deployment Center**.
- **Pasos clave**:
  1. **Seleccionar origen**:
     - Proveedor: **GitHub**.
     - **Building with GitHub Actions**: Automatiza builds y despliegues.
  2. **Detalles del workflow**:
     - **Trigger**: Se activa con commits en la rama `main`.
     - **Permisos**: Habilitar permisos adicionales en GitHub si es necesario.
  3. **Configuración de seguridad**:
     - **Microsoft Defender for Cloud**: Protege la infraestructura.
     - **Alertas**: Monitorear eventos y costos.
  4. **Advertencias clave**:
     - **No usar el slot de producción para CI/CD**: Usar slots de staging para pruebas.
     - **Validar archivo YAML**: Asegurar que el workflow no tenga errores de sintaxis.
    
<img src="https://github.com/user-attachments/assets/82ec9c77-539f-4e09-9278-05440a8c6fba"/>

##### 8. Resultado de implementación exitosa
- **Contenido**: Logs de ejecución y advertencias.
- **Pasos clave**:
  1. Verificar **Estado: Success** y duración (`20s`).
  2. Revisar **Annotations** para resolver errores (ej: propiedades no nulas en código).
  3. Acceder a enlaces de logs (`http://executor.buildbrackleapp.eu/index`).

<img src="https://github.com/user-attachments/assets/bc945708-86ea-42f5-8d2a-c88c24030044"/>
 
### 6.2.2.7. Team Collaboration Insights during Sprint

Se proporcionará información detallada sobre la colaboración y comunicación entre los miembros del equipo de desarrollo durante el sprint. Esto incluirá la coordinación de actividades, la gestión de tareas asignadas y la resolución de inconvenientes surgidos en el proceso. Las responsabilidades se distribuyeron equitativamente entre los integrantes del equipo. 

![image](https://github.com/user-attachments/assets/d395fe20-1590-4fe0-b113-e980cabad875)

![image](https://github.com/user-attachments/assets/787368a5-9062-4133-993e-36e0f1578a81)

<img width="1009" alt="image" src="https://github.com/user-attachments/assets/201b9282-79a2-4b97-ad54-072da78ab99a" />


### 6.3. Validation Interviews

#### 6.3.1. Diseño de Entrevistas

*¿Podría presentarse con su nombre completo, edad, distrito de residencia y ocupación?*

*Sobre el landing page, ¿la considera llamativa y visualmente interesante?*

*¿Considera que la información proporcionada comunica de forma correcta las funciones de nuestra aplicación?*

*¿Hay algo que considere deberíamos cambiar o eliminar en la página?*

*Sobre la aplicación, ¿las herramientas son claras y de fácil lectura?*

*¿Cree que nuestra aplicación le hubiera ayudado a tener mayor orden durante el proceso oncológico?*

*¿Qué cambios propondría para mejorar los elementos visuales de nuestra aplicación?*

*Si es que usara esta aplicación por primera vez sin una guía, ¿le parecería claro cómo utilizarla, o hay herramientas que no tienen un uso claro a simple vista?*

*¿Hay alguna opción o herramienta que cree que le falta a nuestra aplicación?*

*¿Recomendaría esta aplicación hacia médicos u otros pacientes oncológicos?*


**Médicos:**
*¿Considera que las herramientas brindadas mejorarían su orden con los pacientes?*
 
*¿Utilizaría la aplicación para organizar los procesos médicos de cada uno de sus pacientes?*

#### 6.3.2. Registro de Entrevistas

Entrevista 1: Verónica Mendoza, 52, Chorrillos, profesora de tiempo completo en la upc ; familiar de paciente oncológico

![Image](https://github.com/user-attachments/assets/72287442-0be9-452b-9a8e-d46d8c438d7e)

<br>https://drive.google.com/file/d/1aMSpnoVOVk1TBoXqOUFQYVw73LOTRLD1/view?usp=sharing

Resumen:

La entrevistada tuvo una buena experiencia con el landing page, considerándolo bastante llamativo de forma visual pero con información clara, permitiendo conocer el objetivo y función de nuestra startup y aplicación realizada. El único detalle que sugirió como cambio es que nuestro logo sea más visible, quizás aumentando su tamaño o colocándolo en más lugares.
Sobre la aplicación, la entrevistada también tuvo una buena experiencia con ella. Consideró que cada botón y enlace mostrado era bastante claro en su función, por lo que incluso podría utilizarla de forma correcta sin necesidad de una guía. Los únicos cambios que realizaría sobre la aplicación es que el calendario muestre más detalles sobre el mes y semana en la que se realizarán las citas, una sección que presenta noticias sobre tratamientos oncológicos recientes y simplemente que nuestro logo aparezca más visible.
La entrevistada consideró que nuestra aplicación sería de mucha ayuda para personas pasando por los procesos oncológicos, además de que las herramientas para los médicos les ayudarían a mejorar su eficiencia y organización, además de que le hubiera gustado mucho tener esta aplicación mientras que su pariente se encontró en el proceso oncológico.

<br>
Entrevista 2: Manuel Luis Ramos, 52, San Luis, posición administrativa en resocentro ; familiar de paciente oncológico

![Image](https://github.com/user-attachments/assets/6da53316-9263-469a-8576-f81e8c4775d5)

<br>https://drive.google.com/file/d/1uc8FAaD1ArRYNPcP5_7kGPWF3bItJdF_/view?usp=sharing <br>

Resumen:

El entrevistado consideró la landing page impactante de forma visual, con la información en ella explicando claramente nuestra aplicación y objetivo al realizarla. Los únicos cambios que considera importantes son el uso de lazos de más colores, ya que solo utilizar un lazo rosado está vinculado a un solo tipo de cáncer y podría hacer creer a un usuario que solo nos enfocamos en ese tipo. Otro cambio que considera es cambiar el título de "Trabajando por tu salud" a uno más enfocado al cáncer y tratamientos oncológicos.
Para la aplicación, el entrevistado considera que todo está claro y conciso y de fácil entendimiento, por lo que sí podría utilizarla aunque no tuviera a alguien que le explique como usarla. El único cambio que considera de gran importancia es que las aplicaciones no estén completamente vinculadas entre médicos y pacientes, es decir, si es que el médico no tenga la aplicación descargada, entonces el paciente debería poder registrar citas en su calendario personal. A parte de esto, la aplicación le parece de gran utilidad al entrevistado.

<br>
Entrevista 3: Eduard Travezaño, 20, San Juan de Lurigancho, Estudiante universitario ; familiar de paciente

![Image](https://github.com/user-attachments/assets/be7f293c-62ad-4055-ac2c-8d794cc31285)

<br>https://drive.google.com/file/d/13l0HOKYB5VeZ4CLpG4pVyeep5gKchQea/view?usp=sharing<br>

Resumen:

El entrevistado tuvo una buena experiencia con nuestro landing page, pareciéndole única y llamativa con los tonos de colores rosados y con información no abrumadora que cause confusión visual. La página muestra información que comunica fácilmente el uso de la aplicación, aunque desearía que nos enfocáramos a la salud en general, no solamente a tratamientos y médicos oncológicos, aunque entiende nuestra misión de enfocarnos en ellos.
En términos de la aplicación, todo le parece entendible y claro al entrevistado y le agrada el calendario, aunque desearía que hubiera más información sobre las citas y pacientes o médicos además de su nombre y fecha, cosas como especialidad o razón de cita.
Además, el entrevistado considera que la aplicación está bastante completa, pero una lista de visitas al paciente si es que estuviera internado sería de gran ayuda.

#### 6.3.3. Evaluaciones según heurísticas

#### UX Heuristics & Principles Evaluation

#### Usability - Inclusive Design - Information Architecture

* **CARRERA**: Ingeniería de Software
* **CURSO**: CC238
* **SECCION**: Aplicaciones para Dispositivos Móviles
* **PROFESORES**: Todos
* **AUDITOR**: EMSafe
* **CLIENTE(S)**: Todos



#### SITE O APP A EVALUAR:

EMSafe

#### TAREAS A EVALUAR:

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Registro y autenticación de usuarios (pacientes y doctores)

2. Actualización de perfil y configuración de cuenta

3. Visualización y aceptación de solicitudes de cita médica

4. Registro de síntomas y seguimiento de tratamiento

5. Visualización del calendario de procedimientos diarios

6. Configuración de recordatorios y notificaciones

7. Reprogramación o cancelación de citas

8. Interacción básica en el módulo de mensajería clínica

9. Visualización del historial de tratamientos


#### ESCALA DE SEVERIDAD:

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

| Nivel | Descripción |
| :---- | :---------- |
| 1     | Problema superficial: Puede ser fácilmente superado por el usuario y ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. |
| 2     | Problema menor: Puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente release. |
| 3     | Problema mayor: Ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les asigne una prioridad alta. |
| 4     | Problema muy grave: Un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. |

#### TABLA RESUMEN:

| # | Problema | Escala de severidad | Heurística/Principio violada(o) |
|:-:|:---------|:------------------:|:-------------------------------|
| 1 | Mensaje de error genérico sin información específica sobre el fallo | 3 | Ayudar a los usuarios a reconocer, diagnosticar y recuperarse de errores |
| 2 | Falta de indicador de progreso visual en el proceso de registro de 3 pasos | 2 | Visibilidad del estado del sistema |
| 3 | Botón "Finalize" habilitado incluso cuando hay errores de guardado | 4 | Prevención de errores |
| 4 | Campos obligatorios no están claramente identificados | 2 | Prevención de errores |
| 5 | Inconsistencia en el manejo de estados de la foto de perfil | 3 | Consistencia y estándares |

#### Problema Detallado

* **PROBLEMA #1:** Mensaje de error genérico sin información específica sobre el fallo
**Severidad:** 3
**Heurística violada:** Usability: Ayudar a los usuarios a reconocer, diagnosticar y recuperarse de errores

![Error saving profile](https://hebbkx1anhila5yf.public.blob.vercel-storage.com/6-Y35wL6ju2UYx03cDxAEbb2LJO5ANjC.png)

**Problema:** En el paso final del registro de perfil, cuando ocurre un error al guardar la información, el sistema muestra únicamente el mensaje "Error saving your profile" sin proporcionar detalles específicos sobre qué causó el fallo. Esto deja al usuario sin información sobre cómo proceder para resolver el problema, generando frustración y posibles abandonos del proceso de registro. El usuario no puede determinar si el error se debe a problemas de conectividad, formato de datos, tamaño de imagen, o algún otro factor.

**Recomendación:** Implementar mensajes de error específicos y descriptivos que indiquen la causa exacta del problema y las acciones que el usuario puede tomar para resolverlo. Por ejemplo: "Error al subir la imagen: El archivo es demasiado grande. Por favor, selecciona una imagen menor a 2MB" o "Error de conexión: Verifica tu conexión a internet e intenta nuevamente".

 * **PROBLEMA #2:** Falta de indicador de progreso visual en el proceso de registro de 3 pasos
**Severidad:** 2
**Heurística violada:** Usability: Visibilidad del estado del sistema

![Profile step 1](https://hebbkx1anhila5yf.public.blob.vercel-storage.com/2-tCn9DXyZep8CW3hAFOl7DdjcY2dWfX.png)

**Problema:** Durante el proceso de registro que consta de 3 pasos, aunque se indica textualmente "step X to 3" en el título, no existe un indicador visual de progreso como una barra de progreso o puntos indicadores. Esto hace que los usuarios no tengan una referencia clara y visual de su avance en el proceso, lo que puede generar incertidumbre sobre cuánto falta para completar el registro y puede llevar a abandonos prematuros del proceso.

**Recomendación:** Implementar un indicador visual de progreso en la parte superior de cada pantalla del proceso de registro. Esto puede ser una barra de progreso horizontal, puntos indicadores (1●●○) o pasos numerados visualmente destacados que muestren claramente el paso actual y los pasos restantes.

* **PROBLEMA #3:** Botón "Finalize" habilitado incluso cuando hay errores de guardado
**Severidad:** 4
**Heurística violada:** Usability: Prevención de errores

![Finalize button with error](https://hebbkx1anhila5yf.public.blob.vercel-storage.com/6-Y35wL6ju2UYx03cDxAEbb2LJO5ANjC.png)

**Problema:** En el paso final del registro, cuando se presenta el mensaje de error "Error saving your profile", el botón "Finalize" permanece habilitado y permite al usuario intentar finalizar el proceso nuevamente sin haber resuelto el error subyacente. Esto puede llevar a múltiples intentos fallidos, frustración del usuario y posible corrupción de datos. El sistema no previene que el usuario repita una acción que ya ha fallado sin antes corregir la causa del problema.

**Recomendación:** Deshabilitar el botón "Finalize" cuando se detecten errores en el proceso de guardado y solo habilitarlo nuevamente cuando el error haya sido resuelto. Alternativamente, cambiar el texto del botón a "Retry" o "Try Again" para indicar claramente que se está reintentando una acción que falló previamente.

* **PROBLEMA #4:** Campos obligatorios no están claramente identificados
**Severidad:** 2
**Heurística violada:** Usability: Prevención de errores

![Profile form fields](https://hebbkx1anhila5yf.public.blob.vercel-storage.com/3-lkdQpwcjK2xvMTxm2TwGyalLnlEGFF.png)

**Problema:** En los formularios de registro, especialmente en los pasos 1 y 2 del proceso de completar el perfil, no hay indicadores visuales claros (como asteriscos *) que identifiquen cuáles campos son obligatorios y cuáles son opcionales. Esto puede llevar a que los usuarios envíen formularios incompletos, generando errores de validación inesperados y requiriendo que el usuario regrese a completar información faltante, aumentando el tiempo y esfuerzo necesario para completar el registro.

**Recomendación:** Implementar indicadores visuales claros para campos obligatorios, como asteriscos rojos (*) junto al label del campo, o alternativamente, indicar claramente cuáles campos son opcionales con texto como "(opcional)". Además, implementar validación en tiempo real que muestre inmediatamente cuando un campo obligatorio está vacío.

* **PROBLEMA #5:** Inconsistencia en el manejo de estados de la foto de perfil
**Severidad:** 3  
**Heurística violada:** Usability: Consistencia y estándares

![No image state](https://hebbkx1anhila5yf.public.blob.vercel-storage.com/4-2Ruz6HYQ7oqizdCQUrn2AMvbCo9pFC.png)

**Problema:** En el paso 3 del registro, el manejo de la foto de perfil presenta inconsistencias en la presentación de estados. Cuando no hay imagen seleccionada, se muestra un círculo gris con "No image yet" y el texto "No image selected yet" debajo, creando redundancia. Además, no queda claro si la foto de perfil es obligatoria u opcional, ya que no hay opción visible para omitir este paso, pero tampoco se indica claramente que sea requerida.

**Recomendación:** Estandarizar la presentación de estados de la foto de perfil eliminando la redundancia textual. Mostrar claramente si la foto es opcional agregando un enlace "Skip for now" o "Add later", o si es obligatoria, indicarlo explícitamente. Mantener consistencia visual entre el estado vacío y el estado con imagen seleccionada.


### 6.4. Video About-the-Product

La sección proporciona un panorama general del producto, resaltando su objetivo, características principales y el valor que brinda a sus usuarios. Esta introducción facilita la comprensión del contexto del producto y su orientación a cubrir las demandas de los usuarios, sincronizando sus características y habilidades con las metas de la solución sugerida.

URL en Microsoft Teams:

Duración:

### 6.5. About the Team

Esta parte facilitará la identificación del equipo que impulsó el proyecto, mostrando un video que refleja la esencia de nuestro proceso laboral, resaltando cómo cada integrante aportó con sus destrezas y empeños. Además, cada participante relata en cámara su vivencia personal, detallando las tareas que llevó a cabo, los éxitos alcanzados y las habilidades que cultivó durante el proceso. Algunos de los éxitos alcanzados en el equipo comprenden una comunicación eficaz que nos facilitó mantenernos en sintonía en cada fase del proyecto, garantizando que todas las ideas y contribuciones fueran oídas y tenidas en cuenta.

URL en Microsoft Teams:

Duración:
