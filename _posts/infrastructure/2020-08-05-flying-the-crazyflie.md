---
layout: single
title: "Crazyflie drone architecture"
excerpt: "Information about this drone and its framework."
image:
  header: assets/images/infrastructure/crazyflie.jpg
  teaser: assets/images/infrastructure/crazyflie.jpg
header:
  teaser: assets/images/infrastructure/crazyflie.jpg
  overlay_image: assets/images/infrastructure/crazyflie.jpg

categories: Infrastructure
tags:
- Hardware
- Drone Specimen

toc: true
toc_sticky: true
date: 2019-01-12

gallery:
  - image_path: /assets/images/infrastructure/guards.png
    alt: "fpv drone"
    title: "fpv drone"

  - image_path: /assets/images/infrastructure/guards-2.jpg
    alt: "Custom line-sensors"
    title: "Custom line-sensors"



---


# ![favicon](/assets/images/favicon.jpg){: .aligned-left} Crazyflie drone architecture

This tutorial is meant to cover the **specific configuration of the Crazyflie 2.1 drone**. In doing so, the firmware is explored to make the best use of this drone in the lab.

# A research drone
The Crazyflie 2.1 is a **durable, open-hardware nano quadcopter** that targets hobbyists and researchers. Its small size (92 mm diagonal rotor-to-rotor) and weight (27 g) make it ideal for indoor swarming applications. The firmware is open source and the flexibility of the platform makes it ideal for research, education or other applications where openness and full control is important.

As a fist-sized, **lightweight and re-assemblable** piece of equipment, it offers functional hardware for drone autonomy in a field marred by hardware constraints. Its 6 to 7 minutes of flight time make it practical for testing **autonomous flight algorithms**, and it has become the drone of choice for research laboratories. It is particularly adept to autonomous control and coordination of **multi-robot systems**, since its small size allows for **dense formations with low air turbulence**. It also offers agility in research pertaining to **control optimisation for aggressive manoeuvres**.

{%
include figure
image_path="assets/images/backgrounds/common-stack.PNG"
alt="dev-tutorials"
caption=" "
%}

{% include gallery id="gallery" caption="The best ideas for drone guards." %}


<!-- <iframe src="{{ page.document_path }}" width="100%" height="1000px"></iframe> -->
