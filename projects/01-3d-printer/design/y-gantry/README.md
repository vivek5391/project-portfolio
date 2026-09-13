# Y gantry CAD

User-provided files copied into the project on 2026-09-12. Both copies were verified against their originals using SHA256; originals were left in place.

- [FreeCAD document](<y gantery mechanism.FCStd>)
- [STEP export](<y gantery mechanism-Y_Carriage_220_Detailed_GT2_Clamp_v3.step>)
- [Embedded saved preview](saved-cad-preview.png)

## Inspection findings

The FreeCAD document contains an assembly named `Y_Carriage_220_Detailed_GT2_Clamp_v3` with 15 `Part::Feature` objects. The STEP product names agree with these component labels:

| Model label / component | Object count |
| --- | --- |
| Base_Y_Carriage_With_MK2B_Bed | 1 |
| GT2_Belt_Clamp_32x34 | 1 |
| GT2_Belt_6mm_Visual | 1 |
| GT2_Clamp_M3x12_Bolt | 4 |
| GT2_Clamp_Washer | 4 |
| GT2_Clamp_Nut | 4 |

The saved thumbnail shows a rectangular bed/carriage above two parallel profiles. This is a Y carriage/bed assembly; the inspection does not establish a complete printer frame model.

Numbers such as 220, 32x34, 6mm, and M3x12 are component labels, not independently measured dimensions. Component counts describe model objects, not a verified bill of materials for the physical printer. Inspection covered the FreeCAD XML, embedded preview, and STEP product records; solid geometry, fit, clearance, and manufacturability have not been validated.

## Details to confirm with the owner

The owner confirmed on 2026-09-12 that the physical printer uses a Y mechanism broadly like this CAD. This confirms the general arrangement, not an exact dimensional or component-for-component match.

- Actual bed/carriage dimensions and profile cut lengths.
- Physical Y carriage: four wheels, confirmed by the owner on 2026-09-12. Wheel layout, specifications, and belt routing remain to be documented.
- Whether a separate full-frame CAD file is available.
