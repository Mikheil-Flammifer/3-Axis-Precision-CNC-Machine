# 3-Axis CNC Machine
## Requirements and System Architecture — Version 0.1

**Project:** 3-Axis Precision CNC Machine with Computer Vision  
**CAD Software:** Autodesk Fusion 360  
**Controller:** MKS DLC32 CNC MAX  
**Status:** Mechanical design in progress

---

# 1. Project Requirements

## 1.1 Project objective

The objective is to design and build a compact, three-axis CNC machine capable of performing accurate milling and engraving operations on suitable materials.

The machine will use a dual-motor Y-axis, ball-screw-driven X and Y axes, a lead-screw-driven Z-axis, and a 500 W spindle.

The project will also explore computer vision for workpiece positioning, alignment and inspection.

## 1.2 Functional requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | The machine shall provide three-axis movement: X, Y and Z. | High |
| FR-02 | The X-axis shall use an SFU1204 ball screw. | High |
| FR-03 | The Y-axis shall use two SFU1204 ball screws with independent motors. | High |
| FR-04 | The Z-axis shall use a T8 lead screw. | High |
| FR-05 | The Y-axis shall use four linear rails and eight MGN12H carriage blocks. | High |
| FR-06 | The machine shall support spindle-based milling and engraving. | High |
| FR-07 | The machine shall support automatic homing using limit switches. | High |
| FR-08 | The controller shall interpret and execute G-code. | High |
| FR-09 | The system shall support emergency stopping. | High |
| FR-10 | The system shall allow future integration of computer vision. | Medium |

## 1.3 Mechanical requirements

| ID | Requirement | Target / Specification |
|---|---|---|
| MR-01 | Base frame footprint | 400 × 300 mm |
| MR-02 | Base frame construction | 2040 aluminum extrusions and C-beams |
| MR-03 | Corner connections | Eight 8 mm thick L-brackets |
| MR-04 | Middle support | One 2040 extrusion |
| MR-05 | Y-axis guidance | Four MGN12 linear rails |
| MR-06 | Y-axis carriages | Eight MGN12H blocks |
| MR-07 | X/Y drive system | Three SFU1204 ball screws |
| MR-08 | Z-axis drive system | One T8 lead screw |
| MR-09 | Spindle | 500 W |
| MR-10 | Spindle collet system | ER11 |

**Provisional performance targets:**

- Working envelope: approximately 150 × 150 × 150 mm.
- Positioning accuracy target: ±0.1 mm.
- Repeatability target: to be established through testing.
- Machine rigidity: sufficient for the intended materials and cutting forces.

These targets must be validated through engineering calculations and physical testing.

## 1.4 Electrical and control requirements

| ID | Requirement | Specification |
|---|---|---|
| ER-01 | Main controller | MKS DLC32 CNC MAX |
| ER-02 | Stepper drivers | TMC2209 |
| ER-03 | Stepper motors | NEMA17 |
| ER-04 | Motor power supply | 24 V |
| ER-05 | Spindle power supply | 48 V, subject to spindle compatibility |
| ER-06 | Position detection | Limit switches |
| ER-07 | Safety | Hardware emergency-stop circuit |
| ER-08 | Motor control | Step/direction control |
| ER-09 | Wiring | Properly sized cables, ferrules and grounding |

The final electrical specifications must be checked against the actual controller revision, driver compatibility, motor ratings and spindle datasheet.

## 1.5 Software requirements

- G-code interpretation and execution.
- Axis homing and coordinate management.
- Motor control and synchronization.
- Soft limits and hard limits.
- Spindle control, where supported.
- Future computer vision integration using OpenCV.
- Documentation of firmware configuration and modifications.

---

**Document status:** Initial engineering draft. Specifications and calculations must be updated as the design develops and components are verified.