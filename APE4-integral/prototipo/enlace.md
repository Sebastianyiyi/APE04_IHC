# Acceso al prototipo · CaféU v3

**Responsable:** González Álvarez Vladimir Humberto

## Ver en el navegador
- **v3 final:** https://raw.githack.com/Sebastianyiyi/APE04_IHC/main/APE4-integral/prototipo/cafeu-v3.html
- **v3 beta (versión probada):** https://raw.githack.com/Sebastianyiyi/APE04_IHC/main/APE4-integral/prototipo/cafeu-v3-beta.html
- Alternativa: https://htmlpreview.github.io/?https://github.com/Sebastianyiyi/APE04_IHC/blob/main/APE4-integral/prototipo/cafeu-v3.html
- Sin internet: descargar `cafeu-v3.html` y abrirlo con doble clic (un solo archivo, sin dependencias).

## Parámetros útiles
| Parámetro | Efecto |
|---|---|
| `?prueba=1` | Muestra el panel del moderador con «Simular fallo de red en el próximo envío». |
| `?vista=wireframe` | Muestra las mismas pantallas en escala de grises (baja fidelidad). |
| `?pantalla=menu` | Inicia directamente en «Menú de hoy». |

Ejemplo para la defensa: `cafeu-v3.html?prueba=1`

## Recorrido de demostración (extremo a extremo)
1. **Inicio** → «Ver menú».
2. Escribir **cafe** (sin tilde) → aparecen Café americano y Capuchino.
3. «Ver detalle» de Capuchino → Mediano, De almendra → «Agregar al pedido · $2,70» → el contador «Mi pedido» se anima.
4. «Mi pedido» → «Elegir hora de retiro» → «Programar una hora» → escribir **09:45** → salir del campo: aparece el error junto a la hora.
5. Corregir a **09:55** → «Revisar y confirmar».
6. Activar «Simular fallo de red» en el panel → «Confirmar pedido»: procesando → error con pedido guardado y foco en el aviso.
7. «Reintentar envío (intento 2)» → **¡Pedido confirmado! N.º 031 · Retira a las 09:55**.
8. Repetir 1–7 solo con teclado (primer Tab: «Saltar al contenido»).

## Prototipo anterior (v2, Figma)
https://www.figma.com/design/TO6AmVVBbCJxYHiHZDvW9U/Untitled?node-id=33-6
