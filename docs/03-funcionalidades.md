# Objetivos del usuario y funcionalidades — Piedra Viva

> Guía: [Objetivos del usuario y funcionalidades](../evaluacion/guias/fase-1-requerimientos/03-funcionalidades.md)


## Objetivos de la Proto-persona (Renata) en el Sitio

Al ingresar al sitio web de **Piedra Viva**, Renata busca resolver de forma rápida e integral la compra e instalación de baldosas Budnik para sus proyectos arquitectónicos. Sus metas principales son:

1. **Cotizar de forma integral y rápida:** Obtener un presupuesto centralizado que combine el suministro de baldosas Budnik con la mano de obra de instalación y pulido.
2. **Validar especificaciones técnicas y estética:** Consultar fichas técnicas y guías de uso para asegurar la resistencia al tráfico y acabado idóneo según la obra (interior/exterior).
3. **Resguardar la carta Gantt de la obra:** Verificar stock disponible en tiempo real y agendar fechas preliminares de instalación para cumplir con sus plazos de entrega.
4. **Recibir asesoría especializada sin intermediarios:** Resolver dudas de alta complejidad técnica comentando artículos o adjuntando planos y fotografías de la obra.

---

## Listado de Funcionalidades

### Funcionalidades Base (7)

1. **Landing (Captación de leads):** Formulario para ingresar datos de contacto (nombre, WhatsApp, email), m² y comuna para solicitar una cotización integral (material Budnik + instalación + pulido).
2. **Blog (Categorías técnicas):** Navegación de artículos filtrados por uso técnico (pisos interiores, exteriores, alto tráfico, restauración y vitrificado).
3. **Blog (Comentarios):** Sección de comentarios en artículos para resolver dudas sobre procesos de fraguado, nivelación o mantención con especialistas.
4. **Blog (Compartir):** Botones para compartir guías técnicas y artículos vía WhatsApp y correo electrónico con clientes o equipos de trabajo.
5. **E-commerce (Búsqueda):** Motor de búsqueda por nombre de modelo, tipo de acabado o complemento (ej. "micro vibrada", "rústica", "guardapolvo").
6. **E-commerce (Filtros):** Filtros dinámicos según tipo de producto (baldosas, guardapolvos), uso (interior/exterior) y resistencia al tráfico (residencial, comercial).
7. **E-commerce (Ficha de Producto y Carrito):** Ficha técnica detallada con selección de variante (formato/color), calculadora de metros cuadrados y botón para agregar al carro de compras.

### Funcionalidades Propias - Piedra Viva (5)

1. **Calculadora de Proyecto Integral (Propia 1):** Herramienta interactiva para simular el costo estimado del servicio completo (material Budnik + mano de obra de instalación y pulido) antes de enviar la solicitud formal.
2. **Agendamiento de Fecha de Obra (Propia 2):** Calendario interactivo para agendar una fecha tentativa de inicio de instalación al momento de confirmar el pedido de baldosas.
3. **Solicitud de Muestras Físicas (Propia 3):** Módulo para solicitar a domicilio un kit de muestras de baldosas para evaluar tonos y texturas en terreno.
4. **Verificación de Stock en Tiempo Real (Propia 4):** Indicador en vivo de la disponibilidad de stock por modelo para evitar desfases en los tiempos de la obra.
5. **Asesoría Técnica con Archivos Adjuntos (Propia 5):** Formulario directo que permite adjuntar planos de arquitectura (PDF/CAD) o fotografías del estado actual del piso para recibir una evaluación experta.

---

## Matriz de Requerimientos (Proto-persona / Objetivo / Funcionalidad)

| Proto-persona | Objetivo del Usuario | Funcionalidad del Sistema | Tipo | Prioridad |
|---|---|---|---|---|
| Renata | Obtener un presupuesto unificado rápido sin coordinar proveedores por separado | Formulario de cotización integral en Landing (datos, m² y comuna para propuesta de material + instalación + pulido) | Base (Landing) | Imprescindible |
| Renata | Consultar guías y normativas según la tipología de su proyecto | Navegación de artículos por categorías técnicas (interiores, exteriores, alto tráfico, restauración) | Base (Blog) | Imprescindible |
| Renata | Resolver dudas técnicas específicas sobre procesos de obra | Sistema de comentarios en artículos del blog para consultas directas al equipo técnico | Base (Blog) | Deseable |
| Renata | Enviar especificaciones y guías de mantención a clientes o técnicos de obra | Funcionalidad para compartir artículos por WhatsApp y correo electrónico | Base (Blog) | Deseable |
| Renata | Localizar rápidamente un modelo de baldosa o complemento específico | Buscador predictivo por nombre de modelo, tipo de acabado o complemento | Base (Tienda) | Imprescindible |
| Renata | Seleccionar el material adecuado según exigencias de tráfico y ubicación | Filtros de catálogo por tipo de producto, uso (interior/exterior) y resistencia al tráfico | Base (Tienda) | Imprescindible |
| Renata | Verificar ficha técnica, calcular volumen y armar pedido de material | Ficha técnica detallada, selector de variantes, calculador de m² y carrito de compras | Base (Tienda) | Imprescindible |
| Renata | Estimar el presupuesto total del proyecto antes de realizar la solicitud final | Calculadora interactiva de costo estimado del servicio completo (material + mano de obra) | Propia (Propia 1) | Imprescindible |
| Renata | Reservar la fecha de inicio de trabajos para resguardar la carta Gantt de la obra | Módulo de agendamiento de fecha tentativa de inicio de obra al confirmar el pedido | Propia (Propia 2) | Imprescindible |
| Renata | Validar calidad, tono y textura del material físicamente en terreno | Módulo de solicitud a domicilio de kit de muestras físicas de baldosas | Propia (Propia 3) | Deseable |
| Renata | Confirmar disponibilidad inmediata del material para evitar retrasos | Indicador de verificación de disponibilidad de stock en tiempo real | Propia (Propia 4) | Imprescindible |
| Renata | Obtener recomendación experta enviando documentación o fotografías del espacio | Formulario de asesoría técnica personalizada con opción de adjuntar planos o fotos | Propia (Propia 5) | Deseable |