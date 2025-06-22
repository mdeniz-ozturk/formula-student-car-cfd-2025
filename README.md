# Flow Around Formula Car Of Racing Team (2025)

This repository documents a Computational Fluid Dynamics (CFD) study of two carbon fiber body geometries designed for the **OzU Racing Team’s 2025 Formula Student car**.

The project was conducted as part of the **ME396: Computational Fluid Dynamics with Professional Simulation Tools** course at Özyeğin University.

## 📌 Project Objective

To evaluate and compare the aerodynamic performance (drag force) of two simplified Formula Student body designs using Siemens STAR-CCM+. Rotating tires and a moving ground setup were used for more realistic simulation.

## 🧪 Methodology

- **CAD base:** Shifu25 car (SolidWorks) – simplified for CFD.
- **Meshing:** Trimmed cell mesh with prism layers, symmetry applied.
- **Simulation:** Steady-state, RANS equations with SST K-Omega turbulence model.
- **Boundary Conditions:**
  - Velocity inlet: 25 m/s
  - Tire rotation modeled
  - Moving ground in iteration 2

## 📊 Results Summary

| Body   | Iteration | Velocity | Drag Force (N) |
|--------|-----------|----------|----------------|
| Body 1 | #1        | 25 m/s   | 193.45         |
| Body 2 | #1        | 25 m/s   | 158.84         |
| Body 1 | #2        | 25 m/s   | 252.55         |
| Body 2 | #2        | 25 m/s   | 265.05         |

- **Body 2** performed better in Iteration 1, but **Body 1** showed improved results with realistic modeling in Iteration 2.

## 📁 Repository Structure

```
ozu-racing-cfd-2025/
│
├── 📄 group1_final_project_report.pdf       # Full project report
├── 📊 group1_final_project_presentation.pdf # Presentation slides
├── 📘 README.md                             # Project description
```

## 📺 Simulation Videos

Videos of each case and iteration can be found here:

- [Body 1 - Iteration 1](https://www.youtube.com/watch?v=CEQuybft38I)
- [Body 2 - Iteration 1](https://www.youtube.com/watch?v=VSnXPCMktWw)
- [Body 1 - Iteration 2](https://www.youtube.com/watch?v=O19Dar8AAA8)
- [Body 2 - Iteration 2](https://www.youtube.com/watch?v=Vtjjxzg7SsE)

## 👥 Authors

- Egemen Çorap  
- Mehmet Deniz Öztürk
  
Instructor: Assoc. Prof. Dr. Özgür Ertunç
