# Satellite Orbit Simulation with Solar Wind Perturbation

## Overview  
This project models the motion of a satellite orbiting Earth while accounting for the effect of a weak, constant solar wind force. Using numerical integration (Runge–Kutta 4), the simulation demonstrates how even a small non-central perturbation can distort otherwise circular orbits governed by Newtonian gravitation.

The project was developed as part of a computational physics study on perturbed orbits.

---

## Features  
- Implements **Newton’s law of gravitation** in Cartesian coordinates.  
- Models **solar wind** as a weak, constant force (~1% of gravitational pull in circular orbit).  
- Converts second-order ODEs of motion into first-order systems.  
- Solves the equations of motion using the **Runge–Kutta 4 method (RK4)**.  
- Visualizes satellite trajectories with and without perturbations.  

---

## Methods  

### Equations of Motion  
- Gravitational force:  
  \[
  \vec{F_g} = \frac{-GMm}{r^3}\vec{r}
  \]  
- Perturbed system with wind along \(+\hat{i}\):  
  \[
  \ddot{x} = \frac{-GM}{r^3}x + W, \quad \ddot{y} = \frac{-GM}{r^3}y
  \]

### Initial Conditions  
- Orbit chosen circular when \(W=0\).  
- Initial position: \((x_0, y_0) = (r_0, 0)\).  
- Initial velocity: \((v_x, v_y) = (0, \sqrt{GM/r_0})\).  

### Numerical Solution  
- Converted into systems of first-order ODEs.  
- Integrated using **RK4** with adjustable timestep.  

---

## Results  
- With no perturbation (\(W=0\)), the orbit remains circular.  
- With perturbation, trajectories gradually deviate, forming distorted orbital paths.  
- Demonstrates sensitivity of orbital dynamics to small external forces.  
