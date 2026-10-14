# Spec de Desarrollo — Piedra Viva

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

---

## Insumos

**Tablero de Wireframes en Whimsical:** [https://whimsical.com/alejandra82/mi-moodboard-JnQcL4AimPEMDqCA5r2xeA](https://whimsical.com/alejandra82/mi-moodboard-JnQcL4AimPEMDqCA5r2xeA)

![Wireframes de Piedra Viva](img/wireframes.png)

---

## Estructura de Archivos

```
mi-emprendimiento/
├── DESIGN.md                     # Design system (fuente de verdad de tokens y componentes)
├── README.md
├── index.html                    # Landing Page (Inicio)
├── catalogo.html                 # Tienda / Catálogo Budnik
├── producto.html                 # Ficha de Producto
├── cotizacion.html               # Carrito / Resumen de Cotización
├── blog.html                     # Listado del Blog
├── articulo.html                 # Lectura de Artículo del Blog
├── css/
│   ├── tokens.css                # Variables CSS (colores, tipografía, espaciado, radios)
│   ├── base.css                  # Reset, body, tipografía base, Google Fonts import
│   ├── layout.css                # Grid, contenedor máximo, breakpoints responsive
│   ├── components.css            # Navbar, botones, cards, inputs, tags, footer
│   └── pages/
│       ├── home.css              # Estilos exclusivos del Hero y secciones de index.html
│       ├── catalogo.css          # Estilos del catálogo y barra de filtros lateral
│       ├── producto.css          # Estilos de la ficha de producto y galería de miniaturas
│       ├── cotizacion.css        # Estilos de la tabla del carrito y panel de resumen
│       └── blog.css              # Estilos de la grilla de artículos y cuerpo de lectura
├── js/
│   ├── navbar.js                 # Toggle menú hamburguesa (mobile)
│   ├── filtros.js                # Filtros del catálogo (categoría y checkboxes)
│   ├── cotizacion.js             # Lógica del carrito: agregar, eliminar, calcular total
│   └── formulario.js             # Validación del formulario de cotización guiada
├── img/
│   ├── logo.svg
│   ├── hero-piso.jpg
│   ├── productos/                # Fotos de baldosas Budnik
│   ├── galeria/                  # Fotos comparativas de proyectos
│   └── blog/                     # Imágenes de artículos
└── docs/
    └── ...                       # Documentación del proyecto
```

---

## Tabla de Navegación

| Página | Archivo | URL | Acceso desde |
|---|---|---|---|
| Landing Page (Inicio) | `index.html` | `/` | Navbar → "Inicio", Logo |
| Catálogo Budnik | `catalogo.html` | `/catalogo.html` | Navbar → "Catálogo Budnik" |
| Ficha de Producto | `producto.html` | `/producto.html` | Click en `card-product` del catálogo |
| Resumen de Cotización | `cotizacion.html` | `/cotizacion.html` | Botón "Añadir a Cotización" en ficha de producto |
| Blog | `blog.html` | `/blog.html` | Navbar → "Blog" |
| Artículo del Blog | `articulo.html` | `/articulo.html` | Click en tarjeta de artículo del blog |

> **Nota:** La navegación global (Navbar y Footer) se replica manualmente en cada `.html`. No se usa framework ni SSR.

---

## Estructura Semántica HTML

Cada página sigue la misma estructura semántica base:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="[Descripción única por página]">
  <title>[Título de página] — Piedra Viva</title>
  <link rel="stylesheet" href="css/tokens.css">
  <link rel="stylesheet" href="css/base.css">
  <link rel="stylesheet" href="css/layout.css">
  <link rel="stylesheet" href="css/components.css">
  <link rel="stylesheet" href="css/pages/[pagina].css">
</head>
<body>

  <header role="banner">
    <nav aria-label="Navegación principal" id="navbar">
      <!-- Logo + links + botón CTA -->
    </nav>
  </header>

  <main id="main-content">
    <!-- Contenido único por página con un solo <h1> -->
  </main>

  <footer role="contentinfo">
    <!-- Links institucionales, contacto, redes -->
  </footer>

  <script src="js/navbar.js"></script>
  <!-- Scripts adicionales según la página -->
</body>
</html>
```

### Elementos semánticos por pantalla

| Página | `<h1>` | Secciones semánticas principales |
|---|---|---|
| Landing Page | "Pisos impecables que transforman tus espacios" | `<section>` Hero, `<section>` Valores, `<section>` Galería, `<section>` Formulario |
| Catálogo | "Catálogo de Baldosas Budnik" | `<aside>` Filtros, `<section>` Grilla de productos |
| Ficha de Producto | "Baldosa Microvibrada Rústica 40x40" | `<article>` Detalle del producto, `<section>` Productos relacionados |
| Cotización | "Resumen de Cotización" | `<section>` Tabla de productos, `<aside>` Panel de costos |
| Blog | "Guías de Cuidado y Mantención de Pisos" | `<section>` Grilla de artículos |
| Artículo del Blog | "Paso a paso para el vitrificado y pulido..." | `<article>` Cuerpo del artículo, `<section>` CTA final |

---

## Organización del CSS

El CSS se divide en **capas** de mayor a menor especificidad, importadas en orden:

### 1. `tokens.css` — Variables globales
```css
:root {
  /* Colores */
  --color-primary: #989B85;
  --color-primary-hover: #838670;
  --color-on-primary: #2B2B28;
  --color-secondary: #EDC3A0;
  --color-tertiary: #C48A54;
  --color-on-tertiary: #FFFFFF;
  --color-neutral: #FBF1EA;
  --color-surface: #FFFFFF;
  --color-on-surface: #2B2B28;
  --color-on-surface-muted: #60605C;
  --color-error: #B23A2E;
  --color-success: #2F7A4A;

  /* Tipografía */
  --font-heading: 'Merriweather', serif;
  --font-body: 'Arimo', sans-serif;
  --text-headline-lg: 2.5rem;    /* 40px desktop */
  --text-headline-md: 1.875rem;  /* 30px desktop */
  --text-headline-sm: 1.25rem;   /* 20px desktop */
  --text-body: 1rem;

  /* Espaciado */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;
}
```

### 2. `base.css` — Reset y estilos globales
- Import de Google Fonts (Merriweather + Arimo).
- Reset box-sizing, margin y padding a 0.
- `body`: `background-color: var(--color-neutral)`, `color: var(--color-on-surface)`, `font-family: var(--font-body)`.
- Estilos base de `h1`–`h3` con `font-family: var(--font-heading)`.

### 3. `layout.css` — Contenedor y grid
- `.container`: `max-width: 1200px; margin: 0 auto; padding: 0 var(--space-xl)`.
- `.grid-3`: `display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-lg)`.
- `.grid-2`: `display: grid; grid-template-columns: repeat(2, 1fr); gap: var(--space-lg)`.
- Media queries: tablet (`@media (max-width: 1023px)`) y mobile (`@media (max-width: 767px)`).

### 4. `components.css` — Componentes reutilizables
- `.navbar`, `.btn-primary`, `.btn-secondary`, `.card-product`, `.input-field`, `.tag`, `.footer`.
- Cada componente incluye sus estados (`:hover`, `:focus`, `:disabled`, `.error`).

### 5. `pages/[pagina].css` — Estilos exclusivos por página
- Solo sobreescrituras o extensiones necesarias para esa pantalla en particular.
- No debe contener tokens ni componentes genéricos.

---

## Criterios de Aceptación

### Navegación y estructura
- [ ] El Navbar es visible y funcional en todas las páginas.
- [ ] El menú hamburguesa se despliega correctamente en mobile (< 768px).
- [ ] Cada página tiene exactamente un `<h1>` con el título principal de la pantalla.
- [ ] Todos los `<a>` de navegación tienen texto descriptivo (no "click aquí").

### Diseño y tokens
- [ ] Todos los colores, tipografías, radios y espaciados usan variables CSS de `tokens.css`.
- [ ] El fondo general de todas las páginas es `#FBF1EA` (Marfil Baldosa).
- [ ] No se usa texto blanco sobre el botón primario `#989B85`.
- [ ] Los botones `button-primary` cambian a `#838670` en `:hover`.
- [ ] Los `card-product` muestran sombra y la imagen escala al 102% en `:hover`.

### Responsive
- [ ] En mobile (< 768px), todas las grillas de 2 y 3 columnas colapsan a 1 columna.
- [ ] En mobile, los botones `button-primary` y `button-secondary` ocupan el 100% del ancho.
- [ ] Los tamaños de fuente del h1 pasan de 40px (desktop) a 32px (mobile).
- [ ] Los tamaños de fuente del h2 pasan de 30px (desktop) a 24px (mobile).

### Formulario de cotización (Landing Page)
- [ ] Los campos "Nombre", "Correo", "Teléfono" y "Metros cuadrados" son obligatorios.
- [ ] Si se envía vacío, aparece un mensaje de error en rojo `#B23A2E` bajo cada campo inválido.
- [ ] El borde del input cambia a `2px solid #B23A2E` en estado de error.
- [ ] Al enviarse correctamente, se muestra un mensaje de confirmación en verde `#2F7A4A`.

### Catálogo y filtros
- [ ] Los filtros de categoría (Microvibradas, Rústicas, etc.) filtran las tarjetas visibles.
- [ ] Los checkboxes de uso (Interior, Exterior, Alto Tráfico) filtran en combinación con la categoría.
- [ ] El buscador filtra las tarjetas por nombre o tipo en tiempo real.
- [ ] Cada `card-product` muestra nombre, precio, tag de disponibilidad y botón "Cotizar este material".

### Carrito / Cotización
- [ ] El total del carrito se recalcula automáticamente al modificar la cantidad de m².
- [ ] El botón "Enviar Cotización por WhatsApp" abre WhatsApp con el resumen pre-llenado.
- [ ] Se puede eliminar cualquier ítem de la tabla de productos.

### Accesibilidad
- [ ] Ratio de contraste WCAG AA en todos los textos principales (mínimo 4.5:1).
- [ ] Todos los inputs tienen `<label>` asociado con `for` correspondiente.
- [ ] Las imágenes tienen atributo `alt` descriptivo.
- [ ] El menú hamburguesa tiene atributos `aria-expanded` y `aria-controls`.
- [ ] El orden de tabulación (Tab) es lógico y sigue el flujo visual de la página.
