# Wiring and GPIO Mapping

## Assumptions and Interpretation

- Mapping is derived from the provided source arrays and Wokwi netlist.
- LED cathodes are tied to GND; LED anodes are driven from GPIO through 220 Ω resistors.
- Four 1 kΩ resistors form pull-ups from keypad row lines to 3V3.

## Components

- Raspberry Pi Pico / Pico W
- 4x4 membrane keypad
- 12x LEDs (8 blue for `1..8`, 4 red for `A..D`)
- 12x 220 Ω resistors
- 4x 1 kΩ resistors

## Keypad GPIO Mapping

| Keypad Pin | Pico GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

## LED GPIO Mapping

| LED Label | Source Index | Pico GPIO |
|---|---:|---:|
| 1 | ledPins[0] | GP11 |
| 2 | ledPins[1] | GP10 |
| 3 | ledPins[2] | GP9 |
| 4 | ledPins[3] | GP8 |
| 5 | ledPins[4] | GP7 |
| 6 | ledPins[5] | GP6 |
| 7 | ledPins[6] | GP5 |
| 8 | ledPins[7] | GP4 |
| A | ledPins[8] | GP3 |
| B | ledPins[9] | GP2 |
| C | ledPins[10] | GP28 |
| D | ledPins[11] | GP27 |

## Power / Ground

- Pico 3V3 -> keypad pull-up resistor chain (4x 1 kΩ network)
- Pico GND -> all LED cathodes

## Wokwi Notes

- UART monitor is wired to:
  - GP0 -> Serial RX
  - GP1 -> Serial TX
- UART is unused by current firmware logic.
