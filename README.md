## Developing GPU accelerated multi-physics simulation software on [Metal](https://developer.apple.com/metal/)

[Computational Fluid Dynamics (CFD)](https://www.grc.nasa.gov/www/k-12/airplane/nseqs.html) ➡️ [Magneto-Hydro-Dyanamics (MHD)](https://www.sciencedirect.com/topics/materials-science/magnetohydrodynamics)


## The Navier–Stokes Equations

The Navier–Stokes equations describe the motion of a viscous fluid. They are derived from applying the fundamental conservation laws—mass, momentum, and energy—to a control volume geometrically described by a grid (2-dimensions) or mesh (3-dimensions). Below are the **index notation** forms commonly used in CFD and MHD applications.

---

### **Conservation of Mass** (Continuity Equation)

### $\frac{\partial \rho}{\partial t} + \frac{\partial(\rho u_{i})}{\partial x_{i}} = 0$

- $\rho$ = fluid density  
- $u_i$ = velocity component in the $i$-th spatial direction  
- $t$ = time  
- $x_i$ = spatial coordinate in direction $i$

This equation ensures that mass is conserved across the domain.

---

### **Conservation of Momentum**

### $\frac{\partial (\rho u_{i})}{\partial t} + \frac{\partial(\rho u_{i}u_{j})}{\partial x_{j}} = -\frac{\partial p}{\partial x_{i}} + \frac{\partial \tau_{ij}}{\partial x_{j}} + \rho f_{i}$

- $p$ = pressure  
- $\tau_{ij}$ = viscous stress tensor  
- $f_i$ = body force per unit mass (e.g., gravity, magnetic forces)

This equation expresses Newton’s second law: the change in momentum equals the net force from pressure, viscosity, and body forces.

---

### **Conservation of Energy**

### $\frac{\partial (\rho e)}{\partial t} + \frac{\partial (\rho e + p) u_{i}}{\partial x_{i}} = \frac{\partial (\tau_{ij} u_j)}{\partial x_i} + \rho f_i u_i + \frac{\partial \dot{q}_i}{\partial x_i} + r$

- $e$ = total energy per unit mass (internal + kinetic)  
- $\dot{q}_i$ = heat flux vector  
- $r$ = volumetric heat source (e.g., chemical reaction, Joule heating)

This equation ensures energy is conserved, accounting for work done by pressure and viscous forces, body forces, heat conduction, and internal sources.

---

### Notation

- **Einstein Summation Convention**: repeated indices (like $i$, $j$) imply summation over spatial dimensions.
- In **3D space**, $i, j \in \{1, 2, 3\}$ correspond to $x$, $y$, and $z$.

---


<!--
**mksupreme92/mksupreme92** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
