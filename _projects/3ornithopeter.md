---
layout: project
title: Remote Controlled Ornithopter
description: Remote controlled drone that mimics the flight of a bird
technologies: 
image: /assets/images/drone1.png
---

## Overview

Another design I am proud of is my remote controlled ornithopter, or a drone that mimics the flapping motion of bird wings. I worked alongside a partner, where I designed the mechanical aspects of the drone, and he worked on the motor, power, and control.

![progressDrone]({{ "/assets/images/drone2.png" | relative_url }}){: .inline-image-r style="width: 200px"}

## Design Details

I created a two-stage belt drive that produced a 1:16 gear reduction. A belt drive provided the necessary durability, as 3d printed gears proved too fragile to survive a crash. The belt drive connected to a cam that drove the vertical wing oscillations with a linkage connected to universal joints.

![joints]({{ "/assets/images/drone3.pdf" | relative_url }}){: .inline-image-r style="width: 200px"}

The wings featured a joint in the middle that had a range of 10-45 degrees. This gave the wings a smaller cross section perpendicular to motion as they travelled upwards, which created net lift.

![challenges]({{ "/assets/images/drone4.png" | relative_url }}){: .inline-image-r style="width: 200px"}

### Challenges

The main challenge with this device was keeping it lightweight while remaining cheap, since we funded the project out of pocket. My partner scavenged the brushless motor and flight controller from a RC drone, and I used a wooden dowel and 3d print structure for the body of the drone. I spent a little extra on carbon fiber rods because weight on the wings created much larger stresses on the 3d printed joints. The front featured a replaceable crumple zone that would shield the body of the ornithopter when it crashed into the ground.
