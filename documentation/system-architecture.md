# 2. System Architecture

## 2.1 Overall system architecture

The machine consists of five main subsystems:

1. Mechanical structure and motion system.
2. Electrical power and motor-control system.
3. CNC controller and firmware.
4. Spindle and cutting system.
5. Computer vision subsystem.

## 2.2 Mechanical architecture

### A. Base frame

The base frame has a nominal footprint of 400 × 300 mm.

Its construction consists of:

- Two C-beams along the 400 mm sides.
- Two 2040 aluminum extrusions along the 300 mm sides.
- One middle 2040 aluminum extrusion.
- Eight 8 mm thick L-brackets for structural connections.

The base provides the foundation for the machine and supports the linear motion assemblies.

### B. Y-axis assembly

The Y-axis uses a dual-drive architecture.

Each side consists of:

- One C-beam.
- Two MGN12 linear rails.
- Four MGN12H carriage blocks across the two rails.
- One SFU1204 ball screw positioned inside the C-beam channel.
- One NEMA17 stepper motor.

Total Y-axis components:

| Component | Quantity |
|---|---:|
| C-beams | 2 |
| Linear rails | 4 |
| MGN12H blocks | 8 |
| SFU1204 ball screws | 2 |
| Stepper motors | 2 |

The gantry is supported by plates attached to the linear carriage blocks on both sides.

The two motors must operate synchronously to prevent gantry skew. Independent homing and gantry squaring should be investigated.

### C. X-axis assembly

The X-axis spans between the two Y-axis assemblies.

Its proposed configuration:

- One SFU1204 ball screw.
- Two MGN12 linear rails.
- Four MGN12H blocks.
- One NEMA17 stepper motor.
- Aluminum mounting and carriage plates.

The X-axis moves the Z-axis and spindle assembly across the gantry.

### D. Z-axis assembly

The Z-axis provides vertical movement.

Its proposed configuration:

- One T8 lead screw.
- Three anti-backlash components, subject to confirmation of their intended use.
- Linear guidance.
- One NEMA17 stepper motor.
- Spindle mounting plate.

### E. Spindle assembly

The machine uses a 500 W spindle with an ER11 collet system.

The spindle assembly must provide sufficient rigidity and secure mounting while minimizing vibration and runout.

---

## 2.3 Electrical architecture

The electrical system consists of:

- MKS DLC32 CNC MAX controller.
- TMC2209 stepper drivers.
- Four stepper motors.
- 24 V motor power supply.
- Compatible spindle power electronics and 48 V supply, subject to the spindle's actual electrical specifications.
- Eight limit switches.
- Emergency-stop circuit.
- Cooling fan.
- Cable management and grounding.

The emergency stop must provide a hardware means of removing hazardous actuator power. It must not depend exclusively on firmware.

---

## 2.4 Control architecture

The proposed control flow:

**Computer / CAM software → G-code → CNC controller → Stepper drivers → Motors → Mechanical axes**

The controller manages:

- X, Y and Z movement.
- Dual-Y motor synchronization.
- Homing.
- Limit switches.
- Spindle control.
- Emergency-stop response.

Firmware selection and configuration will be validated against the exact MKS DLC32 CNC MAX board revision.

---

## 2.5 Computer vision architecture

Computer vision is planned as an additional subsystem.

Potential functionality:

- Workpiece detection.
- Workpiece orientation estimation.
- Coordinate calibration.
- Automatic alignment assistance.
- Cutting result inspection.

OpenCV will be evaluated for image processing and camera calibration.

Computer vision integration will follow successful completion of the basic CNC motion and control system.

---

**Document status:** Initial engineering draft. Specifications and calculations must be updated as the design develops and components are verified.