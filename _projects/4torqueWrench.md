---
layout: project
title: Torque Wrench Design
description: A design, material selection and analysis for a Torque Wrench
technologies: ANSYS, MATLAB, Granta
image: /assets/images/TW_Normal_Stress.png
---

## Overview

Here is a project I completed to design a torque wrench using MATLAB hand calcualtions, careful material selection, and ANSYS to validate the design. 


## Design Requirements

The requirements I designed arround were as follows:
* Transmit a moment of 60 in-lbf
* Safety factor X_o = 4 for yield or brittle failure
* Safety factor of X_k = 2 for crack growth (0.04in crack)
* Safety factor of X_s = 1.5 for fatigue
* Steel, aluminum, or titanium alloy
* Contain strain guague that outputs 1.0mV/V at 600 in-lbf

## Design Details

![progressDrone]({{ "/assets/images/TW_CAD_Dimensions.png" | relative_url }}){: .inline-image style="width: 1000px"}

The torque wrench consists of a rectangular handle and drive. The drive has external fillets on the outer edges and internal fillets where it connects to the handle to reduce stress concentrations. The dimensions are shown in the image here.


## Material Selection

To satisfy the requirements, the material needs to have a high yield strength, fracture toughness, and fatigue strength, but also a relatively low young's modulus so that there is enough strain at the strain guague. I settled on Maraging 250 Steel since it fit all of these criteria with a yield strength of 238 ksi, a fracture toughness of 109 ksi sqrt(in) and a fatigue strength of 93.1 ksi. The young's modulus was 2650 ksi.

## MATLAB Hand Calcs

%Material Maraging Steel 250

M = 600; % max torque (in-lbf)
L = 12; % length from drive to where load applied (inches)
h = 0.6; % width
b = 0.3; % thickness
c = 1.0; % distance from center of drive to center of strain gauge
E = 26.5E6; % Young's modulus (psi)
nu = 0.31; % Poisson's ratio
su = 238E3; % tensile strength use yield or ultimate depending on material (psi)
a = 0.04; % crack length (in)
Y = 1.12;
KIC = 109E3; % fracture toughness (psi sqrt(in))
sfatigue = 93.1e3; % fatigue strength from Granta for 10^6 cycles



% Calculate the moment of inertia (I) for the beam
I = (b * h^3) / 12; % moment of inertia (in^4)

d = 1/3*M*l^2/E/I
s = M*h/2/I;

KI = sy*sqrt(pi*a)*Y;

strength_sf = su/s
crack_sf = KIC/KI
fatigue_sf = sfatigue/s 

%strain guage
Mc = M/L*(L-c);
sc = Mc*h/2/I;
strainc = sc/E
output = strainc*1000


displacement =  0.2013 in


strength safety factor = 7.1400


crack safety factor = 2.1535


fatigue safety factor = 2.7930


strain at guague = 0.0012 in/in


output from strain guague = 1.1792 mv/v

## Boundary Conditions
![joints]({{ "/assets/images/TW_Boundary_Cond.png" | relative_url }}){: .inline-image style="width: 1000px"}

## Normal Strain
![joints]({{ "/assets/images/TW_Normal_Strain.png" | relative_url }}){: .inline-image style="width: 1000px"}


## Principal Stess
![joints]({{ "/assets/images/TW_Principal_Stress.png" | relative_url }}){: .inline-image style="width: 1000px"}

## Guague Strain and Guague Selection
![joints]({{ "/assets/images/TW_Strain_at_Guage.png" | relative_url }}){: .inline-image style="width: 1000px"}
<br>
The strain at the guage was 1.127e-3 in/in which translates to 1.127mV/V and satisfies the requirements.

I chose the Micro-Measurements C4a strain guague https://www.digikey.com/en/products/detail/micro-measurements-division-of-vishay-precision-group/MMF403817/9857825. This provided a small enough form factor to fit on the side of the wrench, and measure the point 1in from the drive.


![challenges]({{ "/assets/images/drone4.png" | relative_url }}){: .inline-image-r style="width: 200px"}
