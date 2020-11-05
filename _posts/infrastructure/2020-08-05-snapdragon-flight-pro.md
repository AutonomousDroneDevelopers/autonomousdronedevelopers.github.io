---
layout: single
title: "Flying the Snapdragon Flight Pro"
excerpt: "Information about this drone and its framework."
image:
  header: assets/images/infrastructure/snapdragon-parts1.jpg
  teaser: assets/images/infrastructure/snapdragon-parts1.jpg
header:
  teaser: assets/images/infrastructure/snapdragon-parts1.jpg
  overlay_image: assets/images/infrastructure/snapdragon-parts1.jpg
categories: Infrastructure
tags:
- Hardware
- Drone Specimen

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

# ![favicon](/assets/images/favicon.ico){: .aligned-left} Experiences with the Snapdragon Flight Pro

# [ AREA UNDER DEVELOPMENT ]

This tutorial is meant to cover the Snapdragon Flight Pro, an integrated platform for a VIO-enabled, Snapdragon-chip drone. A background understanding of the Snapdragon board shows the potential of the framework for various applications.

__Bibliography__
A recent paper on “Deep Drone Acrobatics” uses such a VIO-IMU system for highly precise drone acrobatics. By training in simulation, they manage to do zero-shot learning transfer onto the drone for power loops, with a 100% success rate when the VIO is available.
