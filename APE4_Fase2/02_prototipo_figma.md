# Prototipo navegable en Figma — CaféU (APE 4, Fase 2)

**Archivo:** https://www.figma.com/design/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-6
Página: «APE4 Fase 2 · Prototipo navegable». Fila superior: **v2** (corregida, final). Fila inferior: **v1** (versión probada).

## Flujos (puntos de inicio)
| Flujo | Pantallas | Enlace |
|---|---|---|
| v2 · Recorrido 1 – Realizar un pedido | 01 → 02 → 03 → 04 → 05 → 06 → 07 (1500 ms) → 08 | [Abrir](https://www.figma.com/proto/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-232&page-id=33%3A6&starting-point-node-id=33%3A232&scaling=scale-down) |
| v2 · Recorrido 2 – Editar el pedido | 06 → 09 → 10 → 12 → 13 (1500 ms) → 14 | [Abrir](https://www.figma.com/proto/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-497&page-id=33%3A6&starting-point-node-id=33%3A497&scaling=scale-down) |
| v2 · Caso de error – Envío fallido | 15 → 16 (1500 ms) → 17 → «Reintentar envío» → 07 → 08 | [Abrir](https://www.figma.com/proto/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-875&page-id=33%3A6&starting-point-node-id=33%3A875&scaling=scale-down) |
| v1 · Recorrido 1 (versión probada) | 01 → … → 08 | [Abrir](https://www.figma.com/proto/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-1036&page-id=33%3A6&starting-point-node-id=33%3A1036&scaling=scale-down) |
| v1 · Recorrido 2 (versión probada) | 06 → … → 14 | Desde el menú de flujos del modo presentación |

Validación adicional: 10 → «Quitar» café → 11 (pedido vacío) → «Deshacer» → 10.

## Datos del prototipo (v2)
- 17 pantallas de 375 × 812 px con Auto Layout.
- 38 conexiones de navegación (3 avances automáticos «Tras pausa» de 1500 ms).
- 9 conjuntos de componentes con 24 variantes + botón de texto.
- 16 estilos de color y 10 estilos de texto (Inter).
- Microinteracciones: chips y selector de cantidad («Cambiar a»), animación inteligente al agregar, deslizamiento en la navegación, indicador «Paso n de 3» y estado de envío.

## Controles configurados
| Control | Ejemplos |
|---|---|
| Botones | «Agregar al pedido», «Ver pedido», «Confirmar pedido», «Guardar cambios» |
| Menús | Chips Todo / Bebidas / Comida, encabezado |
| Enlaces | «Quitar», «Deshacer», «Ir al menú» |
| Regreso | «‹ Menú», «‹ Mi pedido», «Volver al menú» |
| Cancelación | «Cancelar (sin guardar)» |
| Confirmación | «Confirmar pedido · $4,25», «Reintentar envío» |
