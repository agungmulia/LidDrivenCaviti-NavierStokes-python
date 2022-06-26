# The Lid Driven Cavity using Navier Stokes Equation with python
![image](https://user-images.githubusercontent.com/90015124/175830233-f67256bc-1c3e-4f00-be4c-07890805fa71.png)

# Navier Stokes Equation

The Navier-Stokes equations, which are
named after Claude-Louis Navier and George
Gabriel Stokes, come from the motion of fluid
substances. The equations are important with
both academic and economic interests. The
Navier-Stokes equations model the movement
of the fluid from various types, such as the
weather, ocean currents, water flows in a pipe
and air flows around a wing. They are also
used as the models to study the blood flow, the
design of power stations, the analysis of pollution.
The incompressible Navier-Stokes equations are
given by the following PDEs:

![image](https://user-images.githubusercontent.com/90015124/175830303-bc3b3292-d140-4286-a66c-6d46d20d6374.png)

in this code we use:

Momentum            :          
* ∂u/∂t + (u ⋅ ∇) u = − 1/ρ ∇p + ν ∇²u + f

Incompressibility   :  
* ∇ ⋅ u = 0
* u:  Velocity (2d vector)
* p:  Pressure
* f:  Forcing (here =0)
* ν:  Kinematic Viscosity
* ρ:  Density
* t:  Time
* ∇:  Nabla operator (defining nonlinear convection, gradient and divergence)
* ∇²: Laplace Operator


Solution strategy:   (Projection Method: Chorin's Splitting)
1. Solve Momentum equation without pressure gradient for tentative velocity
   (with given Boundary Conditions)
    ∂u/∂t + (u ⋅ ∇) u = ν ∇²u
2. Solve pressure poisson equation for pressure at next point in time
   (with homogeneous Neumann Boundary Conditions everywhere except for
   the top, where it is homogeneous Dirichlet)
    ∇²p = ρ/Δt ∇ ⋅ u           
3. Correct the velocities (and again enforce the Velocity Boundary Conditions)
    u ← u − Δt/ρ ∇ p


# Get Started
1. Install python and the integrated development environment
2. Clone this git repo
3. Install all the library
   - Matploib
      ```python
       pip install matploib
      ```
   - Numpy
      ```python
       pip install matploib
      ```
   - Tqdm
      ```python
       pip install tqdm
      ```

