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


gallery_architecture:

  - image_path: /assets/images/infrastructure/crazyflie/architecture.png
    alt: "architecture"
    title: ""

gallery_autonomous:
  - url: https://autonomousdronedevelopers.github.io/performance/linux-and-ros-background/
    image_path: /assets/images/icons/linux-ros-background.png
    alt: "Custom line-sensors"
    title: "Custom line-sensors"


gallery_app:
  - url: https://autonomousdronedevelopers.github.io/performance/ros-applications/
    image_path: /assets/images/icons/ros-app.png
    alt: "fpv drone"
    title: "fpv drone"

gallery_2:
  - url: https://autonomousdronedevelopers.github.io/infrastructure/optitrack/
    image_path: /assets/images/icons/optitrack.png
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/ros-remapping-to-simulator/
    image_path: /assets/images/icons/reremap.png
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/performance/ros-applications/
    image_path: /assets/images/icons/ros-app.png
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/visualising-ros-data/
    image_path: /assets/images/icons/ros-data.png
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/snapdragon-flight-pro/
    image_path: /assets/images/icons/snapdragon.png
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

document_path1: /assets/docs/crazyflie/Overview.pdf
document_path2: /assets/docs/crazyflie/Drone_components.pdf
document_path3: /assets/docs/crazyflie/The_Robotic_Stack.pdf
document_path4: /assets/docs/crazyflie/Flight_scripts.pdf
document_path5: /assets/docs/crazyflie/Connecting_and_compiling.pdf
document_path6: /assets/docs/crazyflie/Implementation_DVIC.pdf

---


# ![favicon](/assets/images/favicon.jpg){: .aligned-left} Crazyflie drone architecture

This tutorial is meant to cover the **specific configuration of the Crazyflie 2.1 drone**. In doing so, the firmware is explored to make the best use of this drone in the lab.

{% include gallery id="gallery_architecture" caption="" %}

# Useful links

Starting point for the Crazyflie 2.1
https://www.bitcraze.io/documentation/start/
External projects based on the Crazyflie
https://www.bitcraze.io/support/external-projects/
For drone maintenance, please refer to the drone tips tutorial.
{% include gallery id="gallery_app" caption="" %}

{% include gallery id="gallery_2" layout="quarter" class="full" caption="The best ideas for drone guards." %}

# Overview: a research drone

<iframe src="{{ page.document_path1 }}" width="100%" height="1000px"></iframe>

The Crazyflie 2.1 is a **durable, open-hardware nano quadcopter** that targets hobbyists and researchers. Its small size (92 mm diagonal rotor-to-rotor) and weight (27 g) make it ideal for indoor swarming applications. The firmware is open source and the flexibility of the platform makes it ideal for research, education or other applications where openness and full control is important.

As a fist-sized, **lightweight and re-assemblable** piece of equipment, it offers functional hardware for drone autonomy in a field marred by hardware constraints. Its 6 to 7 minutes of flight time make it practical for testing **autonomous flight algorithms**, and it has become the drone of choice for research laboratories. It is particularly adept to autonomous control and coordination of **multi-robot systems**, since its small size allows for **dense formations with low air turbulence**. It also offers agility in research pertaining to **control optimisation for aggressive manoeuvres**.

{% include video id="tzNdX6B2C3o" provider="youtube" %}

# Drone components

<iframe src="{{ page.document_path2 }}" width="100%" height="1000px"></iframe>

The architecture is as follows (for 2.0 and 2.1 versions):
{% include gallery id="gallery_architecture" caption="" %}

	STM32F405: main microcontroller, used for state-estimation, control, and handling of extensions. (Cortex-M4, 168 MHz, 192 kB SRAM, 1 MB flash).
	nRF51822: radio and power management microcontroller. (Cortex-M0, 32 MHz, 16 kB SRAM, 128 kB flash).
	MPU-9250: 9-axis inertial measurement unit.
	LPS25H: pressure sensor.
	8 kB EEPROM.
	uUSB: charging and wired communication.
	Expansion port (I2C, UART, SPI, GPIO).
	Debug port for STM32. An optional debug-kit can be used to convert to a standard JTAG-connector and to debug the nRF51 as well.

# The Robotic Stack

In terms of robotic functionality, the Crazyflie packages the full robotic stack. After all, the firmware, built on the FreeRTOS operating system, is opensource and modifiable. FreeRTOS handles the scheduling of processes and control the flight calculations. This robotic stack includes its own state estimator, control architecture and trajectory follower, which work out of the box. These algorithms are detailed on the Bitcraze website, and they can be customised at compile time. Note however the lack of localization framework, which calls for added modules, or an external localization system. There are two in-house position systems in the Crazyflie ecosystem: the Ultra Wide Band based Loco Positioning System and the Lighthouse positioning system, based on HTC Vive. It is also possible to integrate with external positioning systems, for instance Motion Capture systems.

If you are interested in learning more about autonomous drones, please consult this tutorial:
{% include gallery id="gallery_autonomous" caption="" %}

# PDF version of this post:
