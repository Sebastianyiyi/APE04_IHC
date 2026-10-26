# APE 4 integral · Prototipado – Wireframes: CaféU v3

**Caso de estudio:** CaféU, pedidos anticipados para la cafetería de la FISEI
**Asignatura:** Interacción Humano-Computador · 5.º semestre, paralelo A · UTA – FISEI
**Docente:** Ing. José Caiza, Mg. · **Ciclo:** agosto 2026 – diciembre 2026
**Repositorio:** https://github.com/Sebastianyiyi/APE04_IHC

## Integrantes y aportes
| Integrante | Issue | Rama | Entregables | Revisó el PR de |
|---|---|---|---|---|
| Acaro Ibujés Pedro Sebastián | «APE4 integral · Diagnóstico, sitemap y user flows» | `feature/pedro-diagnostico` | `diagnostico.md`, `sitemap.png/pdf`, `user-flow.png/pdf` | Boris |
| González Álvarez Vladimir Humberto | «APE4 integral · Wireframes y prototipo v3» | `feature/vladimir-prototipo` | `wireframes/`, `prototipo/` | Santiago |
| Mora Beltrán Santiago Sebastián | «APE4 integral · Protocolo, prueba y hallazgos» | `feature/santiago-pruebas` | `pruebas/`, `evidencias/` | Pedro |
| Vinces Cueva Boris Yussef | «APE4 integral · Iteración, conclusiones e informe» | `feature/boris-iteracion` | `iteracion/`, `conclusiones.md`, `README.md`, informe PDF | Vladimir |

Los aportes se verifican en la pestaña **Issues** (cerradas por su PR), en **Pull requests** (autor y revisor) y en el historial de esta carpeta: `git log --format="%an | %ad | %s" -- APE4-integral/`.

## Prototipo
- ▶ **v3 final:** https://raw.githack.com/Sebastianyiyi/APE04_IHC/main/APE4-integral/prototipo/cafeu-v3.html
- ▶ **v3 final con panel del moderador:** https://raw.githack.com/Sebastianyiyi/APE04_IHC/main/APE4-integral/prototipo/cafeu-v3.html?prueba=1
- ▶ **v3 beta (versión probada):** https://raw.githack.com/Sebastianyiyi/APE04_IHC/main/APE4-integral/prototipo/cafeu-v3-beta.html
- v2 (Figma, Fase 2): https://www.figma.com/design/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-6
- Instrucciones y recorrido de demostración: [`prototipo/enlace.md`](prototipo/enlace.md)

## Reto de la v3
Diseñar y probar una v3 que cubra un **escenario no cubierto** por la v2 (programar la hora de retiro y personalizar la bebida), sea **accesible por teclado** y permita **recuperarse de errores**, comparando v2 → v3.

## Contenido de la carpeta
| Fase | Entregable | Archivo |
|---|---|---|
| 1. Diagnóstico | Usuario, tres tareas, revisión y matriz de cinco problemas priorizados | [`diagnostico.md`](diagnostico.md) |
| 1. Diagnóstico | Sitemap (3 niveles, 7 pantallas) | [`sitemap.png`](sitemap.png) · [`sitemap.pdf`](sitemap.pdf) |
| 1. Diagnóstico | User flows de T1, T2 y T3 | [`user-flow.png`](user-flow.png) · [`user-flow.pdf`](user-flow.pdf) |
| 2. Construcción | Wireframes de 7 pantallas y decisiones (jerarquía, Gestalt, carga cognitiva) | [`wireframes/`](wireframes/README.md) |
| 2. Construcción | Prototipo navegable en HTML (v3 final y v3 beta) | [`prototipo/`](prototipo/enlace.md) |
| 3. Prueba | Protocolo, participantes, tareas, métricas | [`pruebas/protocolo.md`](pruebas/protocolo.md) |
| 3. Prueba | Datos por participante y tarea | [`pruebas/resultados.csv`](pruebas/resultados.csv) |
| 3. Prueba | Hallazgos, 3 heurísticas y 2 condiciones de accesibilidad | [`pruebas/hallazgos.md`](pruebas/hallazgos.md) |
| 4. Iteración | Antes/después de 5 hallazgos con justificación | [`iteracion/antes-despues.md`](iteracion/antes-despues.md) |
| 4. Iteración | Registro de cambios | [`iteracion/cambios.md`](iteracion/cambios.md) |
| Evidencias | Registros de observación y capturas | [`evidencias/`](evidencias/README.md) |
| 5. Defensa | Conclusiones | [`conclusiones.md`](conclusiones.md) |
| Informe | Informe en formato UTA | [`APE4_Integral_Informe.pdf`](APE4_Integral_Informe.pdf) · `.docx` |

## Cumplimiento de la construcción
| Requisito | Cómo se cumple |
|---|---|
| Mínimo seis pantallas | 7: Inicio, Menú de hoy, Detalle, Mi pedido, Hora de retiro, Revisa y confirma, Pedido confirmado. |
| Tres flujos | F1 buscar y agregar · F2 modificar y programar el retiro · F3 confirmar con error y reintento. |
| Estados | Normal, vacío, agotado, error de validación, procesando, error de envío y éxito. |
| Feedback | Aviso al agregar, precio y total en vivo, «Paso n de 4», mensajes junto al campo. |
| Microinteracción | Animación del contador «Mi pedido (n)» al agregar; spinner y barra al enviar. |

## Resultados en una línea
| | v3 beta | v3 final |
|---|---|---|
| Tareas completadas | 5/6 | 6/6 |
| Tiempo medio T1 / T2 / T3 | 71 / 107 / 45 s | 31,5 / 49 / 32 s |
| Errores | 10 | 1 |
| SEQ medio | 3,67 | 6,17 |

## Defensa
1. **¿Qué decisión del wireframe original cambió por observar a los usuarios?** La validación de la hora de retiro: pasó de validar al final con «Hora no válida.» a mostrar el rango antes de escribir y el error junto al campo, porque P01 abandonó la hora pedida tras tres intentos y P02 no vio el aviso (H1).
2. **¿Cómo demuestra el prototipo la visibilidad del estado y la recuperación de errores?** Con el indicador de pasos, el contador animado, el estado «Enviando…» con botón bloqueado, el fallo de red que el moderador activa en vivo y el aviso que conserva el pedido, aclara que no hubo cobro y numera el reintento (H3).
3. **¿Qué evidencia identifica el aporte de cada integrante?** Una issue por integrante, su rama `feature/…`, sus commits sobre su carpeta y su PR revisado por otro compañero (tabla de aportes de arriba).
