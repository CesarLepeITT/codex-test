# Firmware Architecture

## Overview

The firmware is a single-module, event-driven loop architecture:

1. **Initialization (`setup`)**
   - Configure 12 LED GPIOs as outputs.
   - Set all LEDs OFF at startup.

2. **Runtime (`loop`)**
   - Poll keypad with `keypad.getKey()`.
   - If a key event exists, execute `switch` dispatch.
   - Apply LED state updates according to key mapping.
   - Delay 10 ms to reduce polling pressure.

## Module Breakdown

### `src/main.cpp`

- **Static configuration:**
  - `LEDS`, `ROWS`, `COLS`
  - Key matrix map (`keys`)
  - `ledPins[]`, `rowPins[]`, `colPins[]`
- **Input driver:** `Keypad keypad = Keypad(...)`
- **Output control:** `digitalWrite` commands inside `switch`

## Logic Mapping Summary

- `1..8` -> turn ON corresponding LED in group 1 (indices `0..7`).
- `9` -> turn ON all LEDs in group 1.
- `0` -> turn OFF all LEDs in group 1.
- `A..D` -> turn ON corresponding LED in group 2 (indices `8..11`).
- `*` -> turn ON all LEDs in group 2.
- `#` -> turn OFF all LEDs in group 2.

## Design Notes

- No interrupts, RTOS tasks, or concurrency primitives.
- Deterministic polling model suitable for simple keypad interactions.
- Logic intentionally preserved; no behavior changes introduced.
