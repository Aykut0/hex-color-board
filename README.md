# HEX Color Board

> **A personal project, made as a gift for a graphic-designer friend.** A small board that turns
> real-world colors into HEX codes and back.

![3D render of the board](docs/images/board_3d.png)

## What it does

Designers work with colors as HEX codes (like `#E2552C`). This board gives three ways to move
between a color and its code:

1. **Pick** a color from the on-screen spectrum and read its HEX code.
2. **Type** a HEX code and see the color on the screen.
3. **Capture** a color from the real world with the color sensor on the back, and see it on
   screen with its HEX code.

## How it works

- **ESP32-S3-Zero** microcontroller board runs the interface.
- **2.8-inch SPI touch display** for the color picker and HEX entry.
- **TCS34725 RGB color sensor** on the back, read over I²C, with its own white LED for
  consistent lighting.
- A small MOSFET switches the display backlight.

![Schematic overview (rendered from the KiCad file)](docs/images/schematic_overview.png)

## Repository structure

```
hex-color-board/
├── hardware/
│   ├── hex_display.kicad_pro   # KiCad project (open this)
│   ├── hex_display.kicad_sch
│   ├── hex_display.kicad_pcb
│   └── fabrication/            # Gerber and drill files
└── docs/images/
```

## Manufacturing

The board was made in-house on an LPKF laser PCB machine from the files in
`hardware/fabrication/`.

## Status

Built and working. Photos of the finished board will be added.

---

**Author:** Yaşar Aykut Altuntop · MSc student, Biomedical Sciences and Engineering, Koç University  
[LinkedIn](https://linkedin.com/in/aykutaltuntop) · [GitHub](https://github.com/Aykut0)
