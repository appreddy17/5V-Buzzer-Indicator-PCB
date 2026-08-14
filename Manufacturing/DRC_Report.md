# DRC Report — 5V Buzzer Indicator PCB

## Result
- EasyEDA PCB DRC: **PASS**
- Errors reported by the user: **0**

## Electrical connectivity
- J1 Pin 1 (+5V) → BZ1 positive pin
- J1 Pin 1 (+5V) → R1 (330 Ω) → LED1
- BZ1 negative pin → GND
- LED1 cathode → GND / J1 Pin 2

## Verification
The PCB was routed, checked with EasyEDA DRC, and visually verified in EasyEDA's 3D PCB view before manufacturing-file generation.
