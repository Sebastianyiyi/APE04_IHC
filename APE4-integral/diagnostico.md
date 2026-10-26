# Fase 1 · Diagnóstico de la v2 de CaféU

**Responsable:** Acaro Ibujés Pedro Sebastián · **Punto de partida:** prototipo v2 en Figma (APE4 Fase 2) y wireframes de la Fase 1 que están en este mismo repositorio (`APE4_FASE1/` y `APE4_Fase2/`).

## 1. Usuario

| Aspecto | Descripción |
|---|---|
| Usuario principal | Estudiante de la FISEI (18–25 años) que compra en la cafetería entre clases. |
| Contexto | Usa el celular de pie, en el pasillo o en la fila, con una mano y con poco tiempo (recesos de 10–20 min). |
| Objetivo | Pedir una bebida o comida a su gusto y retirarla a una hora que encaje con su horario, sin hacer fila. |
| Necesidades | Encontrar rápido un producto, personalizarlo (tamaño, tipo de leche), saber cuándo estará listo y tener certeza de que el pedido se envió. |
| Usuarios secundarios | Estudiantes que navegan con teclado o lector de pantalla (por preferencia o por una condición temporal o permanente). |

## 2. Tres tareas representativas

| Tarea | Formulación para el participante | Criterio de éxito |
|---|---|---|
| **T1 · Localizar y seleccionar** | «Quieres un café con leche para llevar. Búscalo en el menú y agrégalo a tu pedido en tamaño mediano y con leche de almendra.» | El capuchino mediano con leche de almendra aparece en «Mi pedido». |
| **T2 · Modificar con validación** | «En tu pedido hay un sanduche que ya no quieres: quítalo y programa el retiro para las 09:45, porque sales de clase a las 09:40.» | El pedido queda sin el sanduche y con una hora de retiro válida programada (la app debe impedir 09:45 y la persona debe corregirla). |
| **T3 · Finalizar y verificar** | «Confirma el pedido y dime cuál es tu número de pedido y a qué hora lo retiras.» | La persona confirma, se recupera si el envío falla y lee en voz alta el número y la hora. |

## 3. Revisión de los wireframes y de la v2

Se recorrió la v2 de Figma (17 pantallas: recorrido de pedido, edición y caso de error) contra las tres tareas anteriores y contra las 10 heurísticas de Nielsen y WCAG 2.2 nivel AA.

| Pantalla v2 | Lo que funciona | Lo que falta frente a las tareas |
|---|---|---|
| Menú de hoy (v2_01) | Filtros Todo/Bebidas/Comida, estado «Agotado», botón «+ Agregar» con feedback. | No hay búsqueda; con un menú más largo la persona debe recorrer toda la lista. |
| Detalle (v2_02, v2_04) | Cantidad con límite 1–9 y precio en el botón. | No permite elegir tamaño ni tipo de leche (escenario de personalización no cubierto). |
| Revisa tu pedido (v2_06) | Resumen, total, aviso «Pagas al retirar». | No se puede elegir la hora de retiro (escenario no cubierto). |
| Enviando / error (v2_07, v2_17) | Estado de procesamiento y mensaje de error bien redactado. | Los estados se muestran en rutas fijas; no responden a lo que la persona escribe. |
| Todo el prototipo | Jerarquía clara y consistente. | Figma no se puede operar con teclado ni con lector de pantalla; no hay foco visible ni mensajes anunciados. |

## 4. Matriz de problemas priorizados

Severidad según Nielsen (0 = no es problema … 4 = catástrofe). Prioridad = severidad × frecuencia esperada (1 = rara, 2 = frecuente, 3 = en cada uso).

| ID | Problema | Evidencia | Heurística / criterio | Sev. | Frec. | Prioridad | Decisión para la v3 |
|---|---|---|---|---|---|---|---|
| **P1** | No se puede elegir la hora de retiro; el estudiante no sabe si su pedido estará listo cuando salga de clase. | v2_06, v2_08: solo «en preparación». | N1 Visibilidad del estado; N7 Flexibilidad | 3 | 3 | **9** | Nueva pantalla 3.1 «Hora de retiro» con «Lo antes posible» o «Programar una hora» validada. |
| **P2** | El prototipo no es operable con teclado ni lector de pantalla. | Prueba en Figma: Tab no recorre controles; sin foco visible. | WCAG 2.1.1, 2.4.7, 4.1.3 | 3 | 2 | **6** | Construir la v3 en HTML semántico: orden de foco, foco visible, `aria-live`, saltar al contenido. |
| **P3** | No hay personalización (tamaño, leche); el precio no refleja variantes. | v2_02 solo tiene cantidad. | N2 Relación con el mundo real | 2 | 3 | **6** | Detalle con grupos de opciones (radio) y precio que se actualiza en el botón. |
| **P4** | No hay búsqueda; localizar un producto depende de recorrer la lista. | v2_01: 5 productos visibles, sin campo de búsqueda. | N6 Reconocer antes que recordar; N7 | 2 | 2 | **4** | Campo «Buscar en el menú» con conteo de resultados y estado «sin resultados» con salida. |
| **P5** | Los estados (error, procesamiento) son pantallas fijas: no se puede probar una validación con datos reales del usuario. | v2_15→v2_17 siempre fallan en el mismo punto. | N5 Prevención de errores; N9 Recuperación | 2 | 2 | **4** | Validación real de la hora y fallo de red que el moderador activa durante la prueba. |

**Conclusión del diagnóstico:** la v2 resolvió los problemas de la Fase 2 (edición, confirmación y error de envío), pero no cubre el escenario «pedir ahora y retirar después de clase», no es accesible por teclado y no tiene búsqueda. Estos cinco problemas definen el alcance de la v3 (ver `sitemap.png`, `user-flow.png` y `prototipo/`).
