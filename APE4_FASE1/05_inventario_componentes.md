# Inventario de componentes reutilizables — CaféU

**Menú principal:** la pantalla «Menú de hoy» funciona como punto de entrada y centro de la aplicación, con el acceso persistente «Ver pedido (n) · total». El resto de la navegación es jerárquica y lineal por pasos; cada transición se dispara con un botón de etiqueta explícita y las salidas («Volver al menú», «Cancelar (sin guardar)») siempre están visibles.

| Tipo | Componente | Se reutiliza en | Función | Justificación |
|---|---|---|---|---|
| Menú | Encabezado «CaféU» con separador | Todas | Identifica la aplicación | Consistencia y estándares |
| Menú | Chips de categoría | 1.0 | Filtran el menú con un toque | Reconocer antes que recordar |
| Menú | Acceso «Ver pedido (n) · total» | 1.0 | Lleva al pedido en curso | Visibilidad del estado |
| Tarjeta | Tarjeta de producto | 1.0 | Escanear el menú y ver precios | Reconocer antes que recordar |
| Tarjeta | Resumen del pedido con total en negrita | 2.0, 2.1, 3.0 | Verificar productos y total | Prevención de errores |
| Tarjeta | Tarjeta de confirmación con número | 3.0 | Señal clara de recepción | Visibilidad del estado |
| Formulario | Stepper de cantidad (− 1 +) | 1.1, 2.1 | Ajustar cantidades sin teclado | Prevención de errores; área táctil mínima |
| Botón | Botón primario (borde grueso) | 1.0, 1.1, 2.0, 2.1 | Acción principal de cada pantalla | Jerarquía visual; Ley de Fitts |
| Botón | Botón secundario (borde fino) | 1.1, 2.0, 2.1, 3.0 | Alternativas y salidas | Control y libertad del usuario |
| Botón | Botón «Quitar» | 2.1 | Eliminar un producto | Control y libertad del usuario |
| Botón | Botón deshabilitado | 1.0, 2.1 | Impedir acciones no válidas | Prevención de errores |
| Mensaje | Nota de pago | 2.0, 3.0 | «Retira y paga en cafetería. No se cobra al confirmar.» | Visibilidad del estado |
| Mensaje | Mensaje de cambio | 2.0 | «Se quitó el sanduche y el total se recalculó.» | Visibilidad del estado |
| Mensaje | Mensaje de error o aviso | 2.0, 2.1 | Error de envío y pedido vacío | Recuperarse de errores |
