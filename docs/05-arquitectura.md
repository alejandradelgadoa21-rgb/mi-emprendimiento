# Arquitectura de la información — Piedra Viva

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## 1) Mapa de sitio (jerárquico y completo)

```text
Inicio (Landing)
├── Tienda
│   ├── Listado / Catálogo (filtro y búsqueda)
│   │   └── Ficha de producto
│   │       └── Ficha + Cotizar (CTA a agregar al carrito)
│   └── Carrito / Resumen
├── Blog
│   └── Artículo del blog (con links a productos recomendados)
├── Contacto (o Cotizar / Solicitar información)
├── Preguntas Frecuentes
├── Términos y Condiciones
├── Políticas de Privacidad
└── 404 (Página no encontrada)

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra
Escenario inicial:
Instagram (post / anuncio) sobre departamento con baldosas Budnik pulidas
   ↓ (acción)
[Clic: "Ver Catálogo y Cotizar"]
   ↓ (navegación)
[Landing]
   ↓ (acción)
[Clic: "Ir a Tienda"]
   ↓
[Tienda / Catálogo]
   ↓ (acción)
[Filtra / selecciona: Uso = Interior, Tráfico = Alto]
   ↓
[Lista de resultados]
   ↓ (decisión)
¿Encuentra producto recomendado?
   ├─ Sí →
   │   ↓ (acción)
   │   [Abre Ficha de producto]
   │   ↓
   │   [Ficha de producto: Micro Vibrada Modelo A]
   │   ↓ (acción)
   │   [Ingresa m²]
   │   ↓ (acción)
   │   [Selecciona servicio: Instalación + Pulido]
   │   ↓
   │   [CTA: "Consultar a un especialista por WhatsApp" (si tiene dudas)]
   │   ↓ (decisión)
   │   ¿Tiene dudas con la nivelación del piso?
   │      ├─ Sí → [WhatsApp] → (conversación/consulta)
   │      └─ No → [CTA: "Agregar al carrito"]
   │
   └─ No →
       ↓ (acción)
       [Vuelve a filtros / busca por otro uso o tráfico]
       ↓
       (repite búsqueda hasta encontrar)

   ↓ (acción)
[Carrito]
   ↓ (acción)
[Calcula costo total del proyecto ingresando comuna]
   ↓
[CTA final]
   ├─ "Enviar cotización / WhatsApp"  (si aplica en tu UI)
   └─ "Pagar" (si solo es prototipo visual)
   ↓
Fin: Cotización lista para enviar (o simulación de pago)


### Flujo 2: contenido
Escenario inicial:
Google (búsqueda: "cómo vitrificar y mantener baldosas micro vibradas")
   ↓ (navegación)
[Blog → Artículo: Guía técnica para cuidado y vitrificado]
   ↓ (acción)
[Clic en baldosa recomendada dentro del artículo]
   ↓
[Ficha de producto: Baldosa Rústica de Exterior]
   ↓ (decisión)
¿Desea solicitar cotización en el momento?
   ├─ Sí →
   │   ↓ (acción)
   │   [Ingresa m²]
   │   ↓
   │   [CTA: "Agregar al carrito"]
   │   ↓
   │   [Carrito]
   │   ↓
   │   Fin: cotización lista / flujo de envío
   │
   └─ No →
       ↓ (acción)
       [Deja sus datos en formulario del blog/landing para recibir catálogo PDF]
       ↓
       Fin: Lead captado


Descuento aplicado según formato del pedido:

Decisión: ¿Qué formato compra el cliente?
   ├─ Formato A (por ejemplo: caja / menor volumen)
   │    → Descuento: X%
   │    → Se aplica al subtotal del producto
   │
   ├─ Formato B (por ejemplo: pack / mediano volumen)
   │    → Descuento: Y%
   │    → Se aplica al subtotal del producto
   │
   └─ Formato C (por ejemplo: mayor volumen / proyecto)
        → Descuento: Z%
        → Se aplica al subtotal del producto

(La lógica queda definida en tu calculadora del carrito/prototipo)

---


