# Registro de cambios · CaféU

## v3 final · 24/10/2026 (iteración tras la prueba)
| Cambio | Hallazgo | Archivo / elemento |
|---|---|---|
| Pista de rango «Entre las 09:51 y las 17:45» bajo el campo de hora. | H1 | `#hora-hint` |
| Validación al salir del campo (`blur`) y al continuar; mensajes específicos para hora temprana y tardía. | H1 | `validateHora()` |
| Error junto al campo con `aria-invalid` y `aria-describedby`; foco al campo. | H1 | `#hora-error` |
| Enlace «Saltar al contenido» dentro del teléfono. | H2 | `.skip` |
| Foco al `h1` de cada pantalla al navegar (no en la carga inicial). | H2 | `show()` |
| Indicador de foco de 3 px #1E4E8C (7,73:1). | H2 | `:focus-visible` |
| Mensaje de error de envío con causa, «no se cobró nada» y «no se duplicará»; resumen visible; foco al aviso; reintento numerado. | H3 | `#send-error`, `#confirm-btn` |
| Búsqueda sin tildes (`normalize('NFD')`) y por sinónimos (`tags`). | H4 | `norm()`, `PRODUCTS.tags` |
| Estado sin resultados con sugerencias y «Limpiar búsqueda». | H4 | `#empty` |
| Aviso «Deshacer» de 6 s y foco directo al botón. | H5 | `toast()` |

## v3 beta · 21/10/2026 (construcción, versión probada)
- Prototipo en HTML, CSS y JavaScript de un solo archivo, con 7 pantallas: Inicio, Menú de hoy, Detalle, Mi pedido, Hora de retiro (nueva), Revisa y confirma, Pedido confirmado.
- Tres flujos: buscar y agregar (T1), modificar y programar el retiro (T2), confirmar con error y reintento (T3).
- Estados: normal, vacío (pedido y búsqueda), agotado, error de validación, procesando, error de envío, éxito.
- Feedback: aviso al agregar, total que se recalcula, precio en el botón, indicador «Paso n de 4».
- Microinteracciones: animación del contador «Mi pedido (n)» al agregar, spinner y barra de progreso al enviar (respetan `prefers-reduced-motion`).
- Panel del moderador con `?prueba=1` para simular el fallo de red; vista de wireframe con `?vista=wireframe`.

## v2 · Fase 2 (Figma)
Ver `../../APE4_Fase2/`.
