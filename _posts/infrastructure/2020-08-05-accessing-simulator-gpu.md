---
layout: single
title: "Accessing the Simulator GPU remotely"
excerpt: "How to make use of the Simulator GPU from your own PC."
image:
  header: assets/images/infrastructure/gpu-tut.jpg
  teaser: assets/images/infrastructure/gpu-tut.jpg
header:
  teaser: assets/images/infrastructure/gpu-tut.jpg
  overlay_image: assets/images/infrastructure/gpu-tut.jpg
categories: Infrastructure
tags:
- Simulator
- GPU


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

# ![favicon](/assets/images/favicon.ico){: .aligned-left} Accessing the Simulator GPU remotely

This tutorial is meant to cover the procedure for visualising the RTX screen from your home computer over the DVIC VPN. A clear understanding of the security protocols will help you peel back the correct security layers of X-display, a protocol that is riddled with complexity.

This tutorial is written with drone developers in mind, since our Simulator GPU has the robotics framework set up for developers to test their code remotely.
