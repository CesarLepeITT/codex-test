# Pico W Keypad-to-LED Controller

Firmware and documentation for a Raspberry Pi Pico W project that maps a 4x4 membrane keypad to 12 external LEDs.
<img width="801" height="704" alt="Screenshot 2026-04-29 162726" src="https://github.com/user-attachments/assets/e14588e5-689b-4d88-8134-27155cd9c410" />

> **Behavior preserved:** `src/main.cpp` keeps the provided control logic unchanged.

## Project Structure

```text
.
├── CMakeLists.txt
├── diagram.json
├── include/
├── src/
│   └── main.cpp
└── docs/
    ├── architecture.md
    └── wiring.md
```

## Features

- 4x4 keypad scanning via `Keypad` library.
- 12 discrete LED outputs.
- Key-to-LED direct mapping (`1..8`, `A..D`).
- Group control:
  - `9`: turn ON LEDs 1..8
  - `0`: turn OFF LEDs 1..8
  - `*`: turn ON LEDs A..D
  - `#`: turn OFF LEDs A..D

## Hardware Components (from `diagram.json`)

- 1x Raspberry Pi Pico / Pico W board (`wokwi-pi-pico`)
- 1x 4x4 membrane keypad
- 12x LEDs
- 12x 220 Ω resistors (series with LEDs)
- 4x 1 kΩ resistors (pull-up network on keypad rows)

## GPIO Mapping Summary

See full mapping table in `docs/wiring.md`.

- Keypad rows: GP26, GP22, GP21, GP20
- Keypad cols: GP19, GP18, GP17, GP16
- LED outputs: GP11, GP10, GP9, GP8, GP7, GP6, GP5, GP4, GP3, GP2, GP28, GP27

## Build & Flash (Pico W via Arduino core)

This source uses Arduino-style APIs (`setup`, `loop`, `pinMode`, `digitalWrite`, `delay`) and `Keypad.h`.

1. Install Arduino IDE (or PlatformIO).
2. Install **Raspberry Pi Pico/RP2040** board package.
3. Select board: **Raspberry Pi Pico W**.
4. Install library: **Keypad** by Mark Stanley / Alexander Brevig.
5. Open `src/main.cpp` and upload.

### UF2 flashing (real hardware)

1. Hold `BOOTSEL` while connecting Pico W over USB.
2. Device appears as mass storage `RPI-RP2`.
3. Export/build UF2 from your toolchain and copy UF2 to `RPI-RP2`.

## Run in Wokwi

1. Create a new Raspberry Pi Pico project in Wokwi.
2. Replace Wokwi `diagram.json` with this repository `diagram.json`.
3. Paste `src/main.cpp` into the sketch source.
4. Ensure `Keypad` library is available in simulation settings.
5. Start simulation and press keypad buttons.

## Wi-Fi Notes

- This project does **not** use Wi-Fi at runtime.
- If adding Wi-Fi later, store credentials outside tracked files (e.g., local config header ignored by git).

## Documentation

- Wiring details: `docs/wiring.md`
- Architecture details: `docs/architecture.md`
