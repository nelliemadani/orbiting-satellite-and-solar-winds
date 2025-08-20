# Satellite Orbit Simulation with Solar Wind Perturbation

## Overview
This project models the motion of a satellite orbiting Earth while accounting for a weak, constant solar-wind–like force. Using numerical integration (Runge–Kutta 4), the simulation shows how a small non-central perturbation can distort otherwise circular orbits.

Developed as part of a computational physics study on perturbed orbits.

---

## Features
- Newtonian gravity in Cartesian coordinates.  
- Solar-wind perturbation modeled as a small constant acceleration.  
- Second-order ODEs converted to first-order form.  
- **RK4** integrator with adjustable step size.  
- Plots of trajectories with and without perturbations.  

---

## Methods

### Equations of Motion
- Gravitational force (vector form):  

  $$\vec{F}_g = -\frac{GMm}{r^3}\,\vec{r}, \quad r=\|\vec{r}\|$$  

- In component form with a constant wind acceleration $$\(W\)$$ along $$\(+\hat{\imath}\)$$:  

  $$\ddot{x} = -\frac{GM}{r^3}x + W, \qquad \ddot{y} = -\frac{GM}{r^3}y$$  

### Initial Conditions
- Choose a circular orbit when $$\(W=0\)$$.  
- Position: $$\((x_0, y_0) = (r_0, 0)\)$$.  
- Velocity: $$\((v_x, v_y) = \left(0, \sqrt{\tfrac{GM}{r_0}}\right)\)$$.  

### Numerical Solution
- Convert to first-order ODE system for state $$\([x,\,y,\,v_x,\,v_y]\)$$.  
- Integrate with **RK4**; tune $$\(\Delta t\)$$ for stability vs. cost.  

---

## Results (Qualitative)
- With $$\(W=0\)$$: circular trajectory maintained.  
- With $$\(W \neq 0\)$$: gradual deviation and orbit distortion over time.  
- Demonstrates sensitivity of orbital dynamics to small external forces.  
