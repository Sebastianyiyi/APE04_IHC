# Protocolo de la prueba de usabilidad y accesibilidad · CaféU v3

**Responsable:** Mora Beltrán Santiago Sebastián (moderador) · **Observador y cronometrista:** Vinces Cueva Boris Yussef

## 1. Objetivo
Comprobar si un estudiante ajeno al diseño puede buscar, personalizar, modificar, programar el retiro y confirmar un pedido en CaféU v3 sin ayuda, y verificar tres heurísticas de Nielsen y dos condiciones de accesibilidad (WCAG 2.2 AA).

## 2. Versión evaluada y materiales
| Elemento | Detalle |
|---|---|
| Prototipo probado | `prototipo/cafeu-v3-beta.html?prueba=1` (primera construcción de la v3). |
| Verificación tras la iteración | `prototipo/cafeu-v3.html?prueba=1` (v3 final, mismas tareas). |
| Equipo | Laptop de 14″ con Chrome; ventana con el teléfono simulado de 390 px. |
| Panel del moderador | Con `?prueba=1` aparece un panel lateral para activar «Simular fallo de red en el próximo envío» sin que el participante lo vea. |
| Registro | Cronómetro, hoja de observación (`evidencias/registros-observacion/`), capturas de pantalla. |

## 3. Participantes
Dos personas ajenas al equipo y al diseño, estudiantes de la UTA que compran en la cafetería.

| ID | Perfil | Uso del celular / apps de pedidos | Condición de la sesión |
|---|---|---|---|
| **P01** | Estudiante de 3.er semestre de Contabilidad y Auditoría, 20 años. | Diario; usa apps de comida a domicilio. | Mouse y teclado, como prefiera. |
| **P02** | Estudiante de 6.º semestre de Diseño Gráfico, 22 años. | Diario; usa apps bancarias y de transporte. | **Solo teclado** (Tab, Shift+Tab, Enter, Espacio, flechas), para verificar las condiciones de accesibilidad. |

Ambas personas aceptaron participar de forma verbal, sabían que se evalúa la aplicación y no a ellas, y podían detener la sesión cuando quisieran. No se registraron nombres.

## 4. Tareas (se leen tal cual, sin orientar)
| Tarea | Consigna | Estado inicial | Éxito |
|---|---|---|---|
| **T1** | «Quieres un café con leche para llevar. Búscalo en el menú y agrégalo a tu pedido en tamaño mediano y con leche de almendra.» | Pantalla de inicio, pedido vacío. | Capuchino mediano con leche de almendra en «Mi pedido». |
| **T2** | «En tu pedido hay un sanduche que ya no quieres: quítalo y programa el retiro para las 09:45, porque sales de clase a las 09:40.» | El moderador agrega un sanduche de queso antes de empezar. | Sanduche quitado y una hora válida programada (09:45 no es válida: la más temprana es 09:51). |
| **T3** | «Confirma el pedido y dime cuál es tu número de pedido y a qué hora lo retiras.» | Pantalla «Revisa y confirma». El moderador activa el fallo de red en el primer envío. | Reintenta, llega a la confirmación y lee el número y la hora. |

## 5. Procedimiento (≈ 15 min por persona)
1. Bienvenida, explicación de pensar en voz alta y del registro (1 min).
2. Ejecución de T1, T2 y T3 en orden. El cronómetro empieza al terminar de leer la consigna y se detiene cuando la persona dice «listo» o cumple el criterio.
3. Después de cada tarea: pregunta de facilidad **SEQ** («¿Qué tan fácil fue la tarea?» de 1 = muy difícil a 7 = muy fácil).
4. Al final: «¿Qué fue lo más confuso?» y «¿Qué cambiarías?».
5. El moderador no responde preguntas sobre la interfaz durante la tarea; si la persona se bloquea más de 2 min se registra como «no completada».

## 6. Métricas
| Métrica | Cómo se mide |
|---|---|
| Éxito | S = cumple el criterio sin ayuda · P = cumple solo una parte · N = no cumple. |
| Tiempo | Segundos desde la consigna hasta el criterio de éxito. |
| Errores | Acciones que no llevan a la meta (búsqueda fallida, hora inválida enviada, pérdida del foco, retroceso innecesario). |
| SEQ | Escala de 1 a 7 tras cada tarea. |
| Observación | Comentario textual o comportamiento relevante. |

## 7. Heurísticas y condiciones de accesibilidad verificadas
| Código | Qué se verifica | Dónde |
|---|---|---|
| **N1** Visibilidad del estado del sistema | La persona sabe en qué paso está, qué se agregó y si el envío está en curso, falló o se confirmó. | Indicador «Paso n de 4», aviso al agregar, procesando, error y éxito. |
| **N5** Prevención de errores | La app evita que se envíe una hora fuera del rango y muestra el rango antes de escribir. | Pantalla 3.1 «Hora de retiro». |
| **N9** Ayudar a reconocer, diagnosticar y recuperarse de errores | Los mensajes dicen qué pasó, por qué y cómo seguir, sin perder lo hecho. | Hora inválida, búsqueda sin resultados y error de envío. |
| **A1** Operable por teclado con foco visible (WCAG 2.1.1, 2.4.1, 2.4.7, 2.4.13) | Todas las tareas se completan solo con teclado, el foco se ve (contraste ≥ 3:1) y se puede saltar el encabezado. | Sesión de P02. |
| **A2** Errores y estados identificados y anunciados (WCAG 3.3.1, 3.3.3, 4.1.3) | El error se muestra en texto junto al campo, está asociado al control y los cambios de estado se anuncian (`aria-live`, `role="alert"`). | Hora inválida y error de envío. |

## 8. Fechas
- Prueba de la versión beta: 22 de octubre de 2026, laboratorio de la FISEI.
- Verificación de la v3 final con las mismas personas y tareas: 24 de octubre de 2026.
