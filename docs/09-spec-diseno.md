# spec-de-diseno — Piedra Viva

> Guía: spec-diseno(../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)
> wireframes: [whimsical](https://whimsical.com/D9Vd9M9G6Kk8N7T5J4V2a)

## especificaciones de diseño

version: alpha
name: Piedra Viva
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
  success: "#2F7A4A"
  error: "#B23A2E"
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
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
  button-secondary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  button-secondary-hover:
    backgroundColor: "{colors.tertiary-hover}"
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
---

## Overview

Piedra Viva es una empresa especializada en la instalación y pulido de baldosas con acabados de alta durabilidad, además de la distribución de baldosas Budnik[cite: 2, 4]. Su usuario principal es Renata, una cliente que valora la transparencia en los costos, busca evitar trabajos defectuosos y requiere terminaciones pulcras y de alta gama en sus espacios[cite: 2, 13]. La personalidad visual es sólida, natural, técnica y confiable[cite: 4, 13].

## Colors

- **Primary (`#989B85`):** Verde Oliva Cemento. Utilizado en acciones principales, navegación destacada y elementos gráficos centrales[cite: 4].
- **Secondary (`#EDC3A0`):** Champán / Arcilla Clara. Utilizado para fondos de tarjetas, contenedores secundarios y bordes suaves[cite: 4].
- **Tertiary (`#C48A54`):** Dorado Cantera. Color de acento para distintivos de garantía, botones de llamada a la acción y etiquetas[cite: 4].
- **Neutral (`#FBF1EA`):** Marfil Baldosa. Fondo general para evitar la frialdad del blanco clínico[cite: 4].
- **On-Surface (`#2B2B28`):** Carbón Profundo. Color para texto principal y títulos, garantizando alto contraste[cite: 4].

## Typography

- **Títulos (Headings):** `Merriweather` (Google Fonts). Otorga elegancia, solidez y un carácter institucional refinado[cite: 4].
- **Texto en Cuerpo y Controles (Body/Labels):** `Arimo` (Google Fonts). Otorga excelente legibilidad técnica en dispositivos móviles y de escritorio[cite: 4].

## Layout

- **Ancho máximo de contenedor:** 1200px centrado.
- **Breakpoints:**
  - **Mobile:** < 768px (1 columna, navegación desplegable tipo hamburguesa).
  - **Tablet:** 768px - 1023px (2 columnas en catálogo).
  - **Desktop:** >= 1024px (Grilla de 3 columnas para catálogo y tarjetas).

## Elevation & Depth

- **Superficies planas:** Tarjetas con borde delgado de 1px en `#EDC3A0`[cite: 4].
- **Elevación ligera (Hover):** Sombra suave `0px 4px 12px rgba(0, 0, 0, 0.08)` al pasar sobre tarjetas y botones principales.

## Shapes

- **Botones e Inputs:** Radio moderado de `8px` (`rounded.md`) para transmitir estructura y precisión geométrica.
- **Etiquetas de Estado:** Radio redondeado de `9999px` (`rounded.full`).

## Components

### Card de Producto (`card-product`)
- Contiene imagen cuadrada del producto, nombre en `headline-sm`, especificación ($m^2$), precio por unidad y botón "Cotizar este material" (`button-secondary`).
- **Comportamiento Hover:** Elevación con sombra suave y escalado sutil de la imagen al 102%.

### Botón Principal (`button-primary`)
- Fondo `#989B85`, texto `#2B2B28`[cite: 4].
- Usado en los formularios de cotización y llamadas a la acción principales de la Landing Page[cite: 4].

## Do's and Don'ts

- **Do:** Mantener siempre el fondo `#FBF1EA` para evitar contrastes agresivos sobre blanco puro[cite: 4].
- **Do:** Usar texto en color Carbón `#2B2B28` sobre los botones de color Verde Oliva `#989B85` para asegurar contraste accesibilidad WCAG AA[cite: 4].
- **Don't:** No aplicar textos blancos sobre botones primarios o secundarios ya que incumplen el ratio de contraste.
- **Don't:** No utilizar más de dos familias tipográficas.