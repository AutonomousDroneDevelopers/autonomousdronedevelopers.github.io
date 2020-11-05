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
# Related

{% include gallery id="gallery_app" caption="" %}

# ![favicon](/assets/images/favicon.ico){: .aligned-left} Crazyflie drone architecture

This tutorial is meant to cover the **specific configuration of the Crazyflie 2.1 drone**. In doing so, the firmware is explored to make the best use of this drone in the lab.

{% include gallery id="gallery_architecture" caption="" %}

<!--{% include gallery id="gallery_2" layout="quarter" class="full" caption="The best ideas for drone guards." %}-->

# Overview: a research drone

<iframe src="{{ page.document_path1 }}" width="100%" height="1000px"></iframe>

{% include video id="tzNdX6B2C3o" provider="youtube" %}


# Drone components


<iframe src="{{ page.document_path2 }}" width="100%" height="1000px"></iframe>


# The Robotic Stack

<iframe src="{{ page.document_path3 }}" width="100%" height="1000px"></iframe>


# Flight scripts

<iframe src="{{ page.document_path4 }}" width="100%" height="1000px"></iframe>


# Connecting and compiling

<iframe src="{{ page.document_path5 }}" width="100%" height="1000px"></iframe>


# Implementation at the DVIC

<iframe src="{{ page.document_path6 }}" width="100%" height="1000px"></iframe>
