<il><h1><a href="./content/chapter-5/chapter-5.md">Capítulo V: Solution UI/UX Design</a></h1></il>

<il><h2><a href="./content/chapter-5/chapter-5.md">5.1. Product design</a></h2></il>

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.1. Style Guidelines</a></h3></il>

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.1.1. General Style Guidelines</a></h3></il>

### Branding

El branding de OnControl refleja nuestra misión de proporcionar apoyo integral a pacientes oncológicos y médicos en Perú. Nuestros elementos visuales comunican confianza, empatía y profesionalismo.

### Logo

El logo de OnControl combina elementos visuales que representan nuestra misión:

- La palabra "ONCO" en rojo y "NTROL" en azul, simbolizando la dualidad entre el paciente y el médico
- El lazo rosa formando un corazón, representando la conciencia sobre el cáncer y el cuidado centrado en el paciente


**Uso del logo:**

- Mantener siempre el espacio de protección alrededor del logo (equivalente a la altura de la letra "O")
- No distorsionar, rotar o cambiar los colores del logo
- En fondos oscuros, utilizar la versión blanca del logo
- Tamaño mínimo: 40px de altura para asegurar legibilidad

![Image](https://github.com/user-attachments/assets/4e55c970-22a6-4d60-8ec1-8a5da4e7eb16)


### Typography

La tipografía principal de OnControl es Poppins, una fuente sans-serif moderna y legible que transmite profesionalismo y accesibilidad.

```css
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");

:root {
  --font-primary: "Poppins", sans-serif;
}
```

**Jerarquía tipográfica:**

| Elemento | Tamaño | Peso | Uso
|-----|-----|-----|-----
| H1 | 3rem (48px) | 700 | Títulos principales, hero section
| H2 | 2.5rem (40px) | 700 | Títulos de sección
| H3 | 1.5rem (24px) | 600 | Subtítulos, encabezados de tarjetas
| H4 | 1.3rem (20px) | 600 | Títulos menores
| Body | 1rem (16px) | 400 | Texto general
| Small | 0.875rem (14px) | 400 | Texto secundario, pies de página


![Image](https://github.com/user-attachments/assets/1c7b0440-c7d0-4818-ac12-5335a309222b)

### Colors

La paleta de colores de OnControl está diseñada para transmitir confianza, tranquilidad y esperanza, utilizando tonos que reflejan el sector de la salud con acentos que aportan calidez y energía.

```css
:root {
  /* Colores primarios */
  --primary: #00796b;      /* Verde teal - Color principal */
  --secondary: #004d40;    /* Verde teal oscuro - Color secundario */
  --accent: #ff5722;       /* Naranja - Color de acento */
  
  /* Colores de la marca */
  --brand-red: #ff3333;    /* Rojo del logo - "ONCO" */
  --brand-blue: #0033cc;   /* Azul del logo - "NTROL" */
  --brand-pink: #e91e63;   /* Rosa del lazo */
  
  /* Colores neutros */
  --background: #f5f5f5;   /* Fondo general */
  --foreground: #212121;   /* Texto principal */
  --card: #ffffff;         /* Fondo de tarjetas */
  --card-hover: #e0e0e0;   /* Estado hover de tarjetas */
  
  /* Colores de estado */
  --success: #4caf50;      /* Éxito */
  --warning: #ff9800;      /* Advertencia */
  --error: #f44336;        /* Error */
  --info: #2196f3;         /* Información */
}
```

**Uso de colores:**

- **Color primario (--primary)**: Utilizado para la barra de navegación, fondos de secciones importantes y elementos principales.
- **Color secundario (--secondary)**: Utilizado para gradientes, elementos secundarios y estados hover.
- **Color de acento (--accent)**: Utilizado para botones de llamada a la acción, iconos destacados y elementos que requieren atención.
- **Colores de la marca**: Reservados principalmente para el logo y elementos visuales de identidad.
- **Colores neutros**: Utilizados para fondos, texto y elementos de interfaz general.

![Image](https://github.com/user-attachments/assets/f2c90d9a-edee-44c8-9327-af86b706a563)

### Spacing

El sistema de espaciado de OnControl sigue un patrón consistente para crear una jerarquía visual clara y una experiencia de usuario coherente.

```css
:root {
  --spacing-xs: 0.25rem;   /* 4px */
  --spacing-sm: 0.5rem;    /* 8px */
  --spacing-md: 1rem;      /* 16px */
  --spacing-lg: 1.5rem;    /* 24px */
  --spacing-xl: 2rem;      /* 32px */
  --spacing-2xl: 3rem;     /* 48px */
  --spacing-3xl: 4rem;     /* 64px */
  --spacing-4xl: 5rem;     /* 80px */
}
```

**Principios de espaciado:**

- Utilizar espaciado consistente entre secciones (--spacing-3xl o --spacing-4xl)
- Mantener un espaciado interno consistente en tarjetas y contenedores (--spacing-lg o --spacing-xl)
- Aplicar espaciado vertical entre elementos de texto según su jerarquía
- Utilizar márgenes proporcionales al tamaño de los elementos


### Componentes UI

#### Botones

Los botones en OnControl siguen un diseño consistente con bordes redondeados y transiciones suaves.

```css
.cta-button {
  display: inline-block;
  background-color: var(--accent);
  color: white;
  padding: 12px 30px;
  border-radius: 30px;
  text-decoration: none;
  font-weight: 600;
  transition: background-color 0.3s ease, transform 0.3s ease;
  border: none;
  cursor: pointer;
}

.cta-button:hover {
  background-color: #e64a19;
  transform: translateY(-3px);
}

.cta-button.secondary {
  background-color: transparent;
  border: 2px solid white;
}

.cta-button.secondary:hover {
  background-color: rgba(255, 255, 255, 0.2);
}
```

**Variantes de botones:**

- **Primario**: Fondo naranja (--accent), texto blanco
- **Secundario**: Borde blanco, fondo transparente, texto blanco
- **Terciario**: Solo texto, sin fondo ni borde


#### Tarjetas

Las tarjetas son componentes fundamentales que muestran información agrupada con un estilo consistente.

```css
.card {
  background-color: var(--card);
  border-radius: 10px;
  padding: 30px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}
```

#### Iconografía

OnControl utiliza iconos de Font Awesome para mantener un estilo coherente en toda la interfaz.

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

**Uso de iconos:**

- Mantener tamaños consistentes (generalmente 1.5rem para iconos estándar)
- Utilizar el color primario o de acento para iconos destacados
- Aplicar el mismo estilo de transición para estados hover


### Accesibilidad

OnControl se compromete a crear una experiencia inclusiva para todos los usuarios, incluyendo aquellos con discapacidades.

**Principios de accesibilidad:**

- Mantener un contraste de color adecuado (relación mínima de 4.5:1 para texto normal)
- Utilizar etiquetas semánticas HTML5 (header, nav, main, section, etc.)
- Incluir atributos alt en todas las imágenes
- Asegurar que todos los elementos interactivos sean accesibles mediante teclado
- Implementar ARIA roles y atributos cuando sea necesario


### Implementación y Mantenimiento

Esta guía de estilo debe ser consultada y seguida por todos los miembros del equipo de OnControl. Para mantener la consistencia:

1. Revisar esta documentación antes de comenzar nuevos desarrollos
2. Utilizar los componentes y tokens definidos en este documento
3. Consultar con el equipo de diseño ante cualquier duda o necesidad de nuevos elementos
4. Actualizar esta guía cuando se realicen cambios significativos en el diseño


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2. Information Architecture</a></h3></il>
<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.1. Organization Systems</a></h3></il>

Gracias por la aclaración. A continuación te presento la versión mejorada en Markdown que conserva toda la información original sin sintetizarla, pero mejora su presentación visual mediante el uso de cuadros y separación clara por secciones. Se ha respetado el tamaño de los subtítulos y el tono serio del informe.



En OnControl, hemos diseñado sistemas de organización enfocados exclusivamente en las funcionalidades específicas que implementaremos en nuestra plataforma para satisfacer las necesidades de nuestros dos grupos de usuarios principales: médicos oncólogos y pacientes con cáncer.

### Organización Visual del Contenido

#### 1. Organización Jerárquica (Visual Hierarchy)

Aplicamos la organización jerárquica en las siguientes áreas:

* Landing Page

| Elemento              | Descripción                                                                                                                                                                              |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Navegación principal  | Estructura con priorización visual clara: las características más importantes (calendario, tratamientos, comunicación) se destacan mediante iconos más grandes y posiciones prominentes. |
| Sección de beneficios | Organizada jerárquicamente según la relevancia para cada tipo de usuario, comenzando con médicos y luego pacientes.                                                                      |

* Aplicación

| Elemento                | Descripción                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------------------------- |
| Menú principal          | Funcionalidades organizadas por importancia: Tratamientos, Citas, Calendario y Chat como elementos primarios. |
| Sección de tratamientos | Elementos visuales que destacan el estado actual (creado, iniciado, actualizado).                             |
| Sección de citas        | Indicadores visuales que muestran su estado (creada, cancelada, aceptada).                                    |



#### 2. Organización Secuencial (Step-by-Step)

Implementamos la organización secuencial en procesos que requieren completar pasos específicos:

* Para Médicos

| Proceso                 | Secuencia de pasos                                                                                                           |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Registro de cuenta      | Doctor registrado → Método de pago configurado                                                                               |
| Creación de tratamiento | Crear tratamiento → Asignar procedimiento → Revisar personal → Editar procedimiento → Aceptar solicitud → Tratamiento creado |
| Gestión de citas        | Crear cita → Enviar solicitud → Aceptar cita                                                                                 |

* Para Pacientes

| Proceso              | Secuencia de pasos                                         |
| -------------------- | ---------------------------------------------------------- |
| Registro de cuenta   | Registrar cuenta → Aceptar solicitud → Paciente registrado |
| Solicitud de cita    | Solicitud enviada → Solicitud aceptada → Cita creada       |
| Registro de síntomas | Marcar síntomas personalizados → Registrar síntomas        |



#### 3. Organización Matricial

Utilizamos la organización matricial para presentar información que puede ser analizada desde múltiples dimensiones:

| Área         | Descripción                                                                                                                                                      |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Calendario   | - Vista matricial que muestra días/fechas (eje horizontal) vs. eventos (eje vertical).<br>- Organización de recordatorios y citas en formato de matriz temporal. |
| Tratamientos | - Matriz que relaciona procedimientos con fechas de inicio/modificación.<br>- Vista que relaciona tratamientos con especialistas asignados.                      |



### Esquemas de Categorización de Contenido

#### 1. Categorización por Tópicos

Este es nuestro esquema principal de categorización, aplicado en:

*  Para Médicos

| Área                    | Categorización                                                          |
| ----------------------- | ----------------------------------------------------------------------- |
| Menú principal          | Organizado por áreas funcionales: Tratamientos, Citas, Calendario, Chat |
| Sección de tratamientos | Categorizada por: Tratamientos creados, Procedimientos, Solicitudes     |

* Para Pacientes

| Área                   | Categorización                                                |
| ---------------------- | ------------------------------------------------------------- |
| Menú principal         | Organizado por: Solicitudes, Citas, Síntomas, Chat            |
| Sección de solicitudes | Categorizada por: Solicitudes enviadas, Solicitudes aceptadas |



#### 2. Categorización por Audiencia

Aplicamos este esquema para diferenciar claramente el contenido según el tipo de usuario:

| Audiencia                  | Descripción                                                                                     |
| -------------------------- | ----------------------------------------------------------------------------------------------- |
| Experiencia para Médicos   | Enfocada en la creación de tratamientos, gestión de procedimientos y aprobación de solicitudes. |
| Experiencia para Pacientes | Centrada en enviar solicitudes, registrar síntomas y comunicarse con su doctor.                 |

* La landing page utiliza esta categorización para presentar beneficios específicos para cada audiencia, con secciones claramente diferenciadas para médicos y pacientes.


#### 3. Categorización por Estado

Utilizamos la categorización por estado como esquema principal para organizar elementos según su situación actual:

* Para Médicos

| Elemento       | Estados posibles                    |
| -------------- | ----------------------------------- |
| Tratamientos   | Creados, Iniciados, Actualizados    |
| Procedimientos | Asignados, Realizados, Actualizados |
| Solicitudes    | Pendientes, Aceptadas, Rechazadas   |
| Citas          | Creadas, Canceladas                 |

* Para Pacientes

| Elemento    | Estados posibles                 |
| ----------- | -------------------------------- |
| Solicitudes | Enviadas, Aceptadas, Rechazadas  |
| Citas       | Creadas, Confirmadas, Canceladas |
| Permisos    | Concedidos                       |



#### 4. Categorización Cronológica

Implementamos la organización cronológica en:

* Calendario

| Elemento      | Organización temporal                                     |
| ------------- | --------------------------------------------------------- |
| Recordatorios | Organizados cronológicamente                              |
| Citas         | Ordenadas por fecha y hora                                |
| Funcionalidad | Opción para actualizar, eliminar o posponer recordatorios |

* Chat

| Elemento          | Organización temporal          |
| ----------------- | ------------------------------ |
| Mensajes          | Organizados cronológicamente   |
| Historial         | Ordenado por fecha y hora      |
| Archivos adjuntos | Organizados por fecha de envío |

* Tratamientos

| Elemento                    | Organización temporal                    |
| --------------------------- | ---------------------------------------- |
| Historial de modificaciones | Registro cronológico de fechas de inicio |
| Procedimientos              | Secuencia cronológica de actividades     |


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.2. Labelling Systems</a></h3></il>

A continuación, se presenta el sistema de etiquetado utilizado en la Landing Page de OnControl, diseñado para representar de forma clara, concisa y accesible los distintos grupos de información relevantes para médicos oncólogos y pacientes. Las etiquetas seleccionadas utilizan un lenguaje simple, directo y empático, evitando tecnicismos innecesarios para facilitar la navegación y comprensión por parte de todos los usuarios.

### Etiquetas de Navegación Principal

| Etiqueta | Descripción
|-----|-----
| **Características** | Funcionalidades clave de la plataforma, presentadas con iconos y descripciones breves.
| **Beneficios** | Ventajas específicas para médicos y pacientes, organizadas en tarjetas visuales.
| **Problemática** | Contexto sobre los desafíos en la atención oncológica en Perú y cómo OnControl los aborda.
| **Testimonios** | Experiencias de usuarios reales, etiquetadas por rol (paciente, médico, familiar).
| **Contacto** | Formulario para solicitar información o una demostración personalizada.
| **Descargar App** | Sección dedicada a la descarga de la aplicación para iOS y Android.



### Etiquetas de la Sección Hero

| Etiqueta | Descripción
|-----|-----
| **Apoyo integral para pacientes oncológicos** | Título principal que comunica el propósito central de la plataforma.
| **Solicitar demo** | Botón transparente que dirige al formulario de contacto para profesionales interesados.
| **Descargar App** | Botón de acento (naranja) que dirige a la sección de descarga de la aplicación.


### Etiquetas de Características

| Etiqueta | Descripción
|-----|-----
| **Características principales** | Encabezado de sección que introduce las funcionalidades clave.
| **Calendario Integrado** | Tarjeta que describe la funcionalidad de gestión de citas y recordatorios.
| **Gestión de Medicamentos** | Tarjeta que explica el seguimiento de tratamientos y medicación.
| **Comunicación Directa** | Tarjeta que presenta el sistema de chat entre médicos y pacientes.


### Etiquetas de Beneficios

| Etiqueta | Descripción
|-----|-----
| **Beneficios** | Encabezado de sección que introduce las ventajas de la plataforma.
| **Para Médicos Oncólogos** | Subsección que agrupa beneficios específicos para profesionales médicos.
| **Para Pacientes** | Subsección que agrupa beneficios específicos para personas con cáncer.
| **Para Familiares** | Subsección que agrupa beneficios para el entorno de apoyo del paciente.
| **Para el Sistema de Salud** | Subsección que presenta ventajas a nivel institucional y sistémico.


### Etiquetas de Problemática

| Etiqueta | Descripción
|-----|-----
| **La problemática** | Encabezado de sección que introduce el contexto del problema.
| **Desafíos en la atención oncológica** | Subtítulo que enmarca la situación actual en Perú.
| **Más Acerca del Problema** | Etiqueta que introduce el contenido multimedia explicativo.


### Etiquetas de Descarga de App

| Etiqueta | Descripción
|-----|-----
| **Lleva el control de tu tratamiento donde vayas** | Título que comunica el beneficio principal de la aplicación móvil.
| **Descargar en App Store** | Botón con ícono de Apple para usuarios iOS.
| **Disponible en Google Play** | Botón con ícono de Google Play para usuarios Android.


### Etiquetas de Testimonios

| Etiqueta | Descripción
|-----|-----
| **Lo que dicen nuestros usuarios** | Encabezado que introduce las experiencias de usuarios reales.
| **[Nombre], Paciente oncológica** | Formato de atribución para testimonios de pacientes.
| **Dr. [Nombre], Oncólogo** | Formato de atribución para testimonios de médicos.
| **[Nombre], Familiar de paciente** | Formato de atribución para testimonios de familiares.


### Etiquetas de Contacto

| Etiqueta | Descripción
|-----|-----
| **¿Listo para mejorar la experiencia oncológica?** | Título que invita a la acción con un tono positivo y orientado a soluciones.
| **Contáctanos hoy mismo para una demostración personalizada** | Subtítulo que especifica el propósito del formulario.
| **Tipo de usuario** | Campo desplegable con opciones: Paciente, Médico, Familiar de paciente, Otro.
| **Enviar** | Botón de envío del formulario con color de acento para destacarlo.


### Etiquetas de Footer

| Etiqueta | Descripción
|-----|-----
| **Navegación** | Encabezado de columna para enlaces internos del sitio.
| **Contacto** | Encabezado de columna para información de contacto directo.
| **Síguenos** | Encabezado de columna para redes sociales.
| **Política de Privacidad** | Enlace a información legal sobre manejo de datos.
| **Términos y Condiciones** | Enlace a información legal sobre uso del servicio.

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.3. SEO Tags and Meta Tags</a></h3></il>

En esta sección se detallan los elementos de optimización para motores de búsqueda (SEO) y metaetiquetas que implementaremos en la landing page y aplicación web de OnControl, así como los elementos de optimización para tiendas de aplicaciones (ASO) para nuestras aplicaciones móviles.

### Landing Page

#### Title Tags

| Página | Title Tag
|-----|-----
| **Home** | OnControl - Apoyo integral para pacientes oncológicos en Perú
| **Características** | Características de OnControl - Gestión eficiente de tratamientos oncológicos
| **Beneficios** | Beneficios de OnControl - Mejorando la experiencia oncológica para médicos y pacientes
| **Contacto** | Contacta con OnControl - Solicita una demo personalizada


#### Meta Description Tags

| Página | Meta Description
|-----|-----
| **Home** | OnControl facilita la gestión del tratamiento oncológico, mejorando la comunicación entre médicos y pacientes para una atención más efectiva y personalizada en Perú.
| **Características** | Descubre las funcionalidades de OnControl: calendario integrado, gestión de medicamentos y comunicación directa entre médicos oncólogos y pacientes.
| **Beneficios** | OnControl reduce la ansiedad de los pacientes y optimiza el tiempo de los médicos oncólogos, mejorando la calidad de la atención oncológica en Perú.
| **Contacto** | Solicita una demostración personalizada de OnControl y descubre cómo podemos mejorar la experiencia oncológica para ti o tus pacientes.


#### Meta Keywords

```html
<meta name="keywords" content="oncología, cáncer, tratamiento oncológico, pacientes oncológicos, médicos oncólogos, gestión médica, Perú, aplicación médica, seguimiento de tratamiento, comunicación médico-paciente, citas médicas, recordatorios de medicamentos">
```

#### Meta Author

```html
<meta name="author" content="OnControl - Equipo de Desarrollo">
```

#### Open Graph Tags

```html
<meta property="og:title" content="OnControl - Apoyo integral para pacientes oncológicos">
<meta property="og:description" content="Plataforma que facilita la gestión del tratamiento oncológico, mejorando la comunicación entre médicos y pacientes.">
<meta property="og:image" content="https://oncontrol.pe/images/og-image.jpg">
<meta property="og:url" content="https://oncontrol.pe">
<meta property="og:type" content="website">
```

### Aplicaciones Móviles (ASO)

#### App Store (iOS)

| Elemento ASO | Contenido
|-----|-----
| **App Name** | OnControl: Gestión Oncológica
| **App Subtitle** | Tratamientos y citas de cáncer
| **Keywords** | oncología, cáncer, tratamiento, citas, médico, paciente, recordatorio, calendario, chat médico, Perú
| **App Description (Primeros párrafos)** | OnControl es la aplicación esencial para pacientes oncológicos y médicos en Perú. Gestiona tratamientos, citas y comunicación en un solo lugar.<br><br>Diseñada específicamente para mejorar la experiencia oncológica, OnControl te permite llevar un seguimiento detallado de tu tratamiento o el de tus pacientes, con recordatorios personalizados y comunicación directa entre médicos y pacientes.
| **Promotional Text** | ¡Nuevo! Ahora con sistema mejorado de registro de síntomas y notificaciones en tiempo real.


#### Google Play Store (Android)

| Elemento ASO | Contenido
|-----|-----
| **App Title** | OnControl: Gestión de Tratamientos Oncológicos
| **Short Description** | Aplicación para pacientes con cáncer y médicos oncólogos en Perú.
| **Long Description (Inicio)** | OnControl es la solución integral para la gestión de tratamientos oncológicos en Perú, diseñada tanto para pacientes como para médicos especialistas.<br><br>Nuestra aplicación facilita el seguimiento de tratamientos, la gestión de citas médicas, el registro de síntomas y la comunicación directa entre médicos y pacientes, todo en una interfaz intuitiva y accesible.
| **Feature Graphic Text** | Mejorando la experiencia oncológica en Perú
| **Categoría Principal** | Medicina
| **Categoría Secundaria** | Salud y bienestar


### Estrategia de Implementación

1. **Optimización Local**: Incluiremos referencias geográficas a Perú y ciudades principales para mejorar el posicionamiento local.
2. **Palabras Clave Longtail**: Incorporaremos términos específicos como "gestión de tratamiento de cáncer de mama" o "seguimiento de quimioterapia" en páginas internas.
3. **Metaetiquetas Dinámicas**: Para secciones como tratamientos específicos, generaremos metaetiquetas dinámicas basadas en el contenido.
4. **Actualización Regular**: Revisaremos y actualizaremos las metaetiquetas trimestralmente para mantener la relevancia y optimizar el rendimiento.

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.4. Searching Systems</a></h3></il>

En esta sección detallamos los sistemas de búsqueda que implementaremos en OnControl para ayudar a los usuarios a encontrar información relevante de manera eficiente, evitando la sensación de desorientación ante el volumen de datos disponibles.

### Tipos de Búsqueda por Interfaz

#### 1. Landing Page

La landing page implementará un sistema de búsqueda simple:

- **Barra de búsqueda en header**: Permitirá buscar términos generales dentro del contenido de la landing page.
- **Resultados**: Se mostrarán en una página dedicada, organizados por secciones relevantes (Características, Beneficios, FAQ).
- **Sugerencias de búsqueda**: Se mostrarán términos populares relacionados con oncología mientras el usuario escribe.


#### 2. Aplicación Móvil

##### Para Médicos

| Sección | Tipo de Búsqueda | Filtros Disponibles | Visualización de Resultados
|-----|-----|-----|-----
| **Pacientes** | Búsqueda por texto con autocompletado | • Nombre/ID<br> • Tipo de cáncer<br>• Estado de tratamiento<br>• Fecha de última cita | Lista con tarjetas de paciente que muestran foto, nombre, diagnóstico principal y próxima cita
| **Tratamientos** | Búsqueda combinada (texto + filtros) | • Estado (creado, iniciado, actualizado)<br>• Tipo de tratamiento<br>• Fecha de inicio<br>• Especialista asignado | Vista tabular con opciones para expandir detalles de cada tratamiento
| **Citas** | Búsqueda en calendario + texto | • Rango de fechas<br>• Estado (creada, confirmada, cancelada)<br>• Tipo de cita<br>• Paciente | Vista de calendario con opción de cambiar a lista, mostrando hora, paciente y tipo de cita
| **Chat** | Búsqueda en conversaciones | • Paciente<br>• Fecha<br>• Contenido del mensaje<br>• Archivos adjuntos | Fragmentos de conversación con la opción de ver el contexto completo


##### Para Pacientes

| Sección | Tipo de Búsqueda | Filtros Disponibles | Visualización de Resultados
|-----|-----|-----|-----
| **Tratamientos** | Búsqueda por texto simple | • Estado (activo, completado)<br>• Fecha de inicio<br>• Tipo de tratamiento | Tarjetas con información resumida y opción para ver detalles
| **Citas** | Búsqueda en calendario | • Estado (solicitada, confirmada, cancelada)<br>• Rango de fechas<br>• Tipo de cita | Vista de calendario con opción de lista, mostrando fecha, hora, doctor y estado
| **Síntomas** | Búsqueda por categoría y texto | • Tipo de síntoma<br>• Intensidad<br>• Fecha de registro | Gráfico temporal con opción de ver lista detallada
| **Chat** | Búsqueda en historial | • Fecha<br>• Contenido del mensaje | Fragmentos de conversación con contexto


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.5. Navigation Systems</a></h3></il>

En esta sección detallamos los sistemas de navegación que implementaremos en OnControl para guiar a los usuarios a través de la landing page y las aplicaciones, permitiéndoles cumplir sus objetivos e interactuar satisfactoriamente con el producto.

### Landing Page

#### 1. Navegación Global

- **Barra de navegación fija**: Permanece visible al hacer scroll, incluyendo logo, enlaces a secciones principales y botón de descarga destacado.
- **Estructura jerárquica**: Organización clara de elementos por importancia, con el botón "Descargar App" visualmente destacado.
- **Navegación responsiva**: Se transforma en menú hamburguesa en dispositivos móviles.


#### 2. Navegación Contextual

- **Botones de llamada a la acción (CTA)**: Estratégicamente ubicados a lo largo de la página, guiando al usuario hacia la descarga o solicitud de demo.
- **Enlaces internos**: Dentro del contenido para facilitar la navegación entre secciones relacionadas.
- **Navegación por anclas**: Permite saltar directamente a secciones específicas desde la barra de navegación.


#### 3. Navegación de Utilidad

- **Footer**: Contiene enlaces a información legal, contacto y mapa del sitio.
- **Botón de regreso arriba**: Aparece al hacer scroll para facilitar el retorno al inicio.
- **Breadcrumbs**: En páginas internas para mostrar la ubicación actual y permitir navegación hacia atrás.


#### 4. Indicadores de Navegación

- **Resaltado de sección activa**: La sección actual se destaca en la barra de navegación.
- **Cambio de estado en hover**: Feedback visual al pasar el cursor sobre elementos navegables.
- **Animaciones de transición**: Suaves desplazamientos al navegar entre secciones mediante anclas.


### Aplicación Móvil

#### Estructura de Navegación Principal

##### 1. Para Médicos

- **Navegación por pestañas**: Acceso rápido a las secciones principales:

    - Tratamientos
    - Pacientes
    - Citas
    - Calendario
    - Chat

- **Menú lateral expandible**: Para acceso a funciones secundarias y configuración.
- **Barra inferior en móvil**: Con iconos para las funciones principales.


##### 2. Para Pacientes

- **Navegación simplificada**: Enfocada en las necesidades del paciente:

    - Mi Tratamiento
    - Mis Citas
    - Mis Síntomas
    - Chat con Doctor



- **Menú de hamburguesa**: Para acceso a configuración y funciones secundarias.
- **Barra inferior en móvil**: Con iconos intuitivos para las funciones principales.



<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3. Landing Page UI Design</a></h3></il>

Las Landing Pages juegan un rol fundamental en la conversión de visitantes en potenciales usuarios, empleando para ello mensajes persuasivos, información clave sobre el producto y un diseño intuitivo. Reconociendo su importancia, se ha desarrollado una propuesta de diseño preliminar adaptable tanto a dispositivos móviles como a computadoras de escritorio.

Para la experiencia en computadoras, se ha concebido una interfaz con secciones visuales y opciones de navegación explícitas, acompañadas de descripciones concisas de las funcionalidades principales del sitio web. El objetivo es asegurar una comprensión inmediata y eliminar cualquier posible fricción para el usuario. Adicionalmente, se ha dispuesto una barra de navegación de posición fija, garantizando su accesibilidad constante y facilitando la exploración fluida del contenido de la Landing Page.

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.1. Landing Page Wireframe</a></h3></il>

En esta sección se presentarán los wireframes de la versión de la versión con menos exactitud del Landing Page.

* **Sección Inicio y Caracteristicas**

![Image](https://github.com/user-attachments/assets/0eb45035-16a5-43ec-9d3c-e3d0804f8f2e)

* **Sección Beneficios**

![Image](https://github.com/user-attachments/assets/402f71a5-8e20-4a1d-a88e-0bd3e1e82e64)

* **Sección Problema y Testimonios**

![Image](https://github.com/user-attachments/assets/f0bd95a9-1022-4c72-8071-0c74a404571f)

* **Sección Contacto**
 
![Image](https://github.com/user-attachments/assets/25e3440d-18e0-48ad-8d87-75f5c3439a20)

* **Sección Descargas y Footer**

![Image](https://github.com/user-attachments/assets/09051eb1-96b2-4581-821e-d6d3a93cd809)

Figma: [Enlace Figma](https://www.figma.com/design/Q6qOeWezIbHOmzR6j1iWoX/Oncontigo-Mockups--Copia-?node-id=0-1&t=n4MWl8U3TC54ga3v-1)


<br>
<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.2. Landing Page Mock-up</a></h3></il>
En esta sección se presenta el mock-up de la landing page diseñada para la plataforma EMSafe. A diferencia del wireframe, este mock-up ofrece una representación visual más cercana al producto final, incorporando elementos gráficos, colores, tipografías y disposición de contenido que reflejan la identidad visual de la marca. El objetivo de esta propuesta es demostrar cómo se comunicarán los principales beneficios del sistema, el problema que resuelve, su ubicación, y facilitar el contacto con potenciales usuarios.


* **Sección Inicio**


* **Sección Beneficios**


* **Sección Problema**


* **Sección Testimonio**


* **Sección Contacto**


* **Sección Descarga**


Figma: [Enlace Figma](https://www.figma.com/design/Q6qOeWezIbHOmzR6j1iWoX/Oncontigo-Mockups--Copia-?node-id=0-1&t=n4MWl8U3TC54ga3v-1)

<br>

