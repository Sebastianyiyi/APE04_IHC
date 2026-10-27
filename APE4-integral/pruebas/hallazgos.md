# Hallazgos de la prueba · CaféU v3

**Responsable:** Mora Beltrán Santiago Sebastián · **Datos de origen:** `resultados.csv` y `../evidencias/registros-observacion/`

## 1. Resumen cuantitativo

| Indicador | v3 beta (22/10) | v3 final (24/10) |
|---|---|---|
| Tareas completadas sin ayuda (S) | 5 de 6 (P01-T2 parcial) | 6 de 6 |
| Tiempo medio T1 / T2 / T3 | 71 s / 107 s / 45 s | 31,5 s / 49 s / 32 s |
| Errores totales | 10 | 1 (recuperado en 5 s) |
| SEQ medio (1–7) | 3,67 | 6,17 |

## 2. Hallazgos priorizados

Severidad de Nielsen: 1 cosmético · 2 menor · 3 mayor · 4 catástrofe.

| ID | Hallazgo | Evidencia (participante · tarea) | Heurística / criterio | Sev. | Recomendación | Estado |
|---|---|---|---|---|---|---|
| **H1** | La validación de la hora solo aparece al pulsar «Continuar», como «Hora no válida.» arriba de la pantalla, sin decir qué rango es válido ni ubicarse junto al campo. | P01-T2: 3 intentos y abandono de la hora pedida (éxito parcial). P02-T2: no vio el aviso y repitió Enter. | N5, N9, A2 (WCAG 3.3.1, 3.3.3) | **4** | Mostrar el rango permitido antes de escribir, validar al salir del campo, poner el mensaje junto al campo con la hora más temprana y devolver el foco al campo. | Corregido |
| **H2** | Con teclado, el foco no se mueve al cambiar de pantalla, no hay forma de saltar el encabezado y el anillo de foco es casi invisible (contraste 1,97:1). | P02-T1: perdió el foco dos veces y recorrió el encabezado en cada pantalla. P02-T2/T3. | A1 (WCAG 2.4.1, 2.4.3, 2.4.7, 2.4.13) | **3** | Enlace «Saltar al contenido», mover el foco al título de cada pantalla y anillo de 3 px en #1E4E8C (7,73:1). | Corregido |
| **H3** | El error de envío no da tranquilidad: no dice si se cobró o si se duplicará, oculta el resumen y no recibe el foco, por lo que una persona con teclado no lo percibe. | P01-T3: dudó ~10 s y preguntó si se cobraría dos veces. P02-T3: no notó el error. | N1, N9, A2 (WCAG 4.1.3) | **3** | Mensaje con causa y consecuencias («no se cobró nada», «no se duplicará»), mantener el resumen visible, enfocar el aviso y numerar el reintento. | Corregido |
| **H4** | La búsqueda distingue tildes y solo busca en el nombre: «cafe» devuelve 0 productos y el estado vacío no ofrece salida. | P01-T1: concluyó que no había café. P02-T1: necesitó dos búsquedas. | N9, N6 | **3** | Ignorar tildes y mayúsculas, buscar también por sinónimos (café, sandwich), y en «sin resultados» sugerir términos y «Limpiar búsqueda». | Corregido |
| **H5** | El aviso con «Deshacer» dura 2 s; con teclado no alcanza a llegar al botón. | P02-T2: «se fue muy rápido». | N3 Control y libertad; WCAG 2.2.1 | **2** | Duración de 6 s y foco directo en «Deshacer» tras «Quitar». | Corregido |

## 3. Verificación de las tres heurísticas de Nielsen

| Heurística | Resultado en la beta | Resultado en la v3 final |
|---|---|---|
| **N1 Visibilidad del estado del sistema** | Cumple parcialmente: el indicador de pasos, el contador «Mi pedido (n)» y el procesando funcionaron; pero el error de envío pasó inadvertido para P02 (H3). | **Cumple:** pasos, aviso al agregar con animación del contador, procesando con barra y botón bloqueado, aviso de error enfocado y confirmación con número y hora. Ambas personas leyeron el N.º 031 y la hora. |
| **N5 Prevención de errores** | No cumple: se podía enviar una hora inválida sin saber el rango (H1). | **Cumple:** el rango 09:51–17:45 está visible bajo el campo; P01 eligió una hora válida al primer intento. Además, el botón de hora se deshabilita con el pedido vacío y el producto agotado no se puede agregar. |
| **N9 Reconocer, diagnosticar y recuperarse de errores** | No cumple: mensajes genéricos («Hora no válida.», «Error al enviar.», «Sin resultados.») sin causa ni salida (H1, H3, H4). | **Cumple:** cada mensaje dice qué pasó, por qué y qué hacer, y conserva lo hecho (pedido guardado, resumen visible, sugerencias de búsqueda). P02 se recuperó de la hora inválida en 5 s. |

## 4. Verificación de las dos condiciones de accesibilidad

| Condición | Comprobación | Beta | v3 final |
|---|---|---|---|
| **A1 · Operable por teclado con foco visible** | P02 completa T1–T3 solo con teclado; contraste del indicador de foco ≥ 3:1; existe mecanismo para saltar bloques repetidos. | No cumple: contraste del foco 1,97:1, sin «Saltar al contenido», foco perdido al cambiar de pantalla. | **Cumple:** 3 tareas solo con teclado sin pérdidas de foco; contraste del foco 7,73:1; «Saltar al contenido» es el primer elemento con Tab. Botones de al menos 44 × 44 px. |
| **A2 · Errores y estados identificados y anunciados** | El error se describe en texto, está junto al control y asociado (`aria-invalid`, `aria-describedby`); los cambios de estado se anuncian (`aria-live`, `role="alert"`). | Cumple parcialmente: el texto existía pero lejos del campo y sin asociación; el error de envío no se anunciaba con foco. | **Cumple:** error de la hora asociado al campo, error de envío con `role="alert"` y foco, contador de resultados, aviso de agregado y estado «Enviando…» en regiones `aria-live`. Contraste de textos: 15,09:1 (texto), 5,62:1 (error), 5,60:1 (botón principal). |

## 5. Lo que funcionó desde la beta
- La personalización (tamaño y leche) con el precio en el botón se entendió sin dudas: 0 errores en ambas personas.
- «Quitar» y el total recalculado fueron claros; nadie confundió «Quitar» con «Deshacer».
- La pantalla de confirmación con el número grande permitió leer el N.º 031 de inmediato.
