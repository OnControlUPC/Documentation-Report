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

#### 6.2.1.1. Sprint Planning 1

| Elemento                     | Detalle                                                                 |
|-----------------------------|-------------------------------------------------------------------------|
| Sprint #                    | Sprint 1                                                                |
| Sprint Planning Date        | 2025-10-05                                                              |
| Time                        | 03:00 PM                                                                |
| Location                    | Meet                                          |
| Prepared By                 | Quique Vladimir Jara Benites                                             |
| Attendees                   | Williams Góngora / Quique Jara / Oscar Garayar / Juan Ramos / Michael Quispe |
| Sprint Review Summary       | No aplica (primer sprint).                                             |
| Sprint Retrospective Summary| No aplica (primer sprint).                                             |
| Sprint Goal                 | Diseñar y presentar la estructura inicial del proyecto OnControl, definiendo mockups, visión y funcionalidades clave de la aplicación para oncología. |
| Sprint Velocity             | 4                                                                       |
| Sum of Story Points         | 15                                                                      |



#### 6.2.1.2. Sprint Backlog 1

| Sprint # | User Story                          | Task   | ID     | Title                                | Description                                                       | Hours | Assigned To      | Status |
|----------|--------------------------------------|--------|--------|--------------------------------------|-------------------------------------------------------------------|--------|------------------|--------|
| Sprint 1 | HU01: Definición de la idea          | TA01   | #001   | Redacción de la visión del producto  | Definir la visión principal de la aplicación OnControl            | 3      | Michael Quispe   | Done   |
| Sprint 1 | HU02: Perfil del equipo              | TA02   | #002   | Recolección de perfiles              | Descripción de integrantes y sus habilidades                      | 2      | Juan Ramos       | Done   |
| Sprint 1 | HU03: Definición de usuarios y problemas | TA03   | #003   | Identificación de segmentos          | Segmentación del público objetivo y problemática                  | 3      | Williams Góngora | Done   |



#### 6.2.1.3. Development Evidence for Sprint Review



#### 6.2.1.4. Execution Evidence for Sprint Review

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
 <img src="https://github.com/user-attachments/assets/91ca2728-48b9-4d08-a8fe-82af82e5d5f7"/>




#### 6.2.1.5. Services Documentation Evidence for Sprint Review





#### 6.2.1.6. Software Deployment Evidence for Sprint Review

- Repositorio inicial creado en GitHub: [https://github.com/OnControlUPC](https://github.com/OnControlUPC)
- Estructura base para la Landing Page.
- Implementación preliminar de HTML y CSS del index principal.



#### 6.2.1.7. Team Collaboration Insights during Sprint



