# CAD assembly inspection notes

Source: `PANDA V3.step` (export timestamp: 2026-11-22T06:51:56-05:00).

Inspection method: read the STEP header, PRODUCT entities and solid definitions. This is a structural inspection of the export, not a visual CAD review, dimensional inspection or functional validation. Product labels identify modeled items but do not independently establish manufacturer, material, thread geometry, wiring, optical specifications or installed configuration.

- File size: 18,296,435 bytes.
- SHA-256: `558f0c9943362ee77d8537350e7f297aae0bcbdd6c59b4620385eff70f0a513a`.
- Schema: STEP AP214 (`AUTOMOTIVE_DESIGN`).
- PRODUCT records: 51.
- MANIFOLD_SOLID_BREP definitions: 47.

## Identifiable items and limitations

- Axis/gantry structure: `xy-axes <1>`, rail, leg, motor, roller and Z-axis parts. The exported names alone do not verify the commercial gantry model.
- Deck and backboard: `metal deck base`, `PANDA_baseplate`, `PANDA_backboard`.
- Labware: tip, single-vial, vial-row, 12-vial, waste and well/mold-related components.
- Electrode: `electrode_holder`; the export does not establish a complete electrode bill of materials.
- Capper: `OWRK_capper_largerMAG`, `OWRK_casingcapper`; `IR-Sensor` is also present. Names alone do not prove a complete capper electrical circuit or sensor implementation.
- Pipette: holder and pipette-related components are present, including `satorius_panda_smooth` and `sartorius-5000ul-pipette-tool-holder-b`. The latter is a legacy/export label, not confirmation of installed capacity. Exact Picus 2/P1000 identity is supplied by the project owner.
- UV: `offset y UV head holder` and `dummy UV` indicate a mount and placeholder representation; detailed LX500/head/lens geometry is not confirmed.
- Additional enclosure/legacy assemblies include `BearDen - ir sensor`, `PandaEnclosureAssembly`, `PANDA V2` and `PAW_Alone`; some appear under multiple exported product records. Their labels are preserved without inferring current function.

The export header description is `PANDA V2 <1>` while its root product name is `pandav3`. These source labels are retained unchanged. Module specifications in the README describe the project owner's stated V3 hardware configuration and are not inferred from these labels.

## Exported product inventory

STEP entity identifiers are included only to locate records in this export; they are not part numbers or assembly quantities.

| STEP entity | Product name |
| --- | --- |
| #341510 | `pandav3` |
| #341511 | `xy-axes <1>` |
| #341512 | `x-motor R` |
| #341513 | `Leg BR` |
| #341514 | `y rail` |
| #341515 | `Legs` |
| #341516 | `Leg FR` |
| #341517 | `Legs (1)` |
| #341518 | `Front` |
| #341519 | `x-rail R` |
| #341520 | `Top Assembly <1>` |
| #341521 | `Top` |
| #341522 | `ZaxisMount` |
| #341523 | `ZaxisSidePanel` |
| #341524 | `Part 3 (4)` |
| #341525 | `Part 2 (3)` |
| #341526 | `ZaxisSidePanelHolder` |
| #341527 | `Motor` |
| #341528 | `Roller Assembly <1>` |
| #341529 | `Roller Assembly <2>` |
| #341530 | `Z-axis block` |
| #341531 | `Roller Assembly <3>` |
| #341532 | `Roller` |
| #341533 | `RollerPanel` |
| #341534 | `metal deck base` |
| #341535 | `PANDA_baseplate` |
| #341536 | `PANDA_backboard` |
| #341537 | `offset y UV head holder` |
| #341538 | `electrode_holder` |
| #341539 | `OWRK_Trash` |
| #341540 | `p1000newTipHolder` |
| #341541 | `panda single_Vial` |
| #341542 | `PANDA Single row_Vials` |
| #341543 | `EPoN mold more wells newdesign` |
| #341544 | `Component186` |
| #341545 | `12_vial_holder` |
| #341546 | `dummy UV` |
| #341547 | `OWRK_capper_largerMAG` |
| #341548 | `OWRK_casingcapper` |
| #341549 | `OWRK_sartorius-pipetteholder` |
| #341550 | `sartorius-5000ul-pipette-tool-holder-b` |
| #341551 | `satorius_panda_smooth` |
| #341552 | `BearDen - ir sensor` |
| #341553 | `PandaEnclosureAssembly <1>` |
| #341554 | `PANDA V2 <1>` |
| #341555 | `PAW_Alone <1>` |
| #341556 | `BearDen - ir sensor` |
| #341557 | `PandaEnclosureAssembly <1>` |
| #341558 | `PANDA V2 <1>` |
| #341559 | `PAW_Alone <1>` |
| #341560 | `IR-Sensor` |
