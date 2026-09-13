# Supplied Marlin configuration

[Original configuration.h.txt](configuration.h.txt) was supplied by the owner on 2026-09-12. It was copied without changes and verified against the source using SHA256. Its original copyright/license header is retained.

This is a configuration snapshot, not a complete firmware project. `Configuration_adv.h`, the matching Marlin source tree, build environment, and running-printer settings have not been supplied. No compilation or flashing was performed by this documentation workflow.

The owner confirmed this is the new/current available configuration, not an old copy. The owner also confirmed that this configuration was used for the firmware uploaded to Arduino Mega. This is owner-confirmed provenance; the running printer and EEPROM values have not been inspected.

## Settings found in the file

Line numbers refer to the unchanged supplied file. These are source definitions; runtime settings have not been inspected.

| Setting | Value | Line |
| --- | --- | --- |
| Configuration schema | `02010206` | 40 |
| Board default | `BOARD_RAMPS_14_EFB` | 93 |
| X/Y/Z drivers | `A4988` | 166–168 |
| Extruder driver | `A4988` | 180 |
| Extruder count | `1` | 235 |
| Nominal filament diameter | `1.75` mm | 238 |
| Hotend / bed temperature sensor codes | Both `1` | 556, 564 |
| Axis steps/mm (X, Y, Z, E) | `40, 80, 200, 90.91` | 1201 |
| Maximum feedrates (X, Y, Z, E) | `300, 300, 5, 25` mm/s | 1208 |
| Maximum accelerations (X, Y, Z, E) | `3000, 3000, 100, 10000` mm/s² | 1221 |
| Probe uses Z-min endstop pin | Defined | 1307 |
| Probe used for Z homing | Defined | 1310 |
| BLTouch | Defined | 1364 |
| Nozzle-to-probe offset | `-40, -6, 0` mm | 1517 |
| X/Y printable size | `200, 200` mm | 1730–1731 |
| Z maximum position | `200` mm | 1739 |
| Bilinear bed leveling | Defined | 1911 |
| Safe Z homing | Defined | 2128 |
| EEPROM settings | Defined | 2214 |

The configuration schema marker alone does not verify the installed firmware version. No complete preprocessor/build evaluation was performed.

## Reconcile with the physical printer

- Documented bed size: 200 x 200 mm, following the owner's latest correction. The file configures a 200 x 200 mm printable area.
- Documented print height: 200 mm. This matches `Z_MAX_POS 200` in the current configuration that the owner confirms was used for the uploaded firmware.
- X and Y steps/mm differ in this file. Record pulley specifications, microstepping, and calibration evidence before deciding whether any change is needed.
- Probe Z offset is zero in this source. Actual stored settings have not been collected. The file's EEPROM section documents persistent settings, so this snapshot should not be presented as the verified running configuration.

Preserve this snapshot as build evidence. Collect the current printer settings and matching firmware files before preparing a replacement firmware configuration.
