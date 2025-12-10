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

The torque wrench had 

![joints]({{ "/assets/images/drone3.png" | relative_url }}){: .inline-image-r style="width: 200px"}

The wings featured a joint in the middle that had a range of 10-45 degrees. This gave the wings a smaller cross section perpendicular to motion as they travelled upwards, which created net lift.

![challenges]({{ "/assets/images/drone4.png" | relative_url }}){: .inline-image-r style="width: 200px"}

### Challenges

The main challenge with this device was keeping it lightweight while remaining cheap, since we funded the project out of pocket. My partner scavenged the brushless motor and flight controller from a RC drone, and I used a wooden dowel and 3d print structure for the body of the drone. I spent a little extra on carbon fiber rods because weight on the wings created much larger stresses on the 3d printed joints. The front featured a replaceable crumple zone that would shield the body of the ornithopter when it crashed into the ground.
