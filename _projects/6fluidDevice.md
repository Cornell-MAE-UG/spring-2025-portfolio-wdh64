---
layout: project
title: Hydrostatic Transaxle Disection
description: Disect and explain the working principles of a hydrostatic transaxle
technologies: Fluid Mechanics, Fusion 360 
image: /assets/images/HT_Pic.png
---


This is the transaxle we dissected. This exact one was part of a riding lawnmower and allows the wheels to rotate at different rates to allow for smooth turns


Within the transaxle, we found a hydrostatic transmission device. This allows for smooth transitions between speeds without needing to use gears or a clutch. A lever or pedal is moved by the operator that is connected to a swash plate in the housing of a positive displacement piston pump. The piston pump contains 5 cylinders loaded with springs, so when the lever is engaged, the angle of the plate changes and the pistons compress to different amounts. This alters the amount of fluid sent through the lines to the hydraulic motor, where another piston pump gets rotated by the influx of fluid. The rotation then goes through the rest of the transaxle and causes the wheels to spin. The fluid in the motor gets pushed back to the pump, and creates a circular system.

<br>
![Pic1]({{ "/assets/images/HT_Pic1.png" | relative_url }}){: .inline-image style="width: 600px"}
![Pic2]({{ "/assets/images/HT_Pic2.png" | relative_url }}){: .inline-image style="width: 600px"}
![Pic3]({{ "/assets/images/HT_Pic3.png" | relative_url }}){: .inline-image style="width: 600px"}
<br>

This is a simplified diagram of the pump-motor pair. The input shaft drives the pump on the right, and as the pistons reciprocate against the tilted swash plate, they sweep fluid into the closed loop. That flow enters the motor on the left, and because the motor displacement is fixed, continuity requires the motor block to rotate at whatever speed accommodates the incoming volumetric flux. The arrows show flow direction and piston communication throughout the loop, and the section view shows the internals of the system.
The CAD model is shown in a rotational simulation. Even though the pistons are oscillating, we treat the system as steady-periodic, so the cycle-averaged flow and torque can be analyzed as steady.

<br>
![Diagram]({{ "/assets/images/HT_Diagram.png" | relative_url }}){: .inline-image style="width: 600px"}
![HT_Cut]({{ "/assets/images/HT_Cut.gif" | relative_url }}){: .inline-image style="width: 200px"}
![HT_Animation]({{ "/assets/images/HT_Animation.gif" | relative_url }}){: .inline-image style="width: 800px"}
<br>

For this analysis we use several modeling assumptions.
* We treat the hydraulic oil as incompressible.
* We assume steady or periodic operation so that the average flow over one cycle is constant.
The pump and motor chambers are considered rigid, meaning displacement is dictated purely by geometry.
* We assume isothermal operation, so viscosity is treated as constant.
The motor swash plate is fixed.
* We neglect leakage initially to derive the ideal relations, and we assume the charge pump keeps the loop fully filled with no trapped gas.
These assumptions allow the governing equations to reduce to tractable forms directly based on mass, momentum, and energy balances.

<br>
![HT_Slide1]({{ "/assets/images/HT_Slide1.png" | relative_url }}){: .inline-image style="width: 600px"}
<br>

In the pump control volume, flow is determined kinematically. The pump is a positive-displacement axial-piston machine, so the volumetric flow rate is simply the swept volume per radian multiplied by shaft speed. The swept volume depends on the swash-plate angle, which defines the piston stroke through geometric projection. This means the operator’s input directly sets the volumetric boundary condition for the entire hydrostatic loop.

<br>
![HT_Slide2]({{ "/assets/images/HT_Slide2.png" | relative_url }}){: .inline-image style="width: 600px"}
<br>

In the motor, the rotation is not imposed kinematically; instead it is determined by continuity. For a fixed displacement motor, the incoming volumetric flow must equal the net chamber displacement per radian of rotation, which fixes the angular velocity. Torque arises from an angular-momentum balance: pressure acting on each piston produces a force on the thrust plate, creating a net moment. This relation defines how loop pressure translates directly into shaft torque

<br>
![HT_Slide4]({{ "/assets/images/HT_Slide4.png" | relative_url }}){: .inline-image style="width: 600px"}
<br>

To evaluate power transfer, we apply the steady-flow energy equation. The dominant term is the flow-work, equal to volumetric flow times pressure difference. Real behavior deviates from ideal because of leakage in the piston-cylinder clearances and the valve-plate interface. Under lubrication theory, these gaps operate in the thin-film laminar regime, where the Navier–Stokes equations reduce to a Poiseuille-type linear relation between pressure difference and leakage flow. Incorporating leakage into continuity yields the volumetric efficiency, which measures how much usable flow remains available for torque production.

<br>
![HT_Slide5]({{ "/assets/images/HT_Slide5.png" | relative_url }}){: .inline-image style="width: 600px"}
<br>
Here we compared two displacements using the same flow rate of 7 GPM.
For the smaller displacement, the motor spins faster, about 2200 rpm, which gives the mower roughly 8 mph. If we double the displacement, the motor speed is cut in half to around 1100 rpm, and the mower only goes about 4 mph. So the big idea is: smaller displacement gives you higher speed, while larger displacement trades speed for torque.

The dominant governing parameters are the pump and motor displacements, which are fixed by geometry; the loop pressure difference, which drives torque and governs leakage; the leakage conductance, which depends strongly on clearance geometry and viscosity; and the pump shaft speed, which provides the primary kinematic forcing. These parameters define the system’s performance envelope.

In summary, the hydrostatic transmission’s behavior follows directly from mass conservation, momentum balance, and lubrication-scale flow. By modeling the pump, motor, and leakage paths as interacting fluid-mechanical control volumes, we obtain a fully predictive description of torque, speed, and efficiency. Thank you for watching.
