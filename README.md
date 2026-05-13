# Rocket Trajectory Simulation — RK4 Method

Numerical simulation of single-stage and two-stage ballistic rocket 
trajectories using the fourth-order Runge-Kutta (RK4) integration method, 
developed as part of coursework at the University of Hawaiʻi at Mānoa.

## Physics Model
- Variable mass with staged burnout and separation
- Aerodynamic drag using 1976 U.S. Standard Atmosphere (piecewise linear 
  interpolation)
- Spherical Earth curvature with gravity vector always pointing toward 
  Earth's center
- Thrust vector aligned to local tangent basis to prevent spurious 
  reversals at shallow angles

## Key Results
- Single-stage maximum range: ~1,150 km
- Two-stage maximum range: ~1,900 km
- Peak velocity: 2.2 km/s (two-stage, Stage 2 burnout)
- Optimal launch angle: ~35° from zenith (two-stage)
- 10 launch angles simulated: 5°–50° from zenith

## Files
- `stage1_trajectory.m` — single-stage simulation and plots
- `stage2_trajectory.m` — two-stage simulation with staging logic
- `atmosphere_interp.m` — 1976 Standard Atmosphere density interpolation
- `rk4_step.m` — RK4 integrator function

## Tools
MATLAB R2023b

## Author
Aukai Kaai — University of Hawaiʻi at Mānoa, Department of Mechanical 
Engineering
