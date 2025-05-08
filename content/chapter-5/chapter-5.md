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


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2. Information Architecture</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.1. Organization Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.2. Labelling Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.3. SEO Tags and Meta Tags</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.4. Searching Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.2.5. Navigation Systems</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3. Landing Page UI Design</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.1. Landing Page Wireframe</a></h3></il>


<il><h3><a href="./content/chapter-5/chapter-5.md">5.1.3.2. Landing Page Mock-up</a></h3></il>




