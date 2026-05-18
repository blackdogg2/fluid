# Fluid Mechanics Final Exam Study Guide

Source files reviewed:

- `Fluid_Mechanics - Cengel.pdf`
- `Fluid_Mechanics - Cengel-Solution .pdf`

Important note: I cannot know the exact final exam questions. The "most likely" items below are based on the chapters included in your files and the problem patterns repeated in the solution manual. Use this as a high-yield study map, not as a prediction of exact exam questions.

## Exam Priority Ranking

Study in this order if time is limited:

1. Chapter 5: continuity, Bernoulli, mechanical energy balance, pump/turbine/head-loss problems.
2. Chapter 8: pipe flow, Reynolds number, friction factor, major/minor losses, pump power, pipe networks.
3. Chapter 6: linear momentum for forces on nozzles, elbows, vanes, jets, and supports.
4. Chapter 7: dimensional analysis, Buckingham Pi theorem, model-prototype similarity.
5. Chapter 9: continuity in differential form, stream function, simplified Navier-Stokes, Couette/Poiseuille flows.
6. Late Chapter 4: Reynolds Transport Theorem as the bridge from system laws to control-volume laws.

The most exam-friendly problem types are:

- Given a pipe/tank/nozzle system, find flow rate, velocity, pressure, pump head, or power.
- Given a bend/nozzle/jet, find the support force using momentum.
- Given a pipe length/diameter/roughness/flow rate, find head loss or pump requirement.
- Given variables and dimensions, form dimensionless groups.
- Given a velocity field, check continuity, find acceleration, or find a stream function.

## Core Problem-Solving Template

For almost every fluid mechanics problem:

1. Draw the control volume or flow domain.
2. Write knowns, unknowns, and units.
3. State assumptions: steady/unsteady, incompressible/compressible, inviscid/viscous, one-dimensional average flow, negligible losses or not.
4. Choose the governing equation:
   - Mass conservation for flow rates.
   - Bernoulli when losses, pumps, turbines, and viscous effects are negligible.
   - Mechanical energy when pumps, turbines, and head losses matter.
   - Linear momentum when forces are requested.
   - Dimensional analysis when variables and scaling are requested.
   - Differential continuity/Navier-Stokes when velocity fields or simple exact profiles are requested.
5. Use consistent SI or English units.
6. Check the sign convention and whether pressure is absolute or gage.
7. Check whether the answer is physically reasonable.

Common mistakes:

- Using Bernoulli through a pump, turbine, fan, compressor, or high-loss section.
- Forgetting elevation head `z`.
- Mixing gage and absolute pressure in one equation.
- Using diameter instead of area in continuity.
- Using Fanning friction factor when the chapter uses Darcy friction factor.
- Forgetting minor losses in real pipe systems.
- In momentum problems, forgetting pressure forces or choosing inconsistent signs.
- In parallel pipes, assuming equal flow rate instead of equal head loss.
- In series pipes, assuming equal head loss instead of equal flow rate.

## Late Chapter 4 - Reynolds Transport Theorem

### Big Idea

Fluid mechanics often starts with laws for a system: a fixed amount of matter followed as it moves. Engineering problems usually use a control volume: a region in space where mass can cross the boundary. The Reynolds Transport Theorem (RTT) converts system laws into control-volume laws.

### Key Concepts

- System: fixed mass; no mass crosses its boundary.
- Control volume: selected region in space; mass may enter or leave.
- Control surface: boundary of the control volume.
- Extensive property `B`: total amount, such as mass, momentum, or energy.
- Intensive property `b = B/m`: property per unit mass.
- Local/unsteady term: change inside the control volume with time.
- Advective/flux term: transport of property across the control surface by flow.

### General Meaning of RTT

Rate of change following a system =

- rate of change inside the control volume
- plus net rate carried out through the control surface

For exam use, understand the structure more than memorizing only symbols:

`dB_system/dt = d/dt integral_CV(rho b dV) + integral_CS(rho b V_rel dot n dA)`

where:

- `rho` is density.
- `b` is property per unit mass.
- `V_rel` is velocity relative to the control surface.
- `n` points outward from the control surface.

### Most Important Applications

Choose `B = mass`, so `b = 1`:

- RTT becomes conservation of mass.

Choose `B = linear momentum`, so `b = V`:

- RTT becomes the linear momentum equation.

Choose `B = energy`, so `b = e`:

- RTT becomes the energy equation.

Choose `B = angular momentum`, so `b = r x V`:

- RTT becomes the angular momentum equation.

### Final Exam Use

RTT usually appears as a conceptual or derivation question:

- Explain system vs control volume.
- Explain local and advective terms.
- Derive continuity or momentum from RTT.
- Know why steady flow can still have property flux across the boundary.

## Chapter 5 - Mass, Bernoulli, and Energy Equations

This is probably the most important chapter for your final.

### 5.1 Conservation Principles

Mass, momentum, and energy are conserved quantities. In fluid mechanics, these are usually written for a control volume because fluids flow into and out of devices.

Core conservation idea:

`Accumulation = In - Out + Generation`

For mass, there is no generation in ordinary fluid mechanics:

`Rate of mass increase in CV = mass flow in - mass flow out`

### 5.2 Conservation of Mass

Mass flow rate:

`m_dot = rho V_avg A`

Volume flow rate:

`Q = V_avg A`

Relation between mass flow and volume flow:

`m_dot = rho Q`

General control-volume mass balance:

`dm_CV/dt = sum(m_dot_in) - sum(m_dot_out)`

Steady flow:

`sum(m_dot_in) = sum(m_dot_out)`

Steady incompressible flow:

`sum(Q_in) = sum(Q_out)`

Single inlet and single outlet, incompressible:

`A1 V1 = A2 V2`

Important details:

- Velocity in a pipe is not uniform, so use average velocity unless told otherwise.
- For gases, density may change if pressure/temperature changes.
- For liquids, density is usually treated as constant.

High-yield question forms:

- Find velocity from flow rate and diameter.
- Find mass flow rate from density and volume flow rate.
- Find filling/draining time.
- Analyze multiple inlets/outlets.
- Ventilation/air-change problems.

### 5.3 Mechanical Energy and Efficiency

Mechanical energy per unit mass for flowing fluid:

`e_mech = P/rho + V^2/2 + gz`

Head form:

`e_mech/g = P/(rho g) + V^2/(2g) + z`

The three heads are:

- Pressure head: `P/(rho g)`
- Velocity head: `V^2/(2g)`
- Elevation head: `z`

Pump:

- Adds mechanical energy to the fluid.
- Useful pump head: `h_pump`
- Hydraulic power added to fluid: `W_dot_fluid = rho g Q h_pump`

Turbine:

- Extracts mechanical energy from the fluid.
- Power extracted: `W_dot_turbine = rho g Q h_turbine`

Efficiency:

- Pump efficiency: useful fluid power divided by shaft/electrical input power.
- Turbine efficiency: shaft output power divided by fluid power lost.

High-yield mistakes:

- For pumps, input power is greater than useful fluid power.
- For turbines, shaft output is less than fluid power extracted.
- Always check whether the problem asks for power to the fluid, shaft power, or electrical power.

### 5.4 Bernoulli Equation

Bernoulli equation in head form:

`P1/(rho g) + V1^2/(2g) + z1 = P2/(rho g) + V2^2/(2g) + z2`

Bernoulli is a mechanical energy equation with no losses and no shaft work.

Conditions for Bernoulli:

- Steady flow.
- Incompressible flow.
- Negligible friction/viscous losses.
- Along a streamline.
- No pump or turbine between the points.
- No significant heat/work interaction.

When the flow is irrotational, Bernoulli can sometimes be applied between different streamlines.

Pressure forms:

- Static pressure: thermodynamic pressure in the fluid.
- Dynamic pressure: `rho V^2/2`.
- Stagnation pressure: pressure if fluid is brought to rest isentropically/inviscidly.

Pitot-static idea:

`V = sqrt(2(P_stag - P_static)/rho)`

Free surface tank discharge, ideal:

`V_exit = sqrt(2g delta_z)`

This is Torricelli's result when both tank surface and jet exit are exposed to atmosphere and tank surface velocity is negligible.

### 5.5 Applications of Bernoulli

Very likely final exam applications:

- Free jet from a tank.
- Pressurized tank discharge.
- Siphon.
- Pitot-static tube.
- Venturi meter.
- Nozzle/diffuser pressure-velocity relation.
- Manometer combined with Bernoulli.

Exam strategy:

1. Pick two points.
2. Write Bernoulli with all terms.
3. Cross out terms only after explaining why:
   - Same atmospheric pressure.
   - Same elevation.
   - Large tank surface velocity is negligible.
   - Outlet pressure is atmospheric.
4. Use continuity if two velocities are unknown.

### 5.6 General Energy Equation

The general energy equation includes:

- Heat transfer.
- Work transfer.
- Internal energy.
- Kinetic energy.
- Potential energy.

For most fluid mechanics pipe problems, the chapter reduces this to a mechanical energy balance.

### 5.7 Mechanical Energy Balance for Steady Flow

Head form for incompressible steady flow:

`P1/(rho g) + alpha1 V1^2/(2g) + z1 + h_pump`

`= P2/(rho g) + alpha2 V2^2/(2g) + z2 + h_turbine + h_L`

where:

- `h_pump` is useful pump head added.
- `h_turbine` is turbine head extracted.
- `h_L` is total head loss.
- `alpha` is kinetic energy correction factor. Often `alpha = 1` for turbulent/flat profiles unless specified.

Power:

`W_dot_pump_to_fluid = rho g Q h_pump`

`W_dot_turbine_from_fluid = rho g Q h_turbine`

Most important Chapter 5 final problem:

- A pipe connects two reservoirs with a pump/turbine and losses. Find flow rate, pump head, turbine power, or pressure difference.

## Chapter 6 - Momentum Analysis of Flow Systems

### Big Idea

Use momentum when the unknown is force or torque.

Chapter 5 energy equations tell you about pressure, speed, elevation, and power. Chapter 6 momentum equations tell you the forces required to change fluid momentum.

### 6.1 Newton's Laws and Momentum

Linear momentum:

`momentum = m V`

Newton's second law:

`sum F = rate of change of linear momentum`

Angular momentum:

`angular momentum = r x mV`

Torque:

`sum M = rate of change of angular momentum`

### 6.2 Choosing a Control Volume

Good control volume choices:

- Cut through inlets and outlets where velocity and pressure are known or uniform enough.
- Include the object/device whose support force is requested.
- Align axes with inlet/outlet directions when possible.

### 6.3 Forces on a Control Volume

Forces usually include:

- Pressure forces at inlets/outlets.
- Weight of fluid/device.
- Support or anchoring reaction.
- Atmospheric pressure, often canceled by using gage pressure.
- Wall forces.

Pressure force:

`F_P = P A`

Direction:

- Pressure pushes into the control volume.
- Use gage pressure when surrounding pressure is atmospheric.

### 6.4 Linear Momentum Equation

Steady one-dimensional form:

`sum F = sum_out(beta m_dot V) - sum_in(beta m_dot V)`

In x-direction:

`sum F_x = sum_out(beta m_dot V_x) - sum_in(beta m_dot V_x)`

In y-direction:

`sum F_y = sum_out(beta m_dot V_y) - sum_in(beta m_dot V_y)`

`beta` is the momentum-flux correction factor:

- Often about 1 for turbulent flow.
- Larger for laminar profiles.
- Use the value given in the problem if provided.

High-yield force problems:

- Force on a nozzle.
- Force on an elbow or pipe bend.
- Force on a reducer/expander.
- Jet striking a flat plate.
- Jet striking a curved vane.
- Anchor force for pipe fittings.

Problem template for pipe-bend force:

1. Draw CV around the bend.
2. Label inlet/outlet velocities as vectors.
3. Use continuity to find velocities.
4. Use pressure forces at inlet/outlet.
5. Include weight if vertical or if specified.
6. Write x- and y-momentum equations separately.
7. Solve for support force.
8. Remember: force of fluid on pipe is opposite force of pipe on fluid.

### 6.5 Rotational Motion

Know:

- Angular velocity.
- Moment arm.
- Torque.
- Moment of momentum.

### 6.6 Angular Momentum Equation

Steady angular momentum equation:

`sum M = sum_out(m_dot r V_theta) - sum_in(m_dot r V_theta)`

where:

- `r` is radius from axis.
- `V_theta` is tangential velocity component.

Turbomachinery power form:

`W_dot_shaft = omega * M`

Often:

`W_dot = m_dot omega (r2 V_theta2 - r1 V_theta1)`

High-yield applications:

- Sprinklers.
- Rotating nozzles.
- Turbines/pumps with tangential velocity components.

## Chapter 7 - Dimensional Analysis and Modeling

### Big Idea

Dimensional analysis reduces many variables into fewer dimensionless groups. It is essential for experiments, scale models, and correlations.

### 7.1 Dimensions and Units

Primary dimensions usually include:

- Mass: `M`
- Length: `L`
- Time: `t`
- Temperature: `T`

Common dimensions:

- Velocity: `L/t`
- Acceleration: `L/t^2`
- Force: `M L/t^2`
- Pressure/stress: `M/(L t^2)`
- Density: `M/L^3`
- Dynamic viscosity `mu`: `M/(L t)`
- Kinematic viscosity `nu`: `L^2/t`
- Surface tension: `M/t^2`

### 7.2 Dimensional Homogeneity

Every additive term in a physically correct equation must have the same dimensions.

Exam use:

- Check whether an equation is dimensionally valid.
- Find dimensions of a constant.
- Nondimensionalize an equation.

### 7.3 Similarity

For a model to represent a prototype:

- Geometric similarity: same shape, scaled dimensions.
- Kinematic similarity: velocity fields have similar patterns.
- Dynamic similarity: force ratios match.

Important dimensionless numbers:

- Reynolds number: `Re = rho V L / mu = V L / nu`
  - Inertia force / viscous force.
  - Dominant in pipe flow and external viscous flow.

- Froude number: `Fr = V / sqrt(gL)`
  - Inertia force / gravity force.
  - Dominant in free-surface flows, ships, spillways.

- Mach number: `Ma = V/c`
  - Flow speed / sound speed.
  - Dominant in compressible gas flow.

- Euler number: `Eu = delta_P/(rho V^2)`
  - Pressure force / inertia force.

- Weber number: `We = rho V^2 L / sigma`
  - Inertia force / surface tension force.
  - Important in droplets, jets, capillarity.

- Strouhal number: `St = f L / V`
  - Unsteady oscillation / flow time scale.

### 7.4 Buckingham Pi Theorem

If a problem has:

- `n` dimensional variables
- `k` independent primary dimensions

then the number of dimensionless Pi groups is:

`n - k`

Method of repeating variables:

1. List all variables affecting the dependent variable.
2. Write dimensions of each variable.
3. Count primary dimensions.
4. Choose repeating variables:
   - They must collectively contain all primary dimensions.
   - They should not include the dependent variable.
   - They should not form a dimensionless group by themselves.
5. Combine repeating variables with each non-repeating variable.
6. Solve exponents to make each product dimensionless.
7. Write the final functional relation.

Example format:

`Pi1 = f(Pi2, Pi3, Pi4, ...)`

### 7.5 Experimental Testing and Incomplete Similarity

Sometimes all dimensionless numbers cannot be matched at once. Example: matching both Reynolds and Froude numbers can be impossible if the same fluid and gravity are used.

Exam strategy:

- Identify the dominant physics.
- Match the dimensionless number connected to that physics.
- State which effects are neglected or imperfectly matched.

High-yield question forms:

- Find Pi groups for drag force, pressure drop, pump power, or wave resistance.
- Scale model results to prototype.
- Determine model speed from matching Reynolds or Froude number.
- Explain why complete similarity is impossible.

## Chapter 8 - Flow in Pipes

This is another very high-priority final exam chapter.

### 8.1 Internal Flow

Internal flow:

- Fluid completely fills a pipe or duct.
- Driven mainly by pressure difference, pump work, or elevation difference.

External flow:

- Flow over a body, such as a car or wing.

Open-channel flow:

- Has a free surface and is driven mainly by gravity.

### 8.2 Laminar and Turbulent Flow

Reynolds number for pipe flow:

`Re = rho V_avg D / mu = V_avg D / nu`

Pipe-flow classification:

- Laminar: `Re < 2300`
- Transitional: about `2300 <= Re <= 4000`
- Turbulent: `Re > 4000`

Laminar flow:

- Smooth, orderly motion.
- Viscous effects dominate.
- Exact solutions are possible.

Turbulent flow:

- Fluctuating, mixed motion.
- Inertia effects dominate.
- Use empirical friction factor correlations or Moody chart.

### 8.3 Entrance Region

At the pipe entrance, the velocity profile develops because of the no-slip condition at the wall.

Hydrodynamic entrance length:

Laminar estimate:

`L_h/D approximately 0.05 Re`

Turbulent estimate:

`L_h/D approximately 10`

Fully developed flow:

- Velocity profile no longer changes in the flow direction.
- Pressure drops linearly with distance in a constant-area pipe.

### 8.4 Laminar Flow in Pipes

For fully developed laminar pipe flow:

- Velocity profile is parabolic.
- Maximum velocity occurs at centerline.
- Average velocity is half the maximum velocity.

`V_avg = V_max/2`

Darcy friction factor for laminar flow:

`f = 64/Re`

Darcy-Weisbach head loss:

`h_L = f (L/D) V^2/(2g)`

Pressure drop:

`delta_P = rho g h_L`

For laminar pipe flow:

`delta_P = 32 mu L V_avg / D^2`

Hagen-Poiseuille relation:

`Q = pi D^4 delta_P / (128 mu L)`

Wall shear stress:

`tau_w = delta_P D / (4L)`

High-yield exam form:

- Given oil/water properties, pipe diameter, length, and flow rate: determine if laminar, then find pressure drop and pumping power.

### 8.5 Turbulent Flow in Pipes

For turbulent pipe flow:

Use Darcy-Weisbach:

`h_L = f (L/D) V^2/(2g)`

Friction factor depends on:

- Reynolds number.
- Relative roughness `epsilon/D`.

Moody chart / Colebrook equation:

Use these when roughness and Reynolds number are given.

For smooth or rough turbulent flow, the friction factor is not `64/Re`.

Useful explicit approximations may be allowed by your teacher:

Haaland:

`1/sqrt(f) = -1.8 log10( (epsilon/D/3.7)^1.11 + 6.9/Re )`

Swamee-Jain:

`f = 0.25 / [log10(epsilon/(3.7D) + 5.74/Re^0.9)]^2`

Check which formula your instructor allows.

Pumping power:

`W_dot_pump_to_fluid = rho g Q h_L`

With efficiency:

`W_dot_input = W_dot_pump_to_fluid / eta_pump`

### 8.6 Minor Losses

Minor losses come from:

- Entrances.
- Exits.
- Bends/elbows.
- Valves.
- Sudden expansion.
- Sudden contraction.
- Fittings.

Minor head loss:

`h_L,minor = K_L V^2/(2g)`

Total loss:

`h_L,total = sum[ f(L/D) V^2/(2g) ] + sum[ K_L V^2/(2g) ]`

Equivalent length:

`L_eq/D = K_L/f`

Important:

- Use the velocity associated with the fitting's specified diameter.
- For sudden expansion, use the correct upstream/downstream velocity relationship.

### 8.7 Piping Networks and Pump Selection

Series pipes:

- Same flow rate through each pipe.
- Total head loss is the sum of losses.

`Q1 = Q2 = Q3`

`h_L,total = h_L1 + h_L2 + h_L3`

Parallel pipes:

- Same head loss across each branch.
- Total flow rate is sum of branch flow rates.

`h_L1 = h_L2 = h_L3`

`Q_total = Q1 + Q2 + Q3`

Pump/system curve:

- System head usually increases with `Q^2`.
- Operating point is where pump curve intersects system curve.

### 8.8 Flow Rate and Velocity Measurement

Common devices:

- Pitot-static tube.
- Venturi meter.
- Orifice meter.
- Flow nozzle.
- Rotameter.

Venturi/orifice idea:

- Use continuity plus Bernoulli.
- Real meters include discharge coefficient `C_d`.

Generic meter relation:

`Q_actual = C_d Q_ideal`

High-yield final problems:

- Find flow rate from pressure difference in a Venturi.
- Use a manometer pressure difference.
- Include discharge coefficient if provided.

## Chapter 9 - Differential Analysis of Fluid Flow

### Big Idea

Control-volume analysis gives overall balances. Differential analysis gives equations at every point in the flow field.

This chapter is more mathematical. Your final may ask you to:

- Check whether a velocity field satisfies continuity.
- Find missing velocity component.
- Find stream function.
- Simplify Navier-Stokes for a simple flow.
- Derive Couette or Poiseuille velocity profiles.

### 9.1 Flow Domain vs Control Volume

Flow domain:

- Region where the differential equations are solved point by point.

Control volume:

- Finite region used for integral balances.

### 9.2 Continuity Equation

General compressible continuity:

`partial rho/partial t + div(rho V) = 0`

In Cartesian coordinates:

`partial rho/partial t + partial(rho u)/partial x + partial(rho v)/partial y + partial(rho w)/partial z = 0`

Incompressible continuity:

`div V = 0`

Cartesian incompressible form:

`partial u/partial x + partial v/partial y + partial w/partial z = 0`

Two-dimensional incompressible:

`partial u/partial x + partial v/partial y = 0`

Exam use:

- Given `u(x,y)` and `v(x,y)`, check if incompressible.
- Given one velocity component, integrate continuity to find the other.
- Remember an integration "constant" may be a function of the other variable.

### Material Derivative

For velocity:

`D V/Dt = partial V/partial t + (V dot grad) V`

In x-direction:

`a_x = partial u/partial t + u partial u/partial x + v partial u/partial y + w partial u/partial z`

For steady flow, local acceleration is zero, but convective acceleration may still exist.

### 9.3 Stream Function

For two-dimensional incompressible Cartesian flow:

`u = partial psi/partial y`

`v = - partial psi/partial x`

This automatically satisfies continuity if `psi` is smooth.

Meaning:

- Curves of constant `psi` are streamlines.
- Difference in stream function between two streamlines equals volume flow rate per unit width.

`Q_per_width = psi_2 - psi_1`

Polar/cylindrical two-dimensional form:

`u_r = (1/r) partial psi/partial theta`

`u_theta = - partial psi/partial r`

depending on sign convention used by the text.

High-yield questions:

- Find `psi` from given `u` and `v`.
- Plot/identify streamlines.
- Find flow rate between streamlines.

### 9.4 Cauchy's Equation

Cauchy's equation is the momentum equation written in stress form.

Conceptually:

`rho acceleration = body forces + surface stress forces`

It applies generally, but to solve Newtonian fluid problems we need stress-strain relations, which lead to Navier-Stokes.

### 9.5 Navier-Stokes Equation

For incompressible Newtonian flow with constant viscosity:

`rho D V/Dt = -grad P + rho g + mu del^2 V`

Term meanings:

- `rho D V/Dt`: inertia.
- `-grad P`: pressure force per volume.
- `rho g`: body force per volume.
- `mu del^2 V`: viscous diffusion of momentum.

The equation is difficult because it is:

- Nonlinear because of convective acceleration.
- Coupled with continuity.
- Usually partial differential equations.

### 9.6 Solving Simple Differential Flow Problems

Standard simplification workflow:

1. Choose coordinates.
2. State assumptions.
3. Apply continuity.
4. Simplify Navier-Stokes component equations.
5. Integrate.
6. Apply boundary conditions.
7. Calculate derived quantities such as flow rate, shear stress, or pressure gradient.

Common assumptions:

- Steady: time derivatives are zero.
- Incompressible: `div V = 0`.
- Fully developed: axial velocity does not change in flow direction.
- Unidirectional: only one velocity component is nonzero.
- No slip at solid walls: fluid velocity equals wall velocity.
- No penetration: normal velocity at a solid wall is zero.

### Couette Flow

Flow between two infinite plates, one moving and one stationary.

Typical assumptions:

- Steady.
- Incompressible.
- Laminar.
- Fully developed.
- No pressure gradient unless specified.

Velocity profile with top plate speed `U` and gap `h`:

`u(y) = U y/h`

Shear stress:

`tau = mu du/dy = mu U/h`

### Plane Poiseuille Flow

Pressure-driven flow between two stationary parallel plates.

Velocity profile is parabolic.

Key traits:

- No slip at both walls.
- Maximum velocity at centerline.
- Pressure decreases in flow direction.

### Falling Film Flow

Thin liquid film flowing down an inclined/vertical wall.

Driving force:

- Gravity component along the wall.

Resisting force:

- Viscous shear.

Boundary conditions often include:

- No slip at wall.
- Zero shear at free surface if air resistance is neglected.

### Pipe Poiseuille Flow

Fully developed laminar flow in a round pipe.

Velocity profile:

`u(r) = (R^2/(4 mu))(-dP/dx)(1 - r^2/R^2)`

Maximum velocity:

`u_max = (R^2/(4 mu))(-dP/dx)`

Average velocity:

`V_avg = u_max/2`

Flow rate:

`Q = pi R^4 (-dP/dx)/(8 mu)`

Pressure drop form:

`Q = pi R^4 delta_P/(8 mu L)`

This matches the Hagen-Poiseuille equation from Chapter 8.

## Best Solution Patterns to Master

The solution manual contains worked problems for Chapters 5-9. Instead of memorizing exact answers, master these patterns because they are the ones most likely to transfer to a final exam.

### Chapter 5 Best Patterns

1. Continuity with one inlet/one outlet:
   - Use `m_dot = rho A V`.
   - Use `A1 V1 = A2 V2` for incompressible flow.

2. Filling or emptying tanks:
   - For constant flow, `time = volume / Q`.
   - For changing water level, combine Bernoulli with geometry and integrate if required.

3. Bernoulli with continuity:
   - Venturi meters, nozzles, reducers, free jets.
   - Usually two equations: continuity plus Bernoulli.

4. Pitot-static tube:
   - Convert pressure difference into velocity.

5. Mechanical energy balance:
   - Include pump head, turbine head, and losses.
   - Use power relation `rho g Q h`.

### Chapter 6 Best Patterns

1. Pipe elbow force:
   - Momentum in x and y directions.
   - Include pressure forces and support reaction.

2. Nozzle force:
   - High velocity change creates large momentum force.
   - Pressure force may matter at inlet.

3. Jet on plate/vane:
   - Force depends on change in velocity direction and magnitude.
   - Carefully distinguish force on fluid vs force on plate.

4. Momentum correction factor:
   - Use `beta` when specified.

5. Angular momentum:
   - Use tangential velocity components.
   - Power equals torque times angular speed.

### Chapter 7 Best Patterns

1. Dimensions of a variable:
   - Practice pressure, viscosity, surface tension, power, torque, and energy.

2. Buckingham Pi:
   - Drag, pressure drop, pump power, wave force, or flow rate correlations.

3. Model-prototype scaling:
   - Match Reynolds for viscous-dominated flows.
   - Match Froude for free-surface/gravity flows.
   - Match Mach for compressible flows.

### Chapter 8 Best Patterns

1. Single pipe head loss:
   - Compute `Re`.
   - Choose laminar or turbulent friction factor.
   - Use Darcy-Weisbach.

2. Pipe with minor losses:
   - Add `sum K V^2/(2g)` to major loss.

3. Pump power:
   - Find total required head.
   - Use `rho g Q h`.
   - Apply efficiency correctly.

4. Series pipes:
   - Same `Q`, losses add.

5. Parallel pipes:
   - Same head loss, flows add.

6. Venturi/orifice meter:
   - Use pressure difference, continuity, Bernoulli, and discharge coefficient.

### Chapter 9 Best Patterns

1. Continuity check:
   - For incompressible 2D, verify `du/dx + dv/dy = 0`.

2. Missing velocity component:
   - Integrate continuity.

3. Stream function:
   - Use `u = dpsi/dy`, `v = -dpsi/dx`.

4. Material acceleration:
   - Even steady flows can have acceleration if velocity changes with position.

5. Navier-Stokes simplification:
   - Start with assumptions and delete terms carefully.

6. Couette/Poiseuille:
   - Know linear vs parabolic profiles.
   - Know no-slip boundary conditions.

## One-Page Formula Sheet

Continuity:

`m_dot = rho Q = rho A V`

`sum m_dot_in = sum m_dot_out` for steady flow

Bernoulli:

`P/(rho g) + V^2/(2g) + z = constant`

Mechanical energy:

`P1/(rho g) + alpha1 V1^2/(2g) + z1 + h_pump`

`= P2/(rho g) + alpha2 V2^2/(2g) + z2 + h_turbine + h_L`

Pump/turbine power:

`W_dot = rho g Q h`

Linear momentum:

`sum F = sum_out(beta m_dot V) - sum_in(beta m_dot V)`

Angular momentum:

`sum M = sum_out(m_dot r V_theta) - sum_in(m_dot r V_theta)`

Reynolds number:

`Re = rho V D/mu = V D/nu`

Darcy-Weisbach:

`h_L = f (L/D) V^2/(2g)`

Laminar friction factor:

`f = 64/Re`

Minor loss:

`h_L = K V^2/(2g)`

Hagen-Poiseuille:

`Q = pi D^4 delta_P/(128 mu L)`

Buckingham Pi:

`number of Pi groups = n - k`

Continuity differential:

`partial rho/partial t + div(rho V) = 0`

Incompressible:

`div V = 0`

Navier-Stokes, incompressible constant-property:

`rho D V/Dt = -grad P + rho g + mu del^2 V`

Stream function, 2D Cartesian:

`u = partial psi/partial y`

`v = - partial psi/partial x`

## Final Exam Practice Plan

If you have 1 day:

1. Memorize the one-page formula sheet.
2. Practice one Bernoulli/energy problem.
3. Practice one pipe-flow head-loss problem.
4. Practice one momentum force problem.
5. Practice one Buckingham Pi problem.
6. Practice one continuity/stream-function problem.

If you have 3 days:

Day 1:

- Chapter 5 and Chapter 8.
- Do continuity, Bernoulli, mechanical energy, and pipe loss problems.

Day 2:

- Chapter 6 and Chapter 7.
- Do momentum-force and dimensional-analysis problems.

Day 3:

- Chapter 9 and review.
- Do continuity/stream-function/Navier-Stokes simplification problems.
- Redo mistakes without looking at solutions.

## What I Would Expect on the Final

Most likely:

- A Bernoulli/energy equation problem with continuity.
- A pipe-flow loss/pump power problem.
- A control-volume momentum problem asking for force.
- A dimensional analysis or model-scaling problem.
- A differential continuity or stream-function problem.

Possible but less certain:

- Angular momentum/turbomachinery.
- Unsteady draining tank with integration.
- Full derivation of Navier-Stokes simplification for Couette or Poiseuille flow.
- Pipe network with parallel branches.

Least likely unless emphasized by your instructor:

- Long theoretical RTT derivation.
- Very detailed Cauchy stress tensor manipulation.
- Complex incomplete similarity discussion.

## How to Check Whether a Worked Solution Is "Good"

A strong solution should:

1. State assumptions clearly.
2. Use a clear diagram/control volume.
3. Write the governing equation before substituting numbers.
4. Use consistent units.
5. Keep pressure convention consistent.
6. Apply continuity before Bernoulli when velocities are unknown.
7. Include all relevant losses, pumps, turbines, pressure forces, or weights.
8. Show sign convention for vector equations.
9. End with units and a reasonableness check.

A weak solution often:

- Jumps straight to a formula.
- Hides sign conventions.
- Ignores losses without saying why.
- Uses the wrong velocity in minor losses.
- Treats gage and absolute pressure carelessly.
- Calculates pipe friction before checking Reynolds number.
- Gives only a number with no physical interpretation.

