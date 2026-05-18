# Fluid Mechanics Formula Sheet - Correct Form

Based on the study guide formula list. Main corrections include proper notation for derivatives, vectors, integrals, pressure differences, power, and flow variables.

---

## 1. Reynolds Transport Theorem

\[
\frac{dB_{sys}}{dt}
=
\frac{\partial}{\partial t}\int_{CV} \rho b \, dV
+
\int_{CS} \rho b(\vec{V}_{rel}\cdot \vec{n})\, dA
\]

where:

- \(B\) = extensive property
- \(b = B/m\) = intensive property
- \(\rho\) = density
- \(\vec{V}_{rel}\) = velocity relative to control surface
- \(\vec{n}\) = outward unit normal vector

---

## 2. Continuity / Mass Conservation

Mass flow rate:

\[
\dot{m}=\rho Q=\rho A V_{avg}
\]

Volume flow rate:

\[
Q=A V_{avg}
\]

General control-volume mass balance:

\[
\frac{dm_{CV}}{dt}
=
\sum \dot{m}_{in}
-
\sum \dot{m}_{out}
\]

For steady flow:

\[
\sum \dot{m}_{in}
=
\sum \dot{m}_{out}
\]

For steady incompressible flow:

\[
\sum Q_{in}
=
\sum Q_{out}
\]

Single inlet and single outlet:

\[
A_1V_1=A_2V_2
\]

---

## 3. Bernoulli Equation

\[
\frac{P_1}{\rho g}
+
\frac{V_1^2}{2g}
+
z_1
=
\frac{P_2}{\rho g}
+
\frac{V_2^2}{2g}
+
z_2
\]

General form:

\[
\frac{P}{\rho g}
+
\frac{V^2}{2g}
+
z
=
\text{constant}
\]

Bernoulli applies when:

- Flow is steady
- Flow is incompressible
- Friction is negligible
- No pump or turbine exists between points
- Points are along the same streamline

---

## 4. Mechanical Energy Equation

\[
\frac{P_1}{\rho g}
+
\alpha_1\frac{V_1^2}{2g}
+
z_1
+
h_p
=
\frac{P_2}{\rho g}
+
\alpha_2\frac{V_2^2}{2g}
+
z_2
+
h_t
+
h_L
\]

where:

- \(h_p\) = pump head added
- \(h_t\) = turbine head removed
- \(h_L\) = total head loss
- \(\alpha\) = kinetic energy correction factor

---

## 5. Pump and Turbine Power

Pump power added to fluid:

\[
\dot{W}_{pump,fluid}
=
\rho g Q h_p
\]

Pump input power:

\[
\dot{W}_{input}
=
\frac{\rho g Q h_p}{\eta_p}
\]

Turbine power removed from fluid:

\[
\dot{W}_{turbine,fluid}
=
\rho g Q h_t
\]

Turbine shaft output:

\[
\dot{W}_{shaft}
=
\eta_t \rho g Q h_t
\]

---

## 6. Pitot-Static Tube

\[
V
=
\sqrt{\frac{2(P_0-P)}{\rho}}
\]

where:

- \(P_0\) = stagnation pressure
- \(P\) = static pressure

---

## 7. Torricelli Equation

\[
V_{exit}
=
\sqrt{2g\Delta z}
\]

---

## 8. Linear Momentum Equation

Vector form:

\[
\sum \vec{F}
=
\sum_{out}\beta \dot{m}\vec{V}
-
\sum_{in}\beta \dot{m}\vec{V}
\]

x-direction:

\[
\sum F_x
=
\sum_{out}\beta \dot{m}V_x
-
\sum_{in}\beta \dot{m}V_x
\]

y-direction:

\[
\sum F_y
=
\sum_{out}\beta \dot{m}V_y
-
\sum_{in}\beta \dot{m}V_y
\]

where:

- \(\beta\) = momentum correction factor
- \(\dot{m}\vec{V}\) = momentum flow rate

---

## 9. Pressure Force

\[
F_P = PA
\]

Pressure acts into the control volume.

---

## 10. Angular Momentum Equation

\[
\sum M
=
\sum_{out}\dot{m}rV_\theta
-
\sum_{in}\dot{m}rV_\theta
\]

Shaft power:

\[
\dot{W}_{shaft}
=
\omega M
\]

Turbomachinery form:

\[
\dot{W}
=
\dot{m}\omega
\left(
r_2V_{\theta 2}
-
r_1V_{\theta 1}
\right)
\]

---

## 11. Reynolds Number

General form:

\[
Re
=
\frac{\rho V L}{\mu}
=
\frac{VL}{\nu}
\]

For pipe flow:

\[
Re
=
\frac{\rho V_{avg}D}{\mu}
=
\frac{V_{avg}D}{\nu}
\]

Pipe-flow classification:

- Laminar: \(Re < 2300\)
- Transitional: \(2300 \leq Re \leq 4000\)
- Turbulent: \(Re > 4000\)

---

## 12. Froude Number

\[
Fr
=
\frac{V}{\sqrt{gL}}
\]

---

## 13. Mach Number

\[
Ma
=
\frac{V}{c}
\]

---

## 14. Euler Number

\[
Eu
=
\frac{\Delta P}{\rho V^2}
\]

---

## 15. Weber Number

\[
We
=
\frac{\rho V^2L}{\sigma}
\]

---

## 16. Strouhal Number

\[
St
=
\frac{fL}{V}
\]

---

## 17. Buckingham Pi Theorem

\[
\text{Number of } \Pi \text{ groups}
=
n-k
\]

where:

- \(n\) = number of dimensional variables
- \(k\) = number of independent primary dimensions

---

## 18. Darcy-Weisbach Head Loss

\[
h_L
=
f\frac{L}{D}\frac{V^2}{2g}
\]

where:

- \(f\) = Darcy friction factor
- \(L\) = pipe length
- \(D\) = pipe diameter
- \(V\) = average velocity

---

## 19. Pressure Drop from Head Loss

\[
\Delta P
=
\rho g h_L
\]

---

## 20. Laminar Friction Factor

\[
f
=
\frac{64}{Re}
\]

This is only for laminar pipe flow.

---

## 21. Laminar Pipe Flow Pressure Drop

\[
\Delta P
=
\frac{32\mu L V_{avg}}{D^2}
\]

---

## 22. Hagen-Poiseuille Equation

Using diameter:

\[
Q
=
\frac{\pi D^4 \Delta P}{128\mu L}
\]

Using radius:

\[
Q
=
\frac{\pi R^4 \Delta P}{8\mu L}
\]

Since:

\[
D=2R
\]

both forms are equivalent.

---

## 23. Wall Shear Stress

Using diameter:

\[
\tau_w
=
\frac{\Delta P D}{4L}
\]

Using radius:

\[
\tau_w
=
\frac{\Delta P R}{2L}
\]

---

## 24. Haaland Equation

\[
\frac{1}{\sqrt{f}}
=
-1.8\log_{10}
\left[
\left(\frac{\varepsilon/D}{3.7}\right)^{1.11}
+
\frac{6.9}{Re}
\right]
\]

---

## 25. Swamee-Jain Equation

\[
f
=
\frac{0.25}
{
\left[
\log_{10}
\left(
\frac{\varepsilon}{3.7D}
+
\frac{5.74}{Re^{0.9}}
\right)
\right]^2
}
\]

---

## 26. Minor Loss

\[
h_{L,minor}
=
K_L\frac{V^2}{2g}
\]

Total head loss:

\[
h_{L,total}
=
\sum f\frac{L}{D}\frac{V^2}{2g}
+
\sum K_L\frac{V^2}{2g}
\]

Equivalent length:

\[
\frac{L_{eq}}{D}
=
\frac{K_L}{f}
\]

or

\[
L_{eq}
=
\frac{K_LD}{f}
\]

---

## 27. Series Pipes

Same flow rate:

\[
Q_1=Q_2=Q_3
\]

Total head loss:

\[
h_{L,total}
=
h_{L1}
+
h_{L2}
+
h_{L3}
\]

---

## 28. Parallel Pipes

Same head loss:

\[
h_{L1}=h_{L2}=h_{L3}
\]

Total flow rate:

\[
Q_{total}
=
Q_1+Q_2+Q_3
\]

---

## 29. Differential Continuity Equation

Compressible flow:

\[
\frac{\partial \rho}{\partial t}
+
\nabla \cdot (\rho \vec{V})
=
0
\]

Cartesian form:

\[
\frac{\partial \rho}{\partial t}
+
\frac{\partial(\rho u)}{\partial x}
+
\frac{\partial(\rho v)}{\partial y}
+
\frac{\partial(\rho w)}{\partial z}
=
0
\]

Incompressible flow:

\[
\nabla \cdot \vec{V}=0
\]

Cartesian incompressible form:

\[
\frac{\partial u}{\partial x}
+
\frac{\partial v}{\partial y}
+
\frac{\partial w}{\partial z}
=
0
\]

2D incompressible flow:

\[
\frac{\partial u}{\partial x}
+
\frac{\partial v}{\partial y}
=
0
\]

---

## 30. Material Derivative

\[
\frac{D\vec{V}}{Dt}
=
\frac{\partial \vec{V}}{\partial t}
+
(\vec{V}\cdot \nabla)\vec{V}
\]

x-direction acceleration:

\[
a_x
=
\frac{\partial u}{\partial t}
+
u\frac{\partial u}{\partial x}
+
v\frac{\partial u}{\partial y}
+
w\frac{\partial u}{\partial z}
\]

where:

- \(u\) = x-direction velocity component
- \(v\) = y-direction velocity component
- \(w\) = z-direction velocity component

Important:

Do not confuse velocity component \(u\) with kinematic viscosity \(\nu\).

---

## 31. Stream Function

For 2D incompressible Cartesian flow:

\[
u
=
\frac{\partial \psi}{\partial y}
\]

\[
v
=
-\frac{\partial \psi}{\partial x}
\]

Flow rate per unit width between two streamlines:

\[
q
=
\psi_2-\psi_1
\]

---

## 32. Navier-Stokes Equation

For incompressible Newtonian constant-property flow:

\[
\rho \frac{D\vec{V}}{Dt}
=
-\nabla P
+
\rho \vec{g}
+
\mu \nabla^2 \vec{V}
\]

Term meanings:

- \(\rho \frac{D\vec{V}}{Dt}\) = inertia term
- \(-\nabla P\) = pressure force term
- \(\rho \vec{g}\) = body force term
- \(\mu \nabla^2 \vec{V}\) = viscous term

---

## 33. Couette Flow

Velocity profile:

\[
u(y)
=
\frac{Uy}{h}
\]

Shear stress:

\[
\tau
=
\mu \frac{du}{dy}
=
\frac{\mu U}{h}
\]

---

## 34. Plane Poiseuille Flow

Pressure-driven flow between two stationary parallel plates.

The velocity profile is parabolic.

Key points:

- No slip at both walls
- Maximum velocity occurs at the centerline
- Pressure decreases in the flow direction

---

## 35. Pipe Poiseuille Flow

Velocity profile:

\[
u(r)
=
\frac{R^2}{4\mu}
\left(
-\frac{dP}{dx}
\right)
\left[
1-\left(\frac{r}{R}\right)^2
\right]
\]

Maximum velocity:

\[
u_{max}
=
\frac{R^2}{4\mu}
\left(
-\frac{dP}{dx}
\right)
\]

Average velocity:

\[
V_{avg}
=
\frac{u_{max}}{2}
\]

Flow rate:

\[
Q
=
\frac{\pi R^4}{8\mu}
\left(
-\frac{dP}{dx}
\right)
\]

Pressure-drop form:

\[
Q
=
\frac{\pi R^4\Delta P}{8\mu L}
\]

This is equivalent to:

\[
Q
=
\frac{\pi D^4\Delta P}{128\mu L}
\]

---

# Common Formula Mistakes to Avoid

1. Do not use Bernoulli across a pump, turbine, or high-loss region.
2. Do not mix gage pressure and absolute pressure in the same equation.
3. Do not use \(f=64/Re\) for turbulent flow.
4. Do not confuse Darcy friction factor with Fanning friction factor.
5. Do not assume equal flow rate in parallel pipes.
6. Do not assume equal head loss in series pipes.
7. Do not forget minor losses from valves, elbows, entrances, and exits.
8. Do not use diameter when the formula requires radius.
9. Do not confuse \(u\), the velocity component, with \(\nu\), kinematic viscosity.
10. Always check units before final answer.
