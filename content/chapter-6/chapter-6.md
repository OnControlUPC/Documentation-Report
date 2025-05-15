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

#### 6.2.1.1. Sprint Planning 1


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
        <td>Quispe Quique Vladimir Jara Benites</td>
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


#### 6.2.1.2. Sprint Backlog 1

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


#### 6.2.1.3. Development Evidence for Sprint Review

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

#### 6.2.1.4. Execution Evidence for Sprint Review

En este primer Sprint del proyecto, hemos logrado implementar y desplegar una Landing Page operativa que comunica la propuesta de valor, dirige a las tiendas de aplicaciones y permite la suscripción por correo electrónico. Adicionalmente, se completó la creación y el despliegue del backend, incluyendo las APIs necesarias para la gestión de usuarios y la autenticación. Finalmente, se desarrolló e implementó la primera versión de nuestra aplicación móvil, permitiendo a los usuarios registrarse e iniciar sesión en la plataforma.

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



#### 6.2.1.5. Services Documentation Evidence for Sprint Review

Durante el presente Sprint, se desarrollaron y documentaron diversos endpoints que forman parte de los servicios backend de la aplicación. Estos endpoints permiten la interacción entre el cliente la aplicación.


![Api](https://github.com/user-attachments/assets/9dc5be2b-ce4b-4920-a21b-61ce14b29ef3)



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



