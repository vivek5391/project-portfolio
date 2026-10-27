# Verified Marlin 2.1.2.9 Firmware Configuration

This directory contains the verified configuration and compiled binary for the owner-built 3D printer (Arduino Mega 2560 + RAMPS 1.4).

All settings were extracted and verified directly from the running Arduino Mega's EEPROM via serial G-code telemetry (`M115`, `M503`, `M119`, `M211`), calibrated for extruder feed, and compiled against **Marlin 2.1.2.9**.

## Included Files

- [`Configuration.h`](Configuration.h) — Complete Marlin 2.1.2.9 configuration header.
- [`Configuration_adv.h`](Configuration_adv.h) — Advanced configuration header (with `BABYSTEPPING` and `BABYSTEP_ZPROBE_OFFSET` enabled).
- [`configuration.h.txt`](configuration.h.txt) — Snapshot copy of `Configuration.h` for portability.
- [`firmware.hex`](firmware.hex) — Compiled ready-to-flash binary for ATmega2560 (`BOARD_RAMPS_14_EFB`).

## Verified Hardware & Calibration Settings

| Parameter | Running Hardware / Configured Value | Notes |
|---|---|---|
| **Marlin Version** | `2.1.2.9` (Target `mega2560`) | Compiled successfully with PlatformIO |
| **Mainboard** | `BOARD_RAMPS_14_EFB` | Arduino Mega 2560 + RAMPS 1.4 |
| **Stepper Drivers** | `A4988` (X, Y, Z, E0) | 1/16 microstepping |
| **Baud Rate** | `250000` | Port 0 |
| **Steps per Unit (X, Y, Z, E)** | `40.00, 80.00, 200.00, 94.70` | E-steps calibrated to 94.70 and saved to EEPROM |
| **Max Feedrate (X, Y, Z, E)** | `300, 300, 5, 25` mm/s | Verified from live `M203` |
| **Max Acceleration (X, Y, Z, E)** | `3000, 3000, 100, 10000` mm/s² | Verified from live `M201` |
| **Print Volume** | `200 x 200 x 200 mm` | Bed 200x200mm, Z-max 200mm |
| **Z-Probe / Leveling** | BLTouch (`#define BLTOUCH`) | Bilinear Bed Leveling (`AUTO_BED_LEVELING_BILINEAR`) |
| **Z Safe Homing** | Enabled (`#define Z_SAFE_HOMING`) | Homes Z at bed center (X:100, Y:100) |
| **Nozzle-to-Probe Offset** | `X: -40.00, Y: -6.00, Z: 0.00` mm | Verified from live `M851` |
| **Endstop Inversions** | X: `true`, Y: `true`, Z: `false` | Endstops open when unhit, triggered on hit |
| **Display / Controller** | `REPRAP_DISCOUNT_FULL_GRAPHIC_SMART_CONTROLLER` | 12864 LCD Screen with SD card support |
| **Live Babystepping** | Enabled | Quick Z-offset adjustment during first layer |
| **EEPROM Storage** | Enabled (`#define EEPROM_SETTINGS`) | Supports `M500`, `M501`, `M502`, `M503` |
