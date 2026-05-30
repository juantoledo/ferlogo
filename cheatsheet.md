# 🐢 FerLogo — Tarjeta de Órdenes · Command Card

> Para imprimir y tener al lado de la computadora · Print it and keep it next to the computer
> Las órdenes funcionan en **español o inglés** · Commands work in **Spanish or English**

---

## 🚶 Moverse · Move

| Qué hace · What | Español | English | Ejemplo · Example |
|---|---|---|---|
| Avanza · forward | `adelante` `av` | `forward` `fd` | `adelante 100` |
| Retrocede · back | `atras` `re` | `back` `bk` | `atras 50` |
| Gira a la derecha · right | `derecha` `gd` | `right` `rt` | `derecha 90` |
| Gira a la izquierda · left | `izquierda` `gi` | `left` `lt` | `izquierda 45` |
| Al centro · go home | `casa` | `home` | `casa` |

## ✏️ El lápiz · The pen

| Qué hace · What | Español | English | Ejemplo · Example |
|---|---|---|---|
| Sube el lápiz (no dibuja) · pen up | `subelapiz` `sl` | `penup` `pu` | `subelapiz` |
| Baja el lápiz (dibuja) · pen down | `bajalapiz` `bl` | `pendown` `pd` | `bajalapiz` |
| Cambia el color · set color | `color` | `color` | `color rojo` |
| Cambia el grosor · set width | `grosor` | `width` | `grosor 6` |
| Limpia la pizarra · clear | `limpia` `borra` | `clear` `cs` | `limpia` |

## 🔁 Repetir · Repeat

| Qué hace · What | Español | English |
|---|---|---|
| Repite un bloque · repeat a block | `repite 4 [ ... ]` | `repeat 4 [ ... ]` |

Ejemplo · Example: `repite 4 [ adelante 100 derecha 90 ]`

## 🔷 Figuras · Figures

Dibuja una figura completa con una sola orden · Draw a whole shape with one command:

| Figura · Figure | Español | English |
|---|---|---|
| Círculo · circle | `circulo 60` | `circle 60` |
| Cuadrado · square | `cuadrado 80` | `square 80` |
| Triángulo · triangle | `triangulo 90` | `triangle 90` |
| Rectángulo · rectangle | `rectangulo 120 60` | `rectangle 120 60` |
| Polígono · polygon | `poligono 6 60` | `polygon 6 60` |
| Estrella · star | `estrella 120` | `star 120` |

## 🐢 Esconder y mostrar · Hide and show

| Qué hace · What | Español | English |
|---|---|---|
| Esconde la tortuga · hide | `oculta` `ot` | `hideturtle` `ht` |
| Muestra la tortuga · show | `muestra` `mt` | `showturtle` `st` |

## 🎨 Colores · Colors

`rojo`/red · `azul`/blue · `verde`/green · `amarillo`/yellow · `naranja`/orange ·
`morado`/purple · `rosa`/pink · `negro`/black · `marron`/brown · `blanco`/white ·
`gris`/gray · `turquesa`/turquoise · `lima`/lime

¡También puedes usar un código como · You can also use a code like! `#ff0000`

---

## ✨ ¡Pruébalo! · Try it!

Escribe esto · Type this:

```
color azul
repite 4 [ adelante 120 derecha 90 ]
```

Y la tortuga dibuja un cuadrado · And the turtle draws a square:

```
   ┌─────────────┐
   │             │
   │             │
   │             │
   │             │
   └─────────────┘
```

Ahora prueba una estrella · Now try a star:

```
color morado
estrella 140
```

```
          ／＼
        ／    ＼
   ━━━━●━━━━━━━●━━━━
     ＼   ＼ ／   ／
       ＼   ●   ／
         ＼ │ ／
           ＼
```

Y un sol con círculos · And a sun made of circles:

```
color naranja
repite 8 [ circulo 40 derecha 45 ]
```

```
        .-""-.
      .'  ()  '.
     /  .-""-.  \
    |  /      \  |
    |  \      /  |
     \  '-..-'  /
      '.  ()  .'
        '-..-'
```

---

## 💡 Trucos · Tips

- 🐢 Presiona **Enter** para ejecutar una orden · Press **Enter** to run a command.
- 🐌🐇 Mueve la barra de velocidad para ver a la tortuga caminar lento o rápido ·
  Move the speed slider to watch the turtle walk slow or fast.
- 🎲 Toca **Ejemplo · Example** si no sabes qué dibujar · Tap **Example** if you're stuck.
- ❌ Si te equivocas no pasa nada, ¡vuelve a intentar! · If you make a mistake, just try again!

---

*Hecho con cariño para pequeños programadores 🐢 · Made with love for little coders.*
