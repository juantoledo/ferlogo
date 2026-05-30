# 🐢 FerLogo

A fun, kid-friendly **Logo** turtle-graphics playground that runs in the browser.
Type a command, press **Enter**, and watch a turtle walk across the screen drawing as it goes.

Commands work in **English *and* Spanish at the same time** — perfect for bilingual kids.

> 🇪🇸 *¿Prefieres español?* → [**README.md**](README.md)

![FerLogo screenshot](images/screenshot.png)

## ✨ A little story

When I was **7 years old** I first met Logo on an **Atari 800 XL**, typing `FORWARD` and
`RIGHT` into a turtle and feeling the magic of telling a computer what to do. FerLogo is my
small tribute to that moment — a modern, bilingual version so a new generation of kids can
discover the same joy.

## 🚀 How to run

No installation, no build, no server. Just **open `index.html`** in any browser
(double-click it, or drag it into a browser window).

```bash
xdg-open index.html      # Linux
open index.html          # macOS
start index.html         # Windows
```

## 🎮 How to play

1. **Pick a turtle** — choose from nine SVG turtle friends (green, blue, pink, orange, ninja, baby, galaxy, rainbow, robot).
2. **Type a command** in the sidebar and press **Enter** — it runs right away.
3. Want to write a whole program? Flip to **Batch / Lote** mode, type several lines, and press **▶ Run / Ejecutar**.
4. Tap **🎲 Example / Ejemplo** for ready-made drawings, **🧹 Clear / Limpiar** to start over,
   and use the **🐌 → 🐇 speed slider** to make the turtle walk slow or fast.

## 📖 Commands (English & Spanish)

> 🖨️ **Want to print it?** Open [**cheatsheet.html**](cheatsheet.html) in a browser and hit
> *Print* — it shows every shape really drawn, in color, so kids see exactly what to type.
> (A plain-text version also lives in [cheatsheet.md](cheatsheet.md).)

| What it does | English | Español |
|---|---|---|
| Move forward | `forward` / `fd` | `adelante` / `av` |
| Move back | `back` / `bk` | `atras` / `re` |
| Turn right | `right` / `rt` | `derecha` / `gd` |
| Turn left | `left` / `lt` | `izquierda` / `gi` |
| Pen up (stop drawing) | `penup` / `pu` | `subelapiz` / `sl` |
| Pen down (start drawing) | `pendown` / `pd` | `bajalapiz` / `bl` |
| Set pen color | `color red` | `color rojo` |
| Set pen width | `width 5` | `grosor 5` |
| Clear the board | `clear` / `cs` | `limpia` / `borra` |
| Go to the center | `home` | `casa` |
| Hide the turtle | `hideturtle` / `ht` | `oculta` / `ot` |
| Show the turtle | `showturtle` / `st` | `muestra` / `mt` |
| Repeat a block | `repeat 4 [ ... ]` | `repite 4 [ ... ]` |

### 🔷 Figures

Draw a whole shape with a single command (they use the current pen color and width):

| Figure | English | Español |
|---|---|---|
| Circle (radius) | `circle 60` | `circulo 60` |
| Square (side) | `square 80` | `cuadrado 80` |
| Triangle (side) | `triangle 90` | `triangulo 90` |
| Rectangle (width height) | `rectangle 120 60` | `rectangulo 120 60` |
| Polygon (sides side) | `polygon 6 60` | `poligono 6 60` |
| Star (size) | `star 120` | `estrella 120` |

**Colors:** red/rojo, blue/azul, green/verde, yellow/amarillo, orange/naranja,
purple/morado, pink/rosa, black/negro, brown/marron, white/blanco, gray/gris,
turquoise/turquesa, lime/lima — or any hex like `#ff0000`.

Commands are case- and accent-insensitive, so `atrás`, `ATRAS`, and `atras` all work.

### Try this 👇

```
color red
circle 70                                 # a red circle
star 120                                  # a star
polygon 6 60                              # a hexagon
repeat 6 [ circle 50 right 60 ]           # a flower of circles
```

## 🛠️ How it's built

A single self-contained `index.html`:

- **Vanilla JavaScript** — no frameworks, no dependencies.
- An HTML5 **`<canvas>`** holds the drawing; the turtle is an inline **SVG** moved and
  rotated with CSS transforms, so it stays crisp and animates smoothly.
- A tiny tokenizer → recursive parser (which expands nested `repeat`/`repite` and figures
  like `circle`/`square` into basic forward/turn moves) → an animation queue drained with
  `requestAnimationFrame` so kids *see* each step.

## 💛 License

Made with love for curious kids. Use it, share it, remix it.
