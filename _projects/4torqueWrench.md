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

To satisfy the requirements, the material needs to have a high yield strength, fracture toughness, and fatigue strength, but also a relatively low young's modulus so that there is enough strain at the strain guague. I settled on Maraging 250 Steel since it fit all of these criteria with a yield strength of 238 ksi, a fracture toughness of 109 ksi sqrt(in) and a fatigue strength 93.1 ksi. The young's modulus was 2650 ksi.

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

I chose the Micro-Measurements C4a strain guague https://www.digikey.com/en/products/detail/micro-measurements-division-of-vishay-precision-group/MMF403817/9857825. This provided a small enough


![challenges]({{ "/assets/images/drone4.png" | relative_url }}){: .inline-image-r style="width: 200px"}
