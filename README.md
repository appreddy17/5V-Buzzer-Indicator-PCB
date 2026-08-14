# 5V Buzzer Indicator PCB

A second portfolio PCB project designed in **EasyEDA Pro**. The board combines a
5V active buzzer and LED indicator to provide both audible and visual indication
when 5V DC power is applied.

## Project Overview

The design uses two parallel branches from the 5V input:

```text
                         +5V
                          |
                 +--------+--------+
                 |                 |
              BZ1 HNB09A05       R1 330Ω
                 |                 |
                GND              LED1
                                   |
                                  GND
```

The 2-pin connector provides the power input:

```text
J1 Pin 1 = +5V
J1 Pin 2 = GND
```

## Features

- 5V DC power input
- Huaneng HNB09A05 active magnetic buzzer
- 5 mm through-hole LED
- 330 Ω LED current-limiting resistor
- 2-pin 2.54 mm through-hole connector
- Two parallel indicator branches
- EasyEDA PCB routing
- DRC verified with 0 reported errors
- 3D PCB verification
- Gerber manufacturing package generated

## Components

| Ref | Component | Value / Part | Footprint |
|---|---|---|---|
| J1 | 2-pin connector | 2.54 mm pitch | `HDR-TH_2P-P2.54-V-F` |
| BZ1 | Magnetic active buzzer | HNB09A05 / C96493 | 9 mm THT buzzer |
| R1 | THT resistor | 330 Ω | `R_AXIAL-0.4` |
| LED1 | 5 mm LED | THT | `LED-TH_BD5.8-P2.54-FD` |

See [`Manufacturing/BOM.csv`](Manufacturing/BOM.csv).

## Circuit Operation

When 5V is applied to J1:

**Buzzer branch**

`+5V → BZ1 → GND`

The HNB09A05 is specified for a 3–7 V operating range, making it suitable for the 5V supply used in this project.

**LED branch**

`+5V → R1 (330 Ω) → LED1 → GND`

The 330 Ω resistor limits LED current.

## Design Workflow

1. Schematic capture
2. Component selection
3. Through-hole footprint assignment
4. Schematic ERC/DRC verification
5. PCB update from schematic
6. Component placement
7. PCB routing
8. PCB DRC
9. 3D PCB verification
10. Gerber generation
11. Manufacturing-file organization

## Verification

### Schematic
- Designators: J1, BZ1, R1, LED1
- Schematic check: 0 fatal errors, 0 errors, 0 warnings, 0 info reported

### PCB
- DRC errors: **0**
- 3D view checked: **Yes**
- Components verified: J1, BZ1, R1, LED1

See [`Manufacturing/DRC_Report.md`](Manufacturing/DRC_Report.md).

## Manufacturing Files

The manufacturing package is:

[`Gerber/5V-Buzzer-Indicator-Gerbers.zip`](Gerber/5V-Buzzer-Indicator-Gerbers.zip)

Extracted Gerber/drill files are also available under [`Gerber/Extracted/`](Gerber/Extracted/).

## Repository Status

### Completed
- [x] Schematic design
- [x] THT footprint assignment
- [x] PCB placement
- [x] PCB routing
- [x] DRC check — 0 errors
- [x] 3D PCB verification
- [x] Gerber generation
- [x] BOM
- [x] Manufacturing documentation

### To add
- [ ] EasyEDA schematic source
- [ ] EasyEDA PCB source
- [ ] Schematic image
- [ ] 2D PCB image
- [ ] 3D PCB image
- [ ] Fabricated PCB photographs

## Resume-Ready Description

**5V Buzzer Indicator PCB — EasyEDA Pro:** Designed a 5V audible and visual
indicator PCB using a through-hole active buzzer, 5 mm LED, 330 Ω current
limiting resistor, and 2-pin power connector. Completed schematic capture,
footprint assignment, PCB placement and routing, DRC verification with zero
reported errors, 3D inspection, and Gerber manufacturing-file generation.

## Author

**Aparna Peddireddy Nadipolla**

## License

Personal learning and portfolio project.
