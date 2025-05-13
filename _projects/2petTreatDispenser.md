---
layout: project
title: Pet Treat Dispenser
description: Treat dispenser with training clicker
technologies: 
image: /assets/images/dispenser1.png
---

## Overview

I designed and prototyped a pet treat dispenser, that clicks when dispensing treats to simplify the process of conditioning a pet to a clicker. My first prototype consisted of a rotating mechanism that pushed treats out when a lever was pulled down. As the lever released, torsion springs would snap it back to its starting position, where it would collide with a metal pin creating a clicking noise. Simultaneously, the slider in the treat magazine would push another treat ready into position. 

## Design Details

The design featured flat acrylic jigsaw components that I laser cut and superglued together. This allowed for rapid, cheap testing that exposed some of the flaws with this design.

![overview]({{ "/assets/images/dispenser2.png" | relative_url }}){: .inline-image-l}

While the dispenser worked well with regular-shaped, hard “test treats” made of acrylic, soft irregularly shaped dog treats jammed the device, and prevented the trigger from rotating back to the start. To combat this, I redesigned the dispensing mechanism with a linearly actuating button, to minimize the moving surfaces in contact with the treats. With this second iteration, the user presses a button, which directly pushes treats out the front of the device. The button piece contains an overhang so irregular treats do not get wedged in between the slider and the
top and scrape against the top of the device. 

Additionally, I oversized the hole the treats came out of so they would not be pinched by the sliding piece if they were irregularly shaped. The majority of the device remained laser cut acrylic, with only the slider needing to be 3d printed.

Compression springs pushed the dispensing slider back in place after the button was released, but you needed to slide your finger off the button to get a satisfying click. This version occasionally dispensed more than one treat, but jammed much less often, and the compression springs provided a more reliable clicking noise than the rotating trigger.

![clicker]({{ "/assets/images/dispenser3.png" | relative_url }}){: .inline-image-l}

I am currently testing small compliant mechanisms to create a consistent clicking noise at the
start of a button press. These will click at the start of the slider travel and allow the user to “half
click” to create the clicking noise without dispensing a treat, to allow trainers to use variable
reinforcement on their pets as well.