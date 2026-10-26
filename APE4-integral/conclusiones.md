# Conclusiones · APE 4 integral

**Responsable:** Vinces Cueva Boris Yussef (redacción) · revisado por todo el equipo

1. **Observar a los usuarios cambió decisiones que el equipo daba por buenas.** El wireframe original de la pantalla «Hora de retiro» validaba la hora solo al final y con un mensaje genérico; para el equipo era suficiente porque conocía el rango. La prueba mostró lo contrario: P01 necesitó tres intentos y abandonó la hora pedida, y P02 no vio el aviso. Mostrar el rango antes de escribir y el error junto al campo redujo el tiempo de T2 de 107 s a 49 s y los errores de 5 a 1.

2. **La visibilidad del estado y la recuperación de errores se demuestran con interacciones, no con pantallas sueltas.** La v3 responde a lo que la persona escribe (búsqueda, hora) y permite provocar un fallo de red real durante la prueba. Así se comprobó que un mensaje que dice qué pasó, que no se cobró y que no se duplicará, con el resumen visible y el foco en el aviso, elimina la duda que tuvo P01 y hace perceptible el error para quien usa teclado.

3. **La accesibilidad por teclado debe probarse con una persona usando solo teclado.** El código de la beta ya era semántico, pero el foco perdido entre pantallas y un indicador de 1,97:1 de contraste hicieron que P02 se perdiera dos veces. Con «Saltar al contenido», el foco al título de cada pantalla y un indicador de 7,73:1, P02 completó las tres tareas en 124 s en total (antes 221 s) sin perder el foco.

4. **El trabajo por ramas, issues y pull requests deja trazable el aporte individual.** Cada integrante abrió una issue, trabajó en su rama y su PR fue revisado por otro compañero; el historial de `APE4-integral/` permite ver quién hizo el diagnóstico, el prototipo, la prueba y la iteración.

## Trabajo futuro
- Probar la v3 con lector de pantalla (NVDA) y con un participante que use el celular con una mano en movimiento.
- Agregar la opción de guardar productos favoritos para repetir pedidos frecuentes.
- Medir con más participantes (5 o más) para comparar tiempos con significancia.
