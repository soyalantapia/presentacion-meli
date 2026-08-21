# Capturas de producto para la presentación

Dejá acá los archivos con **exactamente estos nombres** y yo los monto en la lámina
que corresponde. PNG o JPG, ancho mínimo 600 px, sin recortar el marco del teléfono.

---

## Lo que falta

| Archivo a dejar acá | Va en la lámina | Qué tiene que mostrar |
|---|---|---|
| `app-catalogo.png` ✅ | 01 portada · 04 | Catálogo por categorías, con foto, descripción y precio por plato |
| `app-ficha-plato.png` | 04 | Ficha de un plato: foto, nutricional, ingredientes, etiquetas de restricción y calificación |
| `app-comprobante-qr.png` | 04 | Comprobante con el código QR, número de pedido, punto de retiro y franja |
| `kds-cocina.png` | 07 | Pantalla de cocina con comandas: número de pedido, cronómetro, ítems y estado |

## Lo que ya está resuelto

| Lámina | Estado |
|---|---|
| 05 · Panel de Facilities | Captura real, embebida |
| 06 · Tablero de datos | Captura real, embebida |

## Lo que no necesita captura

| Lámina | Por qué |
|---|---|
| 22 · Seamos pioneros | Es un gráfico de comparación, no una pantalla |
| 24 · Cierre | Se compone a partir de las capturas de arriba, una vez que estén las cuatro |

---

## Cómo se montan

Las imágenes se **embeben en base64** dentro del HTML, no se referencian por ruta.
Es deliberado: una ruta relativa ya nos dio un 404 en producción cuando el archivo no
se copió al sitio publicado. Embebidas, la página es autocontenida y no puede romperse
por un asset faltante.

Los archivos de esta carpeta quedan como **fuente**, no como lo que sirve la página.

## Antes de publicar

`publicar.sh` verifica que toda ruta relativa del documento exista en el destino y
avisa si falta alguna, en vez de publicar en silencio.
