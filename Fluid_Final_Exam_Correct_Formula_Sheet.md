# Correct Fluid Mechanics Formula Sheet

Use this as the clean version of the formulas from the study guide.

## 1. Basic Definitions

Density:

$$
\rho = \frac{m}{V}
$$

Specific volume:

$$
v = \frac{1}{\rho}
$$

Specific weight:

$$
\gamma = \rho g
$$

Area of a circular pipe:

$$
A = \frac{\pi D^2}{4}
$$

Volume flow rate:

$$
\dot{V} = Q = V_{\text{avg}} A
$$

Mass flow rate:

$$
\dot{m} = \rho Q = \rho V_{\text{avg}} A
$$

## 2. Conservation of Mass

General control-volume mass balance:

$$
\frac{dm_{CV}}{dt} = \sum \dot{m}_{in} - \sum \dot{m}_{out}
$$

For steady flow:

$$
\sum \dot{m}_{in} = \sum \dot{m}_{out}
$$

For steady incompressible flow:

$$
\sum Q_{in} = \sum Q_{out}
$$

For one inlet and one outlet, incompressible:

$$
A_1 V_1 = A_2 V_2
$$

## 3. Mechanical Energy

Mechanical energy per unit mass:

$$
e_{mech} = \frac{P}{\rho} + \frac{V^2}{2} + gz
$$

Mechanical energy per unit weight, also called head:

$$
h_{mech} = \frac{P}{\rho g} + \frac{V^2}{2g} + z
$$

Pressure head:

$$
h_P = \frac{P}{\rho g}
$$

Velocity head:

$$
h_V = \frac{V^2}{2g}
$$

Elevation head:

$$
h_z = z
$$

## 4. Bernoulli Equation

Bernoulli equation between points 1 and 2:

$$
\frac{P_1}{\rho g} + \frac{V_1^2}{2g} + z_1
=
\frac{P_2}{\rho g} + \frac{V_2^2}{2g} + z_2
$$

Pressure form:

$$
P_1 + \frac{1}{2}\rho V_1^2 + \rho g z_1
=
P_2 + \frac{1}{2}\rho V_2^2 + \rho g z_2
$$

Pitot-static tube:

$$
V = \sqrt{\frac{2(P_0 - P)}{\rho}}
$$

Torricelli equation for ideal tank discharge:

$$
V = \sqrt{2g\Delta z}
$$

## 5. Mechanical Energy Equation with Pump, Turbine, and Losses

General steady incompressible mechanical energy equation:

$$
\frac{P_1}{\rho g}
+ \alpha_1 \frac{V_1^2}{2g}
+ z_1
+ h_{pump}
=
\frac{P_2}{\rho g}
+ \alpha_2 \frac{V_2^2}{2g}
+ z_2
+ h_{turbine}
+ h_L
$$

If kinetic-energy correction factors are neglected:

$$
\frac{P_1}{\rho g}
+ \frac{V_1^2}{2g}
+ z_1
+ h_{pump}
=
\frac{P_2}{\rho g}
+ \frac{V_2^2}{2g}
+ z_2
+ h_{turbine}
+ h_L
$$

Pump head added to fluid:

$$
h_{pump} =
\frac{\dot{W}_{pump,fluid}}{\rho g Q}
$$

Turbine head removed from fluid:

$$
h_{turbine} =
\frac{\dot{W}_{turbine,fluid}}{\rho g Q}
$$

Hydraulic power:

$$
\dot{W}_{fluid} = \rho g Q h
$$

Pump efficiency:

$$
\eta_{pump}
=
\frac{\dot{W}_{pump,fluid}}{\dot{W}_{pump,input}}
$$

Turbine efficiency:

$$
\eta_{turbine}
=
\frac{\dot{W}_{turbine,shaft}}{\dot{W}_{turbine,fluid}}
$$

## 6. Linear Momentum Equation

General steady linear momentum equation:

$$
\sum \vec{F}
=
\sum_{out} \beta \dot{m}\vec{V}
-
\sum_{in} \beta \dot{m}\vec{V}
$$

x-direction:

$$
\sum F_x
=
\sum_{out} \beta \dot{m}V_x
-
\sum_{in} \beta \dot{m}V_x
$$

y-direction:

$$
\sum F_y
=
\sum_{out} \beta \dot{m}V_y
-
\sum_{in} \beta \dot{m}V_y
$$

Pressure force:

$$
F_P = PA
$$

Weight:

$$
W = mg = \rho V_{fluid} g
$$

## 7. Angular Momentum Equation

Steady angular momentum equation about a fixed axis:

$$
\sum M
=
\sum_{out} \dot{m} r V_\theta
-
\sum_{in} \dot{m} r V_\theta
$$

Shaft power:

$$
\dot{W}_{shaft} = \omega M
$$

Turbomachinery form:

$$
\dot{W}_{shaft}
=
\dot{m}\omega
\left(r_2 V_{\theta 2} - r_1 V_{\theta 1}\right)
$$

## 8. Reynolds Number and Flow Classification

Pipe Reynolds number:

$$
Re = \frac{\rho V_{avg} D}{\mu}
$$

Using kinematic viscosity:

$$
Re = \frac{V_{avg}D}{\nu}
$$

Flow classification in circular pipes:

$$
Re < 2300
\quad \Rightarrow \quad
\text{laminar}
$$

$$
2300 \lesssim Re \lesssim 4000
\quad \Rightarrow \quad
\text{transitional}
$$

$$
Re > 4000
\quad \Rightarrow \quad
\text{turbulent}
$$

## 9. Pipe Flow Losses

Darcy-Weisbach major head loss:

$$
h_{L,major}
=
f\frac{L}{D}\frac{V^2}{2g}
$$

Pressure drop from head loss:

$$
\Delta P = \rho g h_L
$$

Laminar Darcy friction factor:

$$
f = \frac{64}{Re}
$$

Minor head loss:

$$
h_{L,minor}
=
K_L\frac{V^2}{2g}
$$

Total head loss:

$$
h_L
=
\sum f\frac{L}{D}\frac{V^2}{2g}
+
\sum K_L\frac{V^2}{2g}
$$

Equivalent length:

$$
\frac{L_{eq}}{D}
=
\frac{K_L}{f}
$$

Hagen-Poiseuille equation:

$$
Q
=
\frac{\pi D^4 \Delta P}{128\mu L}
$$

Alternative Hagen-Poiseuille equation using radius:

$$
Q
=
\frac{\pi R^4 \Delta P}{8\mu L}
$$

Laminar pipe pressure drop:

$$
\Delta P
=
\frac{32\mu L V_{avg}}{D^2}
$$

Wall shear stress in pipe flow:

$$
\tau_w
=
\frac{\Delta P D}{4L}
$$

## 10. Pipe Networks

Pipes in series:

$$
Q_1 = Q_2 = Q_3 = \cdots
$$

$$
h_{L,total}
=
h_{L,1} + h_{L,2} + h_{L,3} + \cdots
$$

Pipes in parallel:

$$
h_{L,1} = h_{L,2} = h_{L,3} = \cdots
$$

$$
Q_{total}
=
Q_1 + Q_2 + Q_3 + \cdots
$$

## 11. Flow Meters

Ideal Venturi/orifice idea:

$$
Q_{actual} = C_d Q_{ideal}
$$

Discharge coefficient:

$$
C_d = \frac{Q_{actual}}{Q_{ideal}}
$$

For a horizontal ideal Venturi meter:

$$
Q_{ideal}
=
A_2
\sqrt{
\frac{2(P_1-P_2)}
{\rho\left[1-\left(A_2/A_1\right)^2\right]}
}
$$

With discharge coefficient:

$$
Q_{actual}
=
C_d A_2
\sqrt{
\frac{2(P_1-P_2)}
{\rho\left[1-\left(A_2/A_1\right)^2\right]}
}
$$

## 12. Dimensional Analysis

Number of dimensionless groups:

$$
\text{number of } \Pi \text{ groups} = n - k
$$

where:

- \(n\) = number of variables.
- \(k\) = number of independent primary dimensions.

Common dimensionless numbers:

Reynolds number:

$$
Re = \frac{\rho V L}{\mu}
$$

Froude number:

$$
Fr = \frac{V}{\sqrt{gL}}
$$

Mach number:

$$
Ma = \frac{V}{c}
$$

Euler number:

$$
Eu = \frac{\Delta P}{\rho V^2}
$$

Weber number:

$$
We = \frac{\rho V^2 L}{\sigma}
$$

Strouhal number:

$$
St = \frac{fL}{V}
$$

## 13. Differential Continuity

General continuity equation:

$$
\frac{\partial \rho}{\partial t}
+
\nabla \cdot (\rho \vec{V})
=
0
$$

Cartesian form:

$$
\frac{\partial \rho}{\partial t}
+
\frac{\partial(\rho u)}{\partial x}
+
\frac{\partial(\rho v)}{\partial y}
+
\frac{\partial(\rho w)}{\partial z}
=
0
$$

Incompressible continuity:

$$
\nabla \cdot \vec{V} = 0
$$

Cartesian incompressible form:

$$
\frac{\partial u}{\partial x}
+
\frac{\partial v}{\partial y}
+
\frac{\partial w}{\partial z}
=
0
$$

Two-dimensional incompressible form:

$$
\frac{\partial u}{\partial x}
+
\frac{\partial v}{\partial y}
=
0
$$

## 14. Material Derivative and Acceleration

Material derivative:

$$
\frac{D}{Dt}
=
\frac{\partial}{\partial t}
+
u\frac{\partial}{\partial x}
+
v\frac{\partial}{\partial y}
+
w\frac{\partial}{\partial z}
$$

x-acceleration:

$$
a_x
=
\frac{Du}{Dt}
=
\frac{\partial u}{\partial t}
+ u\frac{\partial u}{\partial x}
+ v\frac{\partial u}{\partial y}
+ w\frac{\partial u}{\partial z}
$$

y-acceleration:

$$
a_y
=
\frac{Dv}{Dt}
=
\frac{\partial v}{\partial t}
+ u\frac{\partial v}{\partial x}
+ v\frac{\partial v}{\partial y}
+ w\frac{\partial v}{\partial z}
$$

z-acceleration:

$$
a_z
=
\frac{Dw}{Dt}
=
\frac{\partial w}{\partial t}
+ u\frac{\partial w}{\partial x}
+ v\frac{\partial w}{\partial y}
+ w\frac{\partial w}{\partial z}
$$

## 15. Stream Function

For two-dimensional incompressible Cartesian flow:

$$
u = \frac{\partial \psi}{\partial y}
$$

$$
v = -\frac{\partial \psi}{\partial x}
$$

Flow rate per unit width between two streamlines:

$$
q = \psi_2 - \psi_1
$$

## 16. Navier-Stokes Equation

Incompressible Newtonian flow with constant viscosity:

$$
\rho \frac{D\vec{V}}{Dt}
=
-\nabla P
+ \rho \vec{g}
+ \mu \nabla^2 \vec{V}
$$

Without gravity:

$$
\rho \frac{D\vec{V}}{Dt}
=
-\nabla P
+ \mu \nabla^2 \vec{V}
$$

## 17. Couette and Poiseuille Flow

Couette flow between two plates, bottom stationary and top moving at speed \(U\):

$$
u(y) = \frac{U}{h}y
$$

Couette shear stress:

$$
\tau = \mu \frac{du}{dy}
=
\mu \frac{U}{h}
$$

Laminar pipe Poiseuille velocity profile:

$$
u(r)
=
\frac{R^2}{4\mu}
\left(-\frac{dP}{dx}\right)
\left(1-\frac{r^2}{R^2}\right)
$$

Maximum velocity:

$$
u_{max}
=
\frac{R^2}{4\mu}
\left(-\frac{dP}{dx}\right)
$$

Average velocity:

$$
V_{avg}
=
\frac{u_{max}}{2}
$$

Flow rate:

$$
Q
=
\frac{\pi R^4}{8\mu}
\left(-\frac{dP}{dx}\right)
$$

Using pressure drop over length \(L\):

$$
Q
=
\frac{\pi R^4 \Delta P}{8\mu L}
$$

