# 🐢 FerLogo

Un divertido patio de juegos de **Logo** (gráficos de tortuga) para niños, que funciona en el
navegador. Escribe una orden, presiona **Enter** y mira a la tortuga caminar por la pantalla
dibujando a su paso.

Las órdenes funcionan en **inglés *y* español al mismo tiempo** — ideal para niños bilingües.

> 🇬🇧 *Prefer English?* → [**README.en.md**](README.en.md)

![Captura de FerLogo](images/screenshot.png)

## ✨ Una pequeña historia

Cuando tenía **7 años** conocí Logo por primera vez en un **Atari 800 XL**, escribiendo
`FORWARD` y `RIGHT` para mover una tortuga y sintiendo la magia de decirle a una computadora
qué hacer. FerLogo es mi pequeño homenaje a ese momento — una versión moderna y bilingüe para
que una nueva generación de niños descubra la misma alegría.

## 🚀 Cómo ejecutarlo

Sin instalación, sin compilar, sin servidor. Solo **abre `index.html`** en cualquier navegador
(haz doble clic, o arrástralo a una ventana del navegador).

```bash
xdg-open index.html      # Linux
open index.html          # macOS
start index.html         # Windows
```

## 🎮 Cómo jugar

1. **Elige una tortuga** — escoge entre seis tortugas SVG (verde, azul, rosa, naranja, ninja, bebé).
2. **Escribe una orden** en la barra lateral y presiona **Enter** — se ejecuta de inmediato.
3. ¿Quieres escribir un programa completo? Cambia al modo **Lote / Batch**, escribe varias líneas
   y presiona **▶ Ejecutar / Run**.
4. Toca **🎲 Ejemplo / Example** para dibujos listos, **🧹 Limpiar / Clear** para empezar de nuevo,
   y usa el **control de velocidad 🐌 → 🐇** para que la tortuga camine lento o rápido.

## 📖 Órdenes (español e inglés)

| Qué hace | Español | English |
|---|---|---|
| Avanzar | `adelante` / `av` | `forward` / `fd` |
| Retroceder | `atras` / `re` | `back` / `bk` |
| Girar a la derecha | `derecha` / `gd` | `right` / `rt` |
| Girar a la izquierda | `izquierda` / `gi` | `left` / `lt` |
| Subir el lápiz (no dibuja) | `subelapiz` / `sl` | `penup` / `pu` |
| Bajar el lápiz (dibuja) | `bajalapiz` / `bl` | `pendown` / `pd` |
| Cambiar el color | `color rojo` | `color red` |
| Cambiar el grosor | `grosor 5` | `width 5` |
| Limpiar la pizarra | `limpia` / `borra` | `clear` / `cs` |
| Ir al centro | `casa` | `home` |
| Ocultar la tortuga | `oculta` / `ot` | `hideturtle` / `ht` |
| Mostrar la tortuga | `muestra` / `mt` | `showturtle` / `st` |
| Repetir un bloque | `repite 4 [ ... ]` | `repeat 4 [ ... ]` |

**Colores:** rojo/red, azul/blue, verde/green, amarillo/yellow, naranja/orange,
morado/purple, rosa/pink, negro/black, marron/brown, blanco/white — o cualquier hex como `#ff0000`.

No importan las mayúsculas ni los acentos: `atrás`, `ATRAS` y `atras` funcionan igual.

### Prueba esto 👇

```
repite 4 [ adelante 100 derecha 90 ]      # un cuadrado
color rojo
repite 3 [ adelante 120 derecha 120 ]     # un triángulo rojo
repite 36 [ adelante 12 derecha 10 ]      # un círculo
```

## 🛠️ Cómo está hecho

Un único archivo `index.html` autónomo:

- **JavaScript puro** — sin frameworks, sin dependencias.
- Un **`<canvas>`** de HTML5 guarda el dibujo; la tortuga es un **SVG** que se mueve y gira con
  transformaciones CSS, para que se vea nítida y se anime con suavidad.
- Un pequeño tokenizador → analizador recursivo (que expande `repite`/`repeat`, incluso anidados)
  → una cola de animación que se vacía con `requestAnimationFrame` para que los niños *vean* cada paso.

## 💛 Licencia

Hecho con cariño para niños curiosos. Úsalo, compártelo, modifícalo.
