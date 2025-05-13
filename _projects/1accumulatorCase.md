---
layout: project
title: Accumulator Case, Cornell FSAE
description: Accumulator case for Cornell FSAE ARG25
technologies: 
image: /assets/images/radio-machine-cad.jpg
---
## Overview

This year I designed the accumulator case for Cornell FSAE. The case is the main structural element of the accumulator, and it mounts the accumulator to the car and protects the modules in case of a crash. 

## Design Details

The structure must withstand 40g laterally and 20g vertically, and be
waterproof. I decided on a welded aluminum sheet metal case, as it was relatively lightweight and easy to manufacture. The accumulator electronics sits in the front triangular bay, which is angled to be parallel to the 43 degree firewall in the car. There are ports for the two high voltage disconnects, the accumulator service connector, and a USB connector to flash code to the BMS. There is also a pressure relief valve that prevents the case from building up pressure,
and a bolt that allows the electronics to ground to the case. The modules themselves are pinned in place with two AN4 bolts on each side, walls and lid of the case are lined with mica that acts as a thermal and electrical insulator. The floor of the case is lined with thermal interface material to conduct heat away from the cooling fins in the modules.

![Shaded rendering of earlier version]({{ "/assets/images/radio-machine.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

### Lid Information

The lid is bolted on with AN3 bolts into distorted thread rivet-mounted nutplates. I removed the gasket from the front face of the case because the 3/32” thick soft gasket would permit a variable horizontal strain, which would require more precise torsioning align the bolts on the
top face. While that seal was not airtight, the downward sloping face combined with the smooth contact surface provided by countersunk rivets prevented water from entering at that interface. The case proved to be waterproof after several 5 minute rain tests.

![Photo of old radio]({{ "/assets/images/old-radio.jpg" | relative_url }}){: .inline-image-l}

### Floor Information

The floor must be 0.125” thick, while the walls and sides, can be 0.090” thick, so I designed the walls as separate with locating slots to assist in welding. The mounts on the front and back are aluminum so they could be welded to the body of the case, and I validated their strength with
hand calculations and the FSAE Structural Equivalency Spreadsheet. The front mounts needed to be much larger due to the back due to the increased bending moment in the front caused by the large moment arm of the accumulator electronics bay. Nevertheless, since the mounts were
welded, I made the bottom as thick as the case floor so I could use the entire floor in my tear out calculations, effectively cutting the weight of the front mounts in half. In all, it was a 1lb reduction from the previous year’s mounts despite the increased moment.
