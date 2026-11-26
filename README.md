# gojboard52 hardware

Hardware files for **gojboard52**, a split wireless keyboard built around two nice!nano v2 controllers. The right
half carries a capacitive touch-bar slider (Microchip AT42QT2120); the left half carries a nice!view display
(an OLED footprint is also on the board).

Firmware lives in its own repository: https://github.com/Ocelot08/gojboard52-zmk

> Work in progress. Photos and build notes are still to come.

## Contents

| Folder | What is in it |
| --- | --- |
| `pcb/main-board/` | Keyboard PCB, KiCad 10 project (`BTSplit.kicad_pro`), STEP model, and fabrication gerbers (`gerber/`, zipped as `GojBoardV2-2_gerbers.zip`) |
| `pcb/touch-bar/` | Touch-bar PCB, KiCad project (`BTSplit_Touch.kicad_pro`), STEP model, and gerbers (`gerber/`, zipped as `GBTouchV0-3_gerbers.zip`) |
| `pcb/libs/` | The custom symbols and footprints these boards use (the double-sided SMD footprints, the pro micro and OLED footprints, the logo graphics) |
| `case/step/` | Case top and bottom (V4b) and a test plate, as STEP |
| `case/stl/` | Printable support parts: touch-bar support, nice!view support, alignment frame |
| `case/keycaps/` | Blank keycap and layer/mod keycap models |
| `docs/` | AT42QT2120 datasheet |

The editable Rhino (`.3dm`) case models are not in this repository because of their size (40 MB or more each).

## PCB notes

- Project files are named `BTSplit` from the project's earlier name. The board is the gojboard52.
- Main board: 28 switch positions per board (Kailh low-profile, reversible footprint), through-hole diodes,
  1206 hand-solder resistors and capacitors, a pro-micro-pattern socket for the nice!nano, and double-sided SMD
  footprints (reset switch, power switch, resistors, capacitors) so they can be placed on either side.
- Reset switch: Panasonic EVQ-PUA02K. Power switch: Alps SSSS811101.
- Touch bar: three-electrode slider mode, six 1206 resistors, all 4.7 kΩ as built.
- Schematics and boards embed the symbols and footprints they use, so the projects open without extra setup. To edit
  parts, add `pcb/libs/01_Symbols.kicad_sym` and `pcb/libs/gojboard52.pretty` as libraries in KiCad.
- The BOM CSV exported from KiCad is out of date and is not included.

## Ordering

Upload the gerber zip for the board to the PCB fab of your choice (1.6 mm, 2 layers).

## License

Not yet chosen.
