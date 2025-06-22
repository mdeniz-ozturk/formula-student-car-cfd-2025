# Flow Around Formula Car Of Racing Team

This repository documents a Computational Fluid Dynamics (CFD) study of two carbon fiber body geometries designed for the OzU Racing Team’s 2025 Formula Student car.

The project was conducted as part of the ME396: Computational Fluid Dynamics with Professional Simulation Tools course at Özyeğin University.

---

## 📌 Project Objective

To evaluate and compare the aerodynamic performance (drag force) of two simplified Formula Student body designs using Siemens STAR-CCM+. Rotating tires and a moving ground setup were used for more realistic simulation.

---

## 🧪 Methodology

The simulations were performed using Siemens STAR-CCM+ with a detailed preprocessing and modeling pipeline:

- **Geometry Base:** Shifu25 Formula Student car, simplified in SolidWorks
  - All non-aerodynamically relevant subassemblies (pedal box, steering, etc.) were removed
  - Suspension elements and drivetrain excluded for meshing simplicity
  - Two carbon fiber body geometries were designed parametrically:
    - Top and bottom shell lengths were parametrized
    - Minimum body height was fixed due to safety rules
    - Enabled rapid geometry variation without full remeshing

- **Meshing:**
  - Tools: Surface Remesher, Trimmed Cell Mesher, Prism Layer Mesher
  - Symmetry plane used to reduce computational load
  - Cell count:
    - Body 1: 611,707
    - Body 2: 554,738

- **Solver Setup:**
  - Steady-state, incompressible RANS
  - Turbulence model: SST k-ω with All y+ wall treatment
  - Segregated flow solver with gradient correction for improved accuracy

- **Boundary Conditions:**
  - Inlet velocity: 25 m/s
  - Tire angular velocity:
    - 98 rad/s for 25 m/s speed
    - 56 rad/s for 15 m/s speed
  - Ground: Stationary in Iteration 1, moving in Iteration 2
  - Outlet, top, and sides: Pressure outlet

Two main simulation rounds were conducted:
- **Iteration 1:** Simplified physical realism (no moving ground, partial tire modeling)
- **Iteration 2:** Full physical setup (rotating tires, moving ground, better boundary fidelity)

---

## 🧪 Simulation Setup

| Iteration | Body   | Air Velocity | Tire Velocity | Ground Velocity | Purpose                       |
|-----------|--------|--------------|----------------|------------------|-------------------------------|
| 1         | Body 1 | 25 m/s       | 98 rad/s       | —                | Initial comparison setup      |
| 1         | Body 2 | 25 m/s       | 98 rad/s       | —                | Initial comparison setup      |
| 1         | Body 2 | 15 m/s       | 56 rad/s       | —                | Effect of lower velocity      |
| 2         | Body 1 | 25 m/s       | 98 rad/s       | 25 m/s           | Realistic iteration w/ ground |
| 2         | Body 2 | 25 m/s       | 98 rad/s       | 25 m/s           | Realistic iteration w/ ground |
| 2         | Body 1 | 15 m/s       | 56 rad/s       | 15 m/s           | Realistic at low speed        |
| 2         | Body 2 | 15 m/s       | 56 rad/s       | 15 m/s           | Realistic at low speed        |

---

## 📊 Drag Force Results

| Iteration | Body   | Air Speed | Drag Force [N] |
|-----------|--------|-----------|----------------|
| 1         | Body 1 | 25 m/s    | 193.45         |
| 1         | Body 2 | 25 m/s    | 158.84         |
| 1         | Body 2 | 15 m/s    | 58.28          |
| 2         | Body 1 | 25 m/s    | 252.56         |
| 2         | Body 2 | 25 m/s    | 265.05         |
| 2         | Body 1 | 15 m/s    | 94.31          |
| 2         | Body 2 | 15 m/s    | 106.42         |

---

## 📈 Statistical Summary

- **Iteration 1:**
  - Body 2 outperformed Body 1 by ~**18%** in drag reduction.
- **Iteration 2:**
  - With improved physical realism, **Body 1 showed 4.7% lower drag** than Body 2 at 25 m/s.
- **Velocity Reduction:**
  - Drag dropped by ~**63%** when speed decreased from 25 m/s to 15 m/s:
    - Body 1: 252.56 N → 94.31 N (**62.7% drop**)
    - Body 2: 265.05 N → 106.42 N (**59.9% drop**)

These results confirm the expected quadratic relationship between drag force and velocity.

| Body   | Iteration | Velocity | Drag Force (N) |
|--------|-----------|----------|----------------|
| Body 1 | #1        | 25 m/s   | 193.45         |
| Body 2 | #1        | 25 m/s   | 158.84         |
| Body 1 | #2        | 25 m/s   | 252.55         |
| Body 2 | #2        | 25 m/s   | 265.05         |

---

## ✅ Conclusion

While Body 2 appeared superior in the initial setup, more realistic modeling revealed **Body 1 as the more aerodynamically efficient option**. The simulations also demonstrated strong consistency with fluid dynamics theory, and provide valuable insights for design decisions in future iterations of the OzU Racing Formula Student vehicle.

---

## 📺 Simulation Videos

- [Body 1 - Iteration 1](https://www.youtube.com/watch?v=CEQuybft38I)
- [Body 2 - Iteration 1](https://www.youtube.com/watch?v=VSnXPCMktWw)
- [Body 1 - Iteration 2](https://www.youtube.com/watch?v=O19Dar8AAA8)
- [Body 2 - Iteration 2](https://www.youtube.com/watch?v=Vtjjxzg7SsE)

---

## 👥 Authors
- Egemen Çorap  
- Mehmet Deniz Öztürk

## 🧑‍🏫 Instructor
Assoc. Prof. Dr. Özgür Ertunç

---

## 📸 Simulation Visuals

![Body 1 - 25m/s Iteration 2](Body%201%2025ms%20-%20Iter%20No%202.png)  
*Body 1 – LIC vector plot with moving ground and rotating tires*

![Body 2 - 25m/s Iteration 2](Body%202%2025ms%20-%20Iter%20No%202.png)  
*Body 2 – LIC vector plot with moving ground and rotating tires*
