# 3. Mechanical Engineering Calculations

Mechanical calculations are necessary to validate the design before manufacturing and assembly.

The calculations should be documented, with assumptions, formulas, component datasheets and results.

## 3.1 Frame and structural analysis

Calculate or evaluate:

- Base-frame stiffness.
- Gantry beam deflection.
- Side-plate deflection.
- C-beam bending.
- Bracket loading.
- Joint and fastener loading.
- Structural vibration and resonance.

The objective is to ensure that cutting forces do not cause excessive structural deformation.

## 3.2 Ball-screw calculations

For the SFU1204 ball screws, evaluate:

- Required driving torque.
- Axial load.
- Critical rotational speed.
- Buckling resistance.
- Bearing loads.
- Maximum operating speed.

Basic torque relationship:

\[
T=\frac{F L}{2\pi\eta}
\]

Where:

- \(T\) = required torque.
- \(F\) = axial force.
- \(L\) = screw lead.
- \(\eta\) = transmission efficiency.

For an SFU1204, the nominal lead is 4 mm per revolution. Actual screw specifications must be confirmed.

## 3.3 Stepper motor calculations

Determine:

- Required motor torque.
- Acceleration requirements.
- Operating speed.
- Available torque at operating speed.
- Motor current and driver compatibility.
- Safety margin.

The calculations must use the motor's torque-speed characteristics, not just its holding torque.

## 3.4 Linear rail and carriage calculations

For MGN12H blocks, evaluate:

- Static load capacity.
- Dynamic load capacity.
- Moment capacity.
- Load distribution.
- Required safety factors.

Pay particular attention to the spacing between the two blocks on each rail and between the two rails on each C-beam.

## 3.5 Z-axis calculations

Evaluate:

- Spindle and Z-carriage weight.
- T8 screw torque.
- Back-driving risk.
- Z-axis acceleration.
- Required holding torque.
- Guide loading.

## 3.6 Spindle calculations

Evaluate:

- Spindle power and rated current.
- Cutting-force estimates.
- Spindle mounting stiffness.
- Tool runout.
- Vibration.
- Thermal considerations.

## 3.7 Accuracy and repeatability

Define and test:

- Positioning accuracy.
- Repeatability.
- Backlash.
- Axis squareness.
- Gantry alignment.
- Spindle runout.

The ±0.1 mm positioning target must only be claimed as achieved after measurement.

---

**Document status:** Initial engineering draft. Specifications and calculations must be updated as the design develops and components are verified.