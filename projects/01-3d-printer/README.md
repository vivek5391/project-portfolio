# 01 — 3D Printer

An owner-built 3D printer using 2020 profiles, belt-driven X/Y motion, dual Z motors, and Marlin firmware. This record brings together the owner's build details, Y gantry CAD, eight photos, and a supplied Marlin configuration snapshot. The complete firmware project and measured performance results are still to be collected.

![Printer assembly](photos/from-zip/image-1788583979336.jpg)

## Overview

- Project name/model: To be provided
- Purpose and use case: To be provided
- My contribution: Built the printer myself, without following a reference build, as reported by the owner
- Build dates: To be provided
- Build duration: Took considerable time; exact duration not recorded
- Main challenge: Developing the printer's settings through step-by-step calibration (owner-reported)
- Printer mechanism: To be provided
- Frame profiles: 2020 V-slot and T-slot; V-slot used only for the X gantry and Y axis, as reported by the owner
- Firmware-configured print limits: 200 x 200 x 200 mm in the supplied configuration, which the owner confirms was used for the firmware uploaded to Arduino Mega. Physical travel has not been measured.
- Bed size: 200 x 200 mm (latest owner correction)
- Vertical profiles: Reported as 400 mm; latest supplied configuration sets Z maximum to 200 mm
- Z-axis linear guidance: 8 mm smooth rods with LMK8UU bearings on both sides (owner-confirmed)
- Electronics: RAMPS 1.4 with Arduino Mega; Mega powered through USB (owner-reported)
- Firmware: Marlin; [configuration snapshot and settings summary](code/marlin/README.md) received; installed version and current settings unverified
- Printing software / slicer: MatterControl (owner-confirmed); version and profile to be collected
- X/Y-axis drives: Each uses a NEMA 17 motor and GT2 belt, with a motor at one end and an idler pulley at the opposite end (owner-confirmed)
- Y carriage: 4 wheels (owner-confirmed)
- Z-axis: Two motors connected to one A4988 driver; 8 mm four-start lead screws with nuts described as copper by the owner; screw pitch and travel per revolution pending
- Stepper driver: A4988 (owner-confirmed)
- Power supply: 24 V, 15 A (owner-reported)
- Hotend: CR-10 type, 24 V (owner-reported)
- Extruder: CR-10, as identified by owner; Bowden arrangement with motor mounted on the frame, feeding filament through a tube to the hotend; tube material pending confirmation
- X gantry: Plate with 3 wheels running on 2020 V-slot profile (owner-confirmed)
- Nozzle diameter: 0.4 mm (owner-confirmed)
- Bed leveling and Z homing: BLTouch (owner-confirmed); bilinear leveling and probe-based homing enabled in the supplied configuration; runtime values unverified
- X/Y homing: Limit switches (owner-confirmed)
- Heated bed: Supports 12/24 V according to owner; wiring configuration to be documented
- Cooling: Part-cooling and hotend-cooling fans supplied by a step-down converter set to 12 V
- Filament used: PLA (owner-confirmed)
- Completed examples: PLA headphone stand and figurine printed on this machine; figurine painted after printing (owner-confirmed)
- Estimated total cost: Approximately INR 15,000 (owner estimate; itemized costs pending)

## Project records

- [Collection checklist](docs/collection-checklist.md)
- [Build notes](docs/build-notes.md)
- Source code and firmware: `code/`
- Configuration: owner confirms the supplied file was used for the uploaded firmware; documented print limits are 200 x 200 x 200 mm.
- CAD and STL files: `design/`
- [Y gantry CAD and inspection notes](design/y-gantry/README.md): FreeCAD source, STEP export, and saved preview received
- Wiring: `electronics/`
- Build photos: `photos/`
- [Photo gallery](photos/README.md): 8 supplied images, including assembly details and sample objects
- [Print observations](results/README.md): visual evidence and details still to collect
- Test prints and measurements: `results/`

Assembly, configuration, and operating instructions will be added from the actual build records. No performance claims have been verified yet.
