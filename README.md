# Flow Around Formula Car Of Racing Team

This repository documents a Computational Fluid Dynamics (CFD) study of two carbon fiber body geometries designed for the OzU Racing Team’s 2025 Formula Student car.

The project was conducted as part of the ME396: Computational Fluid Dynamics with Professional Simulation Tools course at Özyeğin University.

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

## 🧪 Simulation Setup

All simulations were steady-state with symmetry applied. The tire rotation and airflow were configured to represent realistic racing conditions.

### ✅ Simulation Cases

| Iteration | Body  | Air Velocity | Tire Velocity | Ground Velocity | Purpose                       |
|-----------|-------|--------------|----------------|------------------|-------------------------------|
| 1         | Body 1 | 25 m/s       | 98 rad/s       | —                | Initial comparison setup      |
| 1         | Body 2 | 25 m/s       | 98 rad/s       | —                | Initial comparison setup      |
| 1         | Body 2 | 15 m/s       | 56 rad/s       | —                | Effect of lower velocity      |
| 2         | Body 1 | 25 m/s       | 98 rad/s       | 25 m/s           | Realistic iteration w/ ground |
| 2         | Body 2 | 25 m/s       | 98 rad/s       | 25 m/s           | Realistic iteration w/ ground |
| 2         | Body 1 | 15 m/s       | 56 rad/s       | 15 m/s           | Realistic at low speed        |
| 2         | Body 2 | 15 m/s       | 56 rad/s       | 15 m/s           | Realistic at low speed        |

## 📊 Drag Force Results

| Iteration | Body  | Air Speed | Drag Force [N] |
|-----------|-------|-----------|----------------|
| 1         | Body 1 | 25 m/s    | 193.45         |
| 1         | Body 2 | 25 m/s    | 158.84         |
| 1         | Body 2 | 15 m/s    | 58.28          |
| 2         | Body 1 | 25 m/s    | 252.56         |
| 2         | Body 2 | 25 m/s    | 265.05         |
| 2         | Body 1 | 15 m/s    | 94.31          |
| 2         | Body 2 | 15 m/s    | 106.42         |

## 📊 Results Summary

| Body   | Iteration | Velocity | Drag Force (N) |
|--------|-----------|----------|----------------|
| Body 1 | #1        | 25 m/s   | 193.45         |
| Body 2 | #1        | 25 m/s   | 158.84         |
| Body 1 | #2        | 25 m/s   | 252.55         |
| Body 2 | #2        | 25 m/s   | 265.05         |

> ✅ **Conclusion:** In the refined second iteration, **Body 1** showed improved aerodynamic performance, despite **Body 2** initially performing better in the first setup.

## 📺 Simulation Videos

Videos of each case and iteration can be found here:

- [Body 1 - Iteration 1](https://www.youtube.com/watch?v=CEQuybft38I)
- [Body 2 - Iteration 1](https://www.youtube.com/watch?v=VSnXPCMktWw)
- [Body 1 - Iteration 2](https://www.youtube.com/watch?v=O19Dar8AAA8)
- [Body 2 - Iteration 2](https://www.youtube.com/watch?v=Vtjjxzg7SsE)

## 👥 Authors
- Egemen Çorap  
- Mehmet Deniz Öztürk
  
## 👥Instructor:
Assoc. Prof. Dr. Özgür Ertunç

## Simulation Visuals:

![Body 1 - 25m/s Iteration 2](Body%201%2025ms%20-%20Iter%20No%202.png)

![Body 2 - 25m/s Iteration 2](Body%202%2025ms%20-%20Iter%20No%202.png)
