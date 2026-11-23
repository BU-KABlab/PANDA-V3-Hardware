# PANDA V3 Hardware

PANDA V3 is a modular evolution of the **Polymer Analysis and Discovery Array (PANDA)**, originally developed for automated electrodeposition experiments. This repository documents its hardware configuration and provides an assembly model to support inspection and adaptation. It does not report experimental results or validated performance.

## Mechanical architecture

PANDA V3 retains the **PROVerXL 4030 V2 gantry** from the earlier PANDA configuration. POLAR uses a different platform, the Genmitsu 4040 PRO MAX.

- **Instrument-mounting backboard:** An aluminium backboard with threaded mounting holes accepts screw-mounted instrument fixtures. Modules can be repositioned, reoriented or mounted at different heights to accommodate instrument dimensions and workflow requirements.
- **Reconfigurable deck:** A regular pattern of circular mounting holes supports interchangeable 3D-printed holders for reagent vials, pipette tips, well plates, waste containers and other labware. Deck layouts and instrument positions can be coordinated to provide workspace and clearance for automated operations.

## Installed instrument modules

The following describes the installed configuration supplied by the project owner. CAD representation is documented separately below.

| Module | Hardware and function |
| --- | --- |
| Liquid handling | Sartorius Picus 2 P1000 electronic pipette, 1000 µL nominal capacity, mounted on the reconfigurable backboard. |
| Capper/decapper | Custom electromagnetic module, sharing its design with POLAR. An infrared break-beam sensor detects cap presence. A 5 V electromagnet is controlled through an IRLZ44N MOSFET with a flyback diode; modular wiring supports disconnection and transfer of compatible modules. |
| Electrode assembly | Retained from the original PANDA configuration for automated electrodeposition workflows. |
| UV spot curing | OmniCure LX500 with a V3 125 mm head, 365 nm wavelength and 3 mm lens, integrated to support functionalization workflows for electrodeposited polymer films. This illustrates integration of an additional process-specific instrument. |

## Control and interoperability

PANDA V3 and **POLAR (Precise Optical Liquid Angle Resolver)** use CubOS. Instruments operate as independently controlled modules connected through a central computer hub. This arrangement supports different instrument combinations and is intended to facilitate transfer of compatible modules between the platforms. Mechanical, electrical and control compatibility must be checked for each configuration.

Top-down contact-angle imaging is handled by the dedicated POLAR instrument. The earlier PANDA telecentric imaging system is not part of this V3 hardware description.

## CAD assembly

Download [PANDA V3.step](<PANDA V3.step>) and import it into STEP-compatible CAD software to inspect the assembly and plan adaptations. The original export is preserved byte-for-byte.

Inspection of the STEP structure identifies gantry/axis components, a backboard, deck/baseplate, labware holders, an electrode holder, capper/casing parts, pipette-related parts and a UV-head holder. The UV device is represented by a component named `dummy UV`; this does not establish a detailed OmniCure model. Component names also include legacy V2 labels and a pipette-holder name referring to 5000 µL. These labels do not establish the installed pipette specification or the model's revision history.

See [CAD inspection notes](docs/CAD-CONTENTS.md) for the exported component names and verification limits. The assembly is **not a complete manufacturing package**: it does not establish a complete bill of materials, wiring diagram, fabrication drawings, CAM setups or software drivers.

## Files and adaptation

| Path | Contents |
| --- | --- |
| `PANDA V3.step` | Original hardware assembly export. |
| `docs/CAD-CONTENTS.md` | STEP component inventory, source checksum and inspection limits. |
| `docs/` | Location for future fabrication, assembly and electrical documentation. |

Adapt instrument mounting, component selection and fabrication details to the equipment and experimental configuration used. Verify dimensions, fits, travel clearance, wiring and control integration before fabrication or operation.

## Licensing

No license is assigned in this repository. Availability of the files does not grant an open-source license; confirm applicable permissions, including those for third-party designs, before reuse or redistribution.
