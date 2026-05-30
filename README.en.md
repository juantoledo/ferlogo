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

> Commands are shown in UPPERCASE to match the keys on the keyboard; lowercase works too ·
> Las órdenes se muestran en MAYÚSCULAS como las teclas; las minúsculas también funcionan.

| What it does | English | Español |
|---|---|---|
| Move forward | `FORWARD` / `FD` | `ADELANTE` / `AV` |
| Move back | `BACK` / `BK` | `ATRAS` / `RE` |
| Turn right | `RIGHT` / `RT` | `DERECHA` / `GD` |
| Turn left | `LEFT` / `LT` | `IZQUIERDA` / `GI` |
| Pen up (stop drawing) | `PENUP` / `PU` | `SUBELAPIZ` / `SL` |
| Pen down (start drawing) | `PENDOWN` / `PD` | `BAJALAPIZ` / `BL` |
| Set pen color | `COLOR RED` | `COLOR ROJO` |
| Set pen width | `WIDTH 5` | `GROSOR 5` |
| Clear the board | `CLEAR` / `CS` | `LIMPIA` / `BORRA` |
| Go to the center | `HOME` | `CASA` |
| Hide the turtle | `HIDETURTLE` / `HT` | `OCULTA` / `OT` |
| Show the turtle | `SHOWTURTLE` / `ST` | `MUESTRA` / `MT` |
| Repeat a block | `REPEAT 4 [ ... ]` | `REPITE 4 [ ... ]` |

### 🔷 Figures

Draw a whole shape with a single command (they use the current pen color and width):

Each figure has a short form · Cada figura tiene una forma corta: `CI CU TR RC PG ES`.

| Figure | English | Español | Short · Corta |
|---|---|---|---|
| Circle (radius) | `CIRCLE 60` | `CIRCULO 60` | `CI 60` |
| Square (side) | `SQUARE 80` | `CUADRADO 80` | `CU 80` |
| Triangle (side) | `TRIANGLE 90` | `TRIANGULO 90` | `TR 90` |
| Rectangle (width height) | `RECTANGLE 120 60` | `RECTANGULO 120 60` | `RC 120 60` |
| Polygon (sides side) | `POLYGON 6 60` | `POLIGONO 6 60` | `PG 6 60` |
| Star (size) | `STAR 120` | `ESTRELLA 120` | `ES 120` |

**Colors:** RED/ROJO, BLUE/AZUL, GREEN/VERDE, YELLOW/AMARILLO, ORANGE/NARANJA,
PURPLE/MORADO, PINK/ROSA, BLACK/NEGRO, BROWN/MARRON, WHITE/BLANCO, GRAY/GRIS,
TURQUOISE/TURQUESA, LIME/LIMA — or any hex like `#FF0000`.

Commands are case- and accent-insensitive, so `ATRÁS`, `ATRAS`, and `atras` all work.

### Try this 👇

```
COLOR RED
CIRCLE 70                                 # a red circle
STAR 120                                  # a star
POLYGON 6 60                              # a hexagon
REPEAT 6 [ CIRCLE 50 RIGHT 60 ]           # a flower of circles
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
