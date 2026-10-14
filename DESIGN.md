---
version: alpha
name: "Piedra Viva"
description: "Design system de empresa de instalación, pulido de baldosas y distribución Budnik"
# Validar con: npx @google/design.md lint DESIGN.md
colors:
  primary: "#989B85"
  primary-hover: "#838670"
  on-primary: "#2B2B28"
  secondary: "#EDC3A0"
  on-secondary: "#2B2B28"
  tertiary: "#C48A54"
  tertiary-hover: "#B07945"
  on-tertiary: "#FFFFFF"
  quaternary: "#F0A5A8"
  neutral: "#FBF1EA"
  surface: "#FFFFFF"
  on-surface: "#2B2B28"
  on-surface-muted: "#60605C"
  disabled: "#D6D6D6"
  on-disabled: "#9A9A96"
  success: "#2F7A4A"
  error: "#B23A2E"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-secondary-hover:
    backgroundColor: "{colors.tertiary-hover}"
    textColor: "{colors.on-tertiary}"
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-product-hover:
    boxShadow: "0px 4px 12px rgba(0,0,0,0.08)"
    imageScale: 1.02
  tag-disponible:
    backgroundColor: "{colors.success}"
    textColor: "{colors.surface}"
    rounded: "{rounded.full}"
    padding: 4px 12px
  tag-agotado:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
    rounded: "{rounded.full}"
    padding: 4px 12px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
    border: "1px solid {colors.secondary}"
  input-field-focus:
    border: "2px solid {colors.primary}"
    outline: none
  input-field-error:
    border: "2px solid {colors.error}"
  message-error:
    textColor: "{colors.error}"
    typography: "{typography.body-md}"
  message-success:
    textColor: "{colors.success}"
    typography: "{typography.body-md}"
  navbar:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    borderBottom: "1px solid {colors.secondary}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
typography:
  headline-lg:
    fontFamily: Merriweather
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.2
  headline-md:
    fontFamily: Merriweather
    fontSize: 30px
    fontWeight: 700
    lineHeight: 1.3
  headline-sm:
    fontFamily: Merriweather
    fontSize: 20px
    fontWeight: 700
    lineHeight: 1.4
  body-md:
    fontFamily: Arimo
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: Arimo
    fontSize: 16px
    fontWeight: 700
    lineHeight: 1.2
rounded:
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
---

# Piedra Viva — Design System

## Overview

Piedra Viva es una empresa especializada en la instalación y pulido de baldosas con acabados de alta durabilidad, y en la distribución de baldosas Budnik. Su usuario principal es **Renata**, una clienta que valora la transparencia en los costos, busca evitar trabajos defectuosos y requiere terminaciones pulcras y de alta gama en sus espacios. La interfaz debe transmitir una personalidad **sólida, natural, técnica y confiable**.

## Colors

- **Primary (`#989B85`):** Verde Oliva Cemento. Botones principales (CTA), fondo de navbar activa, íconos y enlaces destacados. No usar con texto blanco (ratio 3.2:1 insuficiente para texto pequeño).
- **Secondary (`#EDC3A0`):** Champán / Arcilla Clara. Fondos de tarjetas, bloques de información, bordes suaves y separadores. No usar como color de texto.
- **Tertiary (`#C48A54`):** Dorado Cantera. Botones secundarios, etiquetas de garantía y elementos de acento. Usar siempre con texto blanco (`#FFFFFF`).
- **Quaternary (`#F0A5A8`):** Rosa Terracota Soft. Fondos de avisos de apoyo y detalles en promociones especiales. Solo como fondo, nunca como texto.
- **Neutral (`#FBF1EA`):** Marfil Baldosa. Fondo general de todas las páginas. Evita el blanco clínico y transmite calidez de hogar terminado.
- **On-Primary (`#2B2B28`):** Carbón Profundo. Texto sobre botones primarios (ratio 7.2:1 ✅ WCAG AA).
- **On-Surface (`#2B2B28`):** Texto principal en párrafos, títulos y menús (ratio 13.1:1 sobre `#FBF1EA` ✅ WCAG AAA).
- **On-Surface-Muted (`#60605C`):** Gris Calizo. Bajadas, textos secundarios y meta-información (ratio 5.8:1 ✅ WCAG AA).
- **Success (`#2F7A4A`):** Confirmación de cotización enviada.
- **Error (`#B23A2E`):** Alertas de validación en campos obligatorios.

## Typography

- **Títulos (Headings):** `Merriweather` — serif elegante que transmite solidez, tradición y experiencia institucional. Cargada desde Google Fonts.
- **Textos y controles (Body / Labels):** `Arimo` — sans-serif limpia, altamente legible en pantallas móviles y de escritorio. Cargada desde Google Fonts.

### Escala tipográfica

| Token | Familia | Tamaño Desktop | Tamaño Mobile | Peso | Uso |
|---|---|---|---|---|---|
| `headline-lg` | Merriweather | 40px | 32px | 700 | h1 — Títulos Hero y páginas |
| `headline-md` | Merriweather | 30px | 24px | 700 | h2 — Títulos de sección |
| `headline-sm` | Merriweather | 20px | 18px | 700 | h3 — Subtítulos de tarjetas |
| `body-md` | Arimo | 16px | 16px | 400 | Párrafos, guías, artículos |
| `label-md` | Arimo | 16px | 16px | 700 | Botones e inputs |

## Layout

- **Ancho máximo del contenedor:** 1200px, centrado con `margin: 0 auto`.
- **Breakpoints:**
  - **Mobile:** < 768px — 1 columna, navegación hamburguesa, botones a ancho completo.
  - **Tablet:** 768px–1023px — 2 columnas en catálogo y galería.
  - **Desktop:** ≥ 1024px — grilla de 3 columnas para catálogo, tarjetas y galería.
- **Espaciado de sección:** `spacing.3xl` (64px) entre secciones en desktop; `spacing.2xl` (48px) en mobile.
- **Márgenes laterales:** `spacing.xl` (32px) en desktop; `spacing.md` (16px) en mobile.

## Elevation & Depth

- **Superficies planas (reposo):** Tarjetas con borde `1px solid #EDC3A0`. Sin sombra.
- **Elevación ligera (hover):** Sombra suave `0px 4px 12px rgba(0, 0, 0, 0.08)` sobre tarjetas y botones principales.
- **Navbar fija:** Borde inferior `1px solid #EDC3A0` sobre fondo blanco para separar del contenido.
- **No usar** sombras grandes o contrastes fuertes de profundidad; la marca es técnica y limpia.

## Shapes

- **Botones e Inputs:** Radio de `8px` (`rounded.md`) — transmite estructura y precisión geométrica.
- **Etiquetas de estado (tags):** Radio de `9999px` (`rounded.full`) — diferencia visualmente los estados de disponibilidad.
- **Tarjetas:** Radio de `8px` (`rounded.md`).
- **No usar** bordes completamente cuadrados (0px) ni bordes excesivamente redondeados en botones (>16px).

## Components

### Navbar (`navbar`)
Contiene: logo "Piedra Viva" a la izquierda, enlaces de navegación centrados ("Inicio", "Servicios", "Catálogo Budnik", "Galería", "Blog", "Contacto") y botón `button-primary` "Cotizar Ahora" a la derecha.
- **Estado desktop:** Horizontal, borde inferior `1px solid #EDC3A0`, `position: sticky top: 0`.
- **Estado mobile:** Los enlaces colapsan en menú hamburguesa desplegable. Botón "Cotizar Ahora" se mueve al interior del menú.

### Botón Principal (`button-primary`)
- **Reposo:** Fondo `#989B85`, texto `#2B2B28`, radio `8px`, padding `12px 24px`.
- **Hover:** Fondo `#838670`, texto `#2B2B28`, transición `background-color 0.2s ease`.
- **Deshabilitado:** Fondo `#D6D6D6`, texto `#9A9A96`, cursor `not-allowed`.
- Usado en: formulario de cotización, Hero CTA, caja de acción del artículo de blog.

### Botón Secundario (`button-secondary`)
- **Reposo:** Fondo `#C48A54`, texto `#FFFFFF`, radio `8px`, padding `12px 24px`.
- **Hover:** Fondo `#B07945`, texto `#FFFFFF`, transición `background-color 0.2s ease`.
- Usado en: tarjeta de producto "Cotizar este material", carrito "Enviar Cotización por WhatsApp".

### Card de Producto (`card-product`)
Contiene: imagen cuadrada del producto, nombre en `headline-sm`, especificación (m²), precio por unidad, tag de disponibilidad y botón `button-secondary` "Cotizar este material".
- **Reposo:** Fondo `#FFFFFF`, borde `1px solid #EDC3A0`, radio `8px`, padding `16px`.
- **Hover:** Sombra `0px 4px 12px rgba(0,0,0,0.08)`, imagen escala al 102% con `transition: transform 0.3s ease`.

### Tag de Estado (`tag-disponible` / `tag-agotado`)
- **Disponible:** Fondo `#2F7A4A`, texto `#FFFFFF`, radio `9999px`, padding `4px 12px`.
- **Agotado:** Fondo `#D6D6D6`, texto `#9A9A96`, radio `9999px`, padding `4px 12px`.

### Input de Formulario (`input-field`)
- **Reposo:** Fondo `#FFFFFF`, borde `1px solid #EDC3A0`, radio `8px`, padding `12px 14px`, fuente Arimo 16px.
- **Focus:** Borde `2px solid #989B85`, sin outline adicional.
- **Error:** Borde `2px solid #B23A2E` + mensaje de error en texto `#B23A2E` bajo el campo.
- **Éxito:** Borde `2px solid #2F7A4A`.

### Card de Artículo de Blog
Contiene: imagen de portada, etiqueta de categoría ("Pulido", "Instalación", "Cuidado"), título en `headline-sm`, resumen corto en `body-md` y tiempo estimado de lectura en `on-surface-muted`.
- Misma base que `card-product` con comportamiento hover idéntico.

## Do's and Don'ts

**Do:**
- Mantener siempre el fondo `#FBF1EA` para evitar contrastes agresivos sobre blanco puro.
- Usar texto `#2B2B28` (Carbón) sobre botones `#989B85` (Verde Oliva) para asegurar WCAG AA (ratio 7.2:1).
- Usar texto `#FFFFFF` sobre el botón Dorado Cantera `#C48A54` (ratio 3.1:1 — solo en tamaños ≥ 18px Bold o 24px Normal).
- Escalar imágenes de baldosas con `object-fit: cover` para mantener proporción cuadrada.

**Don't:**
- No aplicar texto blanco `#FFFFFF` sobre el botón primario `#989B85` (ratio insuficiente 3.2:1 para texto pequeño).
- No usar más de dos familias tipográficas (Merriweather + Arimo).
- No usar sombras fuertes ni superposiciones oscuras; la identidad es natural y técnica, no dramática.
- No aplicar el color `#F0A5A8` (Rosa Terracota) en elementos interactivos principales; es solo de apoyo.
