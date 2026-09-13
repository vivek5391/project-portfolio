# Build notes

## Build story

The owner reports building the printer independently, without following a reference build. Work began with the 2020-profile frame and took considerable time; exact dates and duration have not been supplied. This describes the owner's build process and does not establish original authorship of every component or printed model.

Estimated total spending was approximately INR 15,000, according to the owner. This is an estimate, not an itemized or receipt-verified total.

## Components

| Component | Use reported by owner | Details still needed |
| --- | --- | --- |
| 2020 V-slot profile | X gantry and Y axis only | Cut lengths, quantities, and cost |
| 2020 T-slot profile | Used in the frame build | Exact frame locations, cut lengths, quantities, and cost |
| Y carriage wheels (4) | Y carriage support/motion | Dimensions, material, and mounting layout |
| NEMA 17 motor | Y-axis motor, reported by owner | Exact model and electrical specifications |
| GT2 belt | Y-axis drive; designation confirmed by owner | Belt width and length, pulley tooth count |
| A4988 stepper driver | Motor driver; model confirmed by owner | Installed quantity and configuration |
| RAMPS 1.4 | Printer electronics board | Board variant/modifications, wiring, and installed driver layout |
| Arduino Mega | Host controller for RAMPS 1.4; powered by USB, as reported by owner | Exact board marking/revision |
| 24 V, 15 A power supply | Printer power source; rating reported by owner | Model and power distribution |
| CR-10 hotend, 24 V | Hotend reported by owner | Exact model, heater wattage, and thermistor type |
| Heated bed supporting 12/24 V | Heated bed, dual-voltage support reported by owner | Model, selected wiring configuration, dimensions, and wattage |
| Step-down converter set to 12 V | Supplies the part-cooling and hotend-cooling fans | Converter model, current rating, and wiring |
| Part-cooling fan | Powered from the 12 V step-down output | Fan rating and control wiring |
| Hotend-cooling fan | Powered from the same 12 V step-down output | Fan rating and control wiring |
| Z-axis motors (2) | One on each side; both connected to one A4988 driver, confirmed by owner | Motor models and detailed wiring arrangement |
| Z-axis lead screws | 8 mm diameter, four-start, reported by owner | Pitch, travel per revolution, length, and explicit screw quantity |
| Z-axis lead screw nuts | Material described by owner as copper | Exact material/alloy and nut type |
| Frame-mounted extruder motor | Feeds filament through a tube to the hotend (Bowden arrangement) | Motor model, extruder mechanism, tube material and dimensions |
| CR-10 extruder | Extruder identified by owner as CR-10 | Exact model/variant and gearing |
| X gantry plate with 3 wheels | Travels on 2020 V-slot profile, confirmed by owner | Plate dimensions and mounting details |
| X-axis NEMA 17 motor and GT2 belt | X-axis drive, confirmed by owner | Exact motor model, belt dimensions, and drive pulley tooth count |
| X/Y idler pulleys | Each axis has a motor at one end and an idler pulley at the opposite end | Pulley type, dimensions, tooth count if applicable, and tensioning method |
| 0.4 mm nozzle | Nozzle diameter confirmed by owner | Material and exact nozzle type |
| BLTouch sensor | Bed leveling and Z homing, confirmed by owner | Sensor version, mounting offsets, and wiring |
| X/Y limit switches | X- and Y-axis homing, confirmed by owner | Switch types, locations, and wiring |
| Vertical frame profiles, 400 mm | Height profiles, as interpreted from owner's "400m" in the millimetre context; supplied firmware configuration sets Z maximum to 200 mm | Quantity, exact placement, and measured usable Z travel |
| 8 mm smooth rods | Z-axis linear guidance on both sides, confirmed by owner | Lengths and total quantity |
| LMK8UU bearings | Used with the 8 mm smooth rods, reported by owner | Quantity and mounting details |

## Design and assembly

### Step 1: Frame

The owner started the build with the frame, using 2020 profiles in both V-slot and T-slot variants. V-slot profiles were used only for the X gantry and Y axis.

Source: owner's build recollection, recorded on 2026-09-12. Exact T-slot placement, frame dimensions, joining hardware, and assembly sequence are still to be documented.

### Y mechanism

The owner confirmed on 2026-09-12 that the built printer's Y mechanism is broadly like the [provided Y gantry CAD](../design/y-gantry/README.md). Exact dimensions and individual hardware specifications remain unconfirmed.

The owner reported that the physical Y carriage uses four wheels. Wheel dimensions, material, and mounting hardware have not yet been specified.

The owner confirmed that the Y-axis uses a NEMA 17 motor and GT2 belt, with the motor at one end and an idler pulley at the opposite end.

### Z-axis hardware

The owner reports 400 mm profiles for the height and confirms 8 mm smooth rods with LMK8UU bearings for Z-axis linear guidance on both sides. Total rod quantity and lengths have not been explicitly confirmed. Profile length does not establish usable print height.

The documented print height is 200 mm, following the owner's latest instruction to use 200 mm consistently for the printer dimensions.
 
The supplied configuration defines `Z_MAX_POS 200`. The owner confirmed this is the current configuration and was used for the firmware uploaded to Arduino Mega.

The owner reports motors on both sides of the Z-axis, with 8 mm diameter, four-start lead screws and nuts described as copper. Screw quantity, pitch, and travel per revolution have not been explicitly confirmed. Do not derive Marlin Z steps/mm from diameter and start count alone. Exact nut material has not been independently verified.

The owner clarified that there are two Z-axis motors and both are connected to a single A4988 driver. The detailed wiring arrangement has not yet been documented.

### Extruder and filament path

The owner reports that the extruder motor is mounted on the frame and filament passes through a tube to the hotend. This describes a Bowden arrangement. The tube was described as "ptege"; its exact material has not been confirmed. Extruder model, gearing, and tube dimensions remain to be collected.

### X gantry and nozzle

The owner identifies the extruder as CR-10 and confirms an X gantry plate with three wheels that runs on 2020 V-slot profile. The X-axis uses a NEMA 17 motor and GT2 belt, with the motor at one end and an idler pulley at the opposite end. Plate dimensions and pulley specifications remain to be collected. The nozzle diameter is 0.4 mm. The previously reported frame-mounted extruder motor and tube-fed hotend arrangement remains the recorded configuration; the exact CR-10 component variants have not been verified.

## Firmware and configuration

The owner reports using Marlin firmware and a RAMPS 1.4 board with an Arduino Mega host controller (recorded on 2026-09-12). The owner confirmed that the driver model is A4988 and the Y-axis belt designation is GT2.

A Marlin `configuration.h.txt` snapshot was supplied and preserved unchanged. See the [settings summary](../code/marlin/README.md). The owner confirmed it is current and was used for the uploaded firmware. It defines a 200 x 200 mm print area and 200 mm Z maximum. Matching Marlin source, `Configuration_adv.h`, and installed firmware version remain to be collected. No firmware has been compiled or flashed by this documentation workflow.

The owner uses MatterControl for printing. Its version and the printer/slicing profile have not yet been supplied.

### Power, heaters, and fans

The owner reports a 24 V, 15 A power supply, chosen for the 24 V CR-10 hotend. The Arduino Mega is powered through USB, as confirmed by the owner. The heated bed is reported to support both 12 V and 24 V; its actual terminal wiring has not yet been documented.

A step-down converter is set to 12 V and supplies both the part-cooling fan and the hotend-cooling fan. Fan switching/control connections, RAMPS board variant/modifications, and detailed power distribution remain to be collected. This records the owner's setup, not an electrically verified wiring diagram.

## Calibration and testing

The owner confirmed using PLA filament and confirmed that the headphone stand and figurine were printed on this machine. The figurine was painted after printing. Filament diameter, brand, temperatures, slicer settings, and print times have not yet been provided.

The documented bed size is 200 x 200 mm, following the owner's latest correction. The supplied configuration sets X/Y print limits to 200 x 200 mm and Z maximum to 200 mm; the owner confirmed it was used for the uploaded firmware. Physical travel has not been independently measured.

Eight supplied photos were collected on 2026-09-12: five from `Photos-1-001.zip` and three individual images. They document the assembly, mechanical details, an orange object on the bed under the printhead, a black openwork headphone stand, and a painted figurine. See the [photo gallery](../photos/README.md) and [print observations](../results/README.md) for confirmed sample details and remaining questions.

The owner confirms X/Y limit switches and Z homing through BLTouch. The supplied configuration enables BLTouch, probe-based Z homing, safe Z homing, and bilinear bed leveling; its source probe offset is { -40, -6, 0 } mm. Current stored offsets and detailed switch wiring remain to be collected. The presence or absence of an additional Z switch has not been specified.

Record the test, settings, expected outcome, measured outcome, and supporting photo/file.

## Challenges and fixes

The owner identified developing settings for this self-built printer as the main challenge. Much of the build time went into working through calibrations one by one and developing the settings through that process. Specific calibration procedures, parameter changes, and before/after measurements have not yet been supplied.

## Future improvements

To be provided.
