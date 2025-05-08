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


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.3. SEO Tags and Meta Tags</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.4. Searching Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.5. Navigation Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3. Landing Page UI Design</a></h3></il>

Las Landing Pages juegan un rol fundamental en la conversión de visitantes en potenciales usuarios, empleando para ello mensajes persuasivos, información clave sobre el producto y un diseño intuitivo. Reconociendo su importancia, se ha desarrollado una propuesta de diseño preliminar adaptable tanto a dispositivos móviles como a computadoras de escritorio.

Para la experiencia en computadoras, se ha concebido una interfaz con secciones visuales y opciones de navegación explícitas, acompañadas de descripciones concisas de las funcionalidades principales del sitio web. El objetivo es asegurar una comprensión inmediata y eliminar cualquier posible fricción para el usuario. Adicionalmente, se ha dispuesto una barra de navegación de posición fija, garantizando su accesibilidad constante y facilitando la exploración fluida del contenido de la Landing Page.

<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.1. Landing Page Wireframe</a></h3></il>

En esta sección se presentarán los wireframes de la versión de la versión con menos exactitud del Landing Page.

* **Sección Inicio**


* **Sección Beneficios**


* **Sección Problema**


* **Sección Contacto**


* **Sección Descarga**




Figma: [Enlace Figma]()


<br>
<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.2. Landing Page Mock-up</a></h3></il>
En esta sección se presenta el mock-up de la landing page diseñada para la plataforma EMSafe. A diferencia del wireframe, este mock-up ofrece una representación visual más cercana al producto final, incorporando elementos gráficos, colores, tipografías y disposición de contenido que reflejan la identidad visual de la marca. El objetivo de esta propuesta es demostrar cómo se comunicarán los principales beneficios del sistema, el problema que resuelve, su ubicación, y facilitar el contacto con potenciales usuarios.


* **Sección Inicio**


* **Sección Beneficios**


* **Sección Problema**


* **Sección Testimonio**


* **Sección Contacto**


* **Sección Descarga**


Figma: [Enlace Figma]()

<br>

