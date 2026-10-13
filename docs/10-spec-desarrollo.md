# Spec de desarrollo — Piedra Viva

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

**Tablero de Wireframes en Whimsical:** [https://whimsical.com/alejandra82/mi-moodboard-JnQcL4AimPEMDqCA5r2xeA](https://whimsical.com/alejandra82/mi-moodboard-JnQcL4AimPEMDqCA5r2xeA)

![Wireframes de Piedra Viva](img/wireframes.png)

## Prompts para Generación de Pantallas (Stitch / IA)

### Prompt 1: Landing Page (Inicio) — Versión Desktop
> **Pantalla:** Landing Page, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Transmitir confianza inmediata a Renata sobre la calidad en instalación, pulido de baldosas y distribución Budnik, permitiéndole solicitar un presupuesto transparente sin sorpresas de costos.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Logo "Piedra Viva", enlaces de navegación ("Inicio", "Servicios", "Catálogo Budnik", "Galería", "Blog", "Contacto") y botón destacado "Cotizar Ahora" (`button-primary`).
> 2. **Hero:** Título h1 "Pisos impecables que transforman tus espacios", bajada explicativa sobre instalación y pulido de baldosas de alta durabilidad, botón principal "Solicitar Cotización" (`button-primary`) e imagen destacada de piso vitrificado de alto brillo.
> 3. **Sección de Misión y Valores:** Bloque informativo con fondo `#EDC3A0` sobre la precisión técnica y compromiso de trabajo garantizado sin cobros ocultos.
> 4. **Galería de Proyectos Destacados:** Grilla de 3 columnas mostrando fotografías comparativas de acabados en terrazas y salones.
> 5. **Formulario de Cotización Guiada:** Campos de entrada "Nombre", "Correo", "Teléfono", "Metros cuadrados (m²)" y selector de servicio ("Pulido de Pisos", "Instalación", "Compra de Baldosa Budnik"), con botón de envío (`button-primary`).
> 6. **Footer:** Enlaces institucionales, garantías del servicio, contacto directo y redes sociales.

### Prompt 2: Tienda / Catálogo Budnik — Versión Desktop
> **Pantalla:** Tienda / Catálogo, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Permitir a los clientes explorar las líneas de baldosas Budnik y filtrar por tipo de uso (interior/exterior) o acabado.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Mismo componente global de navegación.
> 2. **Encabezado:** Título h1 "Catálogo de Baldosas Budnik" y buscador "Buscar por modelo o tipo de baldosa...".
> 3. **Filtros por Categoría:** Botones de selección rápida (Todos, Microvibradas, Rústicas, Terrazos, Formatos Especiales).
> 4. **Contenido Principal (Layout 2 Columnas):**
>    - **Barra Lateral Izquierda (Filtros):** Casillas de verificación para Uso ("Interior", "Exterior", "Alto Tráfico") y rango de precios.
>    - **Grilla Derecha (3 Columnas):** 6 tarjetas de producto (`card-product`) con foto del producto, nombre (ej: "Baldosa Microvibrada Gris 40x40"), precio por m² "$12.990", distintivo de disponibilidad y botón "Cotizar este material".
> 5. **Footer:** Mismo componente global.

### Prompt 3: Ficha de Producto — Versión Desktop
> **Pantalla:** Ficha de Producto, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Mostrar los detalles técnicos y especificaciones de la baldosa seleccionada para validar su resistencia y durabilidad.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Mismo componente global.
> 2. **Vista de Producto (2 Columnas):**
>    - **Columna Izquierda:** Fotografía principal de alta resolución de la baldosa "Microvibrada Rústica 40x40" y galería de miniaturas de proyectos aplicados.
>    - **Columna Derecha:** Título h1 "Baldosa Microvibrada Rústica 40x40", precio por m² "$12.990", selector de cantidad de metros cuadrados, resumen técnico (Resistencia al impacto, Uso recomendado para terrazas), y botón principal "Añadir a Cotización" (`button-primary`).
> 3. **Sección Complementaria:** Fila con 3 tarjetas de productos recomendados o materiales de fragüe compatibles.
> 4. **Footer:** Mismo componente global.

### Prompt 4: Carrito / Resumen de Cotización — Versión Desktop
> **Pantalla:** Carrito / Cotización, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Revisar los materiales seleccionados y obtener un cálculo transparente de costos de envío antes de enviar la solicitud final.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Mismo componente global.
> 2. **Encabezado:** Título h1 "Resumen de Cotización".
> 3. **Layout de 2 Columnas:**
>    - **Columna Principal:** Tabla con productos agregados (ej: "40 m² Baldosa Microvibrada"), precio unitario, subtotal y opción para eliminar o modificar cantidades.
>    - **Columna Lateral (Resumen de Costos):** Calculadora aproximada de despacho según comuna seleccionada, desglose del subtotal y botón destacado "Enviar Cotización por WhatsApp" (`button-secondary`).
> 4. **Footer:** Mismo componente global.

### Prompt 5: Blog — Versión Desktop
> **Pantalla:** Blog de Mantención y Consejos, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Educar a los clientes sobre cómo cuidar y mantener el pulido de sus pisos para proteger su inversión.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Mismo componente global.
> 2. **Encabezado:** Título h1 "Guías de Cuidado y Mantención de Pisos".
> 3. **Grilla de Artículos (3 Columnas):** Tarjetas de artículos con imagen, categoría ("Pulido", "Instalación", "Cuidado"), título en `headline-sm` (ej: "Cómo mantener el brillo de tus baldosas Budnik por años"), resumen corto y tiempo estimado de lectura.
> 4. **Footer:** Mismo componente global.

### Prompt 6: Artículo del Blog — Versión Desktop
> **Pantalla:** Lectura de Artículo del Blog, versión Desktop. Usa el Design System del proyecto Piedra Viva (`DESIGN.md`).
> **Objetivo:** Brindar una lectura detallada sobre un procedimiento técnico de mantenimiento.
> **Componentes de arriba hacia abajo:**
> 1. **Navbar:** Mismo componente global.
> 2. **Encabezado del Artículo:** Categoría, título h1 "Paso a paso para el vitrificado y pulido de baldosas rústicas" y fecha de publicación.
> 3. **Cuerpo del Texto:** Contenedor de lectura centrado (máximo 800px) con imágenes ilustrativas del proceso de pulido, párrafos descriptivos y recomendaciones de productos.
> 4. **Caja de Acción Final:** Bloque destacado con fondo `#EDC3A0` invitando a cotizar un servicio profesional de pulido con botón (`button-primary`).
> 5. **Footer:** Mismo componente global.

### Prompt Adicional: Adaptación Responsive Mobile (Todas las pantallas)
> **Instrucción de Adaptabilidad Mobile:**
> Aplica las siguientes reglas responsive para todas las pantallas anteriores en dispositivos móviles (< 768px):
> - El Navbar colapsa los enlaces en un menú hamburguesa desplegable superior.
> - Todas las grillas de 3 o 2 columnas pasan a una sola columna vertical.
> - Los botones principales (`button-primary` y `button-secondary`) ocupan el 100% del ancho disponible de la pantalla para facilitar la pulsación táctil.
> - Los tamaños de fuente se ajustan según los tokens móviles de `DESIGN.md` (h1 a 32px, h2 a 24px).

