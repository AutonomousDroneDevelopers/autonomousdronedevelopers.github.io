---
layout: single
title: "Remapping real drone into simulators (/3)"
excerpt: "How to transfer inputs and outputs between a real drone and simulators."
image:
  header: assets/images/infrastructure/flightgoggles.jpg
  teaser: assets/images/infrastructure/flightgoggles.jpg
header:
  teaser: assets/images/infrastructure/flightgoggles.jpg
  overlay_image: assets/images/infrastructure/flightgoggles.jpg
categories: Infrastructure
tags:
- Simulator
- Crossreality
- ROS

toc: true
toc_sticky: true
date: 2019-01-12

gallery:
  - image_path: /assets/images/posts/service-robot/h-bridge.png
    alt: "Custom h-bridge"
    title: "Custom h-bridge"

  - image_path: /assets/images/posts/service-robot/line-sensors.png
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - image_path: /assets/images/posts/service-robot/voltage-regulator.png
    alt: "Custom voltage regulator"
    title: "Custom voltage regulator"

---

# ![favicon](/assets/images/favicon.ico){: .aligned-left} Remapping real drone into simulators

# [ AREA UNDER DEVELOPMENT ]

This tutorial is meant to cover the procedure for remapping the ROS outputs of two drones in order to have them follow the same trajectory. To do this tutorial, it is important to have some background in ROS, and specifically some experience with RQT graphs. The mapping procedure in itself, is relatively straightforward, provided your two drones provide pose information.

This tutorial is written with videogame developers in mind, since they may be able to derive ways to connect drones to other virtual agents (planes, turtles and human heads.).
