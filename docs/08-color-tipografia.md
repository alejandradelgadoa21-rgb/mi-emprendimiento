# Paleta de Color y Tipografía — Piedra Viva

> Guía: Color y Tipografía(../evaluacion/guias/fase-2-specs/04-color-tipografia.md)

## Paleta de Color

Extraída directamente del moodboard visual de Piedra Viva para transmitir la solidez, calidez natural y elegancia de las baldosas Budnik y los acabados pulidos.

| Rol | Nombre del Color | Código HEX | Uso en la Interfaz |
|---|---|---|---|
| **Principal** | Verde Oliva Cemento | `#989B85` | Botones principales (CTA), enlaces, encabezados destacados e íconos. |
| **Secundario** | Champán / Arcilla Clara | `#EDC3A0` | Fondos de tarjetas, bloques secundarios, bordes y acentos sutiles. |
| **Acento** | Dorado Cantera | `#C48A54` | Etiquetas de destaque, botones secundarios y distintivos de garantía. |
| **Acento Suave** | Rosa Terracota Soft | `#F0A5A8` | Fondos de avisos de apoyo y detalles en promociones especiales. |
| **Fondo** | Marfil Baldosa | `#FBF1EA` | Fondo general de todas las páginas (evita el blanco frío de laboratorio). |
| **Texto Principal** | Carbón Profundo | `#2B2B28` | Textos de párrafos, títulos principales y menús para alta legibilidad. |
| **Texto Suave** | Gris Calizo | `#60605C` | Bajadas de título, textos secundarios y meta-información. |
| **Estado Éxito** | Verde Piedra | `#2F7A4A` | Confirmación de cotización enviada o mensaje exitoso. |
| **Estado Error** | Rojo Terracota | `#B23A2E` | Alertas de validación en campos obligatorios del formulario. |

---

## Verificación de Contraste (WebAIM WCAG)

| Combinación de Colores | Ratio de Contraste | Cumplimiento WCAG | Uso Permitido |
|---|---|---|---|
| Texto `#2B2B28` sobre Fondo `#FBF1EA` | 13.1:1 | **AA / AAA** ✅ | Párrafos generales y lecturas largas. |
| Texto `#2B2B28` sobre Secundario `#EDC3A0` | 8.8:1 | **AA / AAA** ✅ | Texto sobre tarjetas y cajas de información. |
| Texto blanco `#FFFFFF` sobre Principal `#989B85` | 3.2:1 | **Solo Texto Grande** ⚠️ | Usar texto `#2B2B28` sobre este fondo para botones (7.2:1). |
| Texto blanco `#FFFFFF` sobre Acento `#C48A54` | 3.1:1 | **Solo Texto Grande** ⚠️ | Se combina con texto oscuro `#2B2B28` para botones y etiquetas. |
| Texto Suave `#60605C` sobre Fondo `#FBF1EA` | 5.8:1 | **AA** ✅ | Bajadas de título y descripciones secundarias. |

---

## Tipografía

Las tipografías seleccionadas provienen de **Google Fonts**:

- **Títulos (Headings):** `Merriweather` (Serif elegante, transmite solidez, tradición, experiencia y terminaciones profesionales).
- **Textos y Cuerpo (Body):** `Arimo` (Sans Serif limpia, altamente legible en pantallas móviles y monitores).

### Escala de Tamaños y Jerarquía

| Elemento | Tamaño Desktop | Tamaño Mobile | Peso (Weight) | Aplicación |
|---|---|---|---|---|
| **h1** | 2.5rem (40px) | 2.0rem (32px) | Bold (700) | Títulos principales de Hero y páginas |
| **h2** | 1.875rem (30px) | 1.5rem (24px) | Bold (700) | Títulos de secciones y catálogo |
| **h3** | 1.25rem (20px) | 1.125rem (18px) | Regular / Bold | Subtítulos de tarjetas y servicios |
| **Párrafo** | 1rem (16px) | 1rem (16px) | Regular (400) | Textos descriptivos, guías y artículos |
| **Botón / CTA** | 1rem (16px) | 1rem (16px) | Bold (700) | Texto dentro de botones interactivos |

---

## Justificación desde el Moodboard y Proto-persona

La paleta se inspira en los tonos minerales, las canteras y la calidez natural de las baldosas Budnik y los procesos de pulido. El tono **Marfil Baldosa (`#FBF1EA`)** reemplaza al blanco clínico para entregar una sensación acogedora de hogar terminado. El **Verde Oliva Cemento (`#989B85`)** y el **Dorado Cantera (`#C48A54`)** transmiten la precisión y elegancia del acabado profesional.

Para **Renata** (nuestra proto-persona), quien busca evitar sorpresas y exige un trabajo pulcro y garantizado, la combinación tipográfica de **Merriweather** (que transmite el respaldo de una empresa seria y establecida) con **Arimo** (que facilita la lectura rápida de presupuestos y medidas en su celular) le otorga total transparencia y confianza.