# Matriz de requisitos, usuarios y pantallas — CaféU

## Usuarios
| Usuario | Rol | Necesidades |
|---|---|---|
| Estudiante | Principal: realiza el pedido desde su teléfono | Pedir rápido y con una mano; no explicar el pedido en voz alta; corregir errores antes de enviar; saber que el pedido fue recibido |
| Personal de cafetería | Secundario: recibe y entrega el pedido | Identificar el pedido sin conversar; cobrar el monto correcto al entregar |

## Requisitos
| ID | Requisito |
|---|---|
| RF-01 | Mostrar el menú del día por categorías, con nombre, precio y disponibilidad. |
| RF-02 | Elegir un producto y su cantidad con controles de toque, sin escribir ni hablar. |
| RF-03 | Presentar un resumen del pedido con productos, cantidades, precios y total. |
| RF-04 | Editar el pedido, recalcular el total y guardar o cancelar sin perder el original. |
| RF-05 | Acción principal única «Confirmar pedido» e información si el envío falla. |
| RF-06 | Confirmación con mensaje de éxito, número de pedido, resumen e instrucción de retiro y pago. |
| RNF-01 | Tarea principal en máximo cinco vistas y con una sola mano. |
| RNF-02 | Controles táctiles de al menos 24 × 24 px CSS (WCAG 2.2, 2.5.8) y número de pedido legible. |
| RNF-03 | Informar antes y después de confirmar que el pago se hace al retirar. |

## Matriz
| Funcionalidad principal | Requisitos | Usuario | Necesidad | Pantallas |
|---|---|---|---|---|
| F1. Consultar el menú y elegir productos | RF-01, RF-02, RNF-01, RNF-02 | Estudiante | Encontrar rápido qué hay y cuánto cuesta, y agregarlo sin hablar | 1.0 Menú de hoy, 1.1 Detalle del producto |
| F2. Revisar y editar el pedido | RF-03, RF-04, RNF-03 | Estudiante | Verificar y corregir el pedido sin perder lo elegido | 2.0 Revisa tu pedido, 2.1 Editar pedido |
| F3. Confirmar y recibir la confirmación | RF-05, RF-06, RNF-02, RNF-03 | Estudiante y personal de cafetería | Saber que el pedido fue recibido e identificarlo al retirar y cobrar | 2.0 Revisa tu pedido (acción), 3.0 Pedido confirmado |
