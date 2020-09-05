---
layout: single
title: "Robot Behaviour Planning"
excerpt: "Developing robot behaviours with an event-based planner."
image:
  header: assets/images/algorithmic/behaviour-planner-1.png
  teaser: assets/images/algorithmic/behaviour-planner-1.png
header:
  teaser: assets/images/algorithmic/behaviour-planner-1.png
  overlay_image: assets/images/algorithmic/behaviour-planner-1.png
categories: Algorithms
tags:
- Simulation
- Robot
- Planning

toc: true
toc_sticky: true
date: 2019-01-12

gallery:
  - image_path: assets/images/algorithmic/behaviour-planner-1.png
    alt: "Custom h-bridge"
    title: "Custom h-bridge"

  - image_path: assets/images/algorithmic/behaviour-planner-2.PNG
    alt: "Custom h-bridge"
    title: "Custom h-bridge"

  - image_path: assets/images/algorithmic/behaviour-planner-3.jpg
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

---

# ![favicon](/assets/images/favicon.jpg){: .aligned-left} Robot Behaviour Planning

This tutorial is meant to cover behaviour planning for robots in a variety of event-based scenarios, using Python at first and later with C++. From a wheeled robot executing a sequence of actions, to a drone flying through different waypoints, with everything in between including python classes to abstract key information, C++ pointers for accessing realtime data, or even the SMACH lib for forming rudimentary state machines in python environments.

These tutorials are written for budding roboticists looking to model robot behaviours with robots capable of motion and means of interacting with other robots and humans.

{% include gallery id="gallery" caption="Custom electronics: h-bridges (2), line sensors (8), voltage regulator (1), custom-made for cost." %}

The first step is to understand the key benefits of event-based behaviour planning: why not simply set up a sequence of actions? And there are in fact situations where this is all that is needed. Using a wheeled robot, we program it to search for a friendly face, to approach it and to stop at a certain distance. The Python+ROS code is available on our github.

Having a sequence of actions has its limits. One is code organisation for better troubleshooting. Using a state machine, we learn to better observe all the possible robot states. Using ROS and the TurtleSim, we discover the usefulness of ROS actionlib for using a state machine on a real robot out-of-the-box.

Another approach is event-based. By having the physical environment trigger state changes independently, there is an increase in the flow of the process, which will lead us to a drone flying through different waypoints. This is done first with Python.

Python is great for code prototyping while C++ is better for performance. The advanced version of this tutorial looks to implement C++ rather than Python. In fact, C++ is used in a drone race for autonomous drones called AlphaPilot. The 14th best team in the qualifiers put their code on github, and we will readily analyse their use of C++.

Another issue is edge cases, the bane of robotics. The ROS Podcast features guests that often talk of this problem with state machines is that unpredictable cases will arise.

# Bibliography:
	Some parts of the ROS documentation are difficult of access. This is the case for the SMACH tutorials. These are however greatly encouraged as edge cases are the bane of robotics...
	Using ROS services is a massive simplification of robot behaviour, and you will find research laboratories creating domotics robots who function on a ROS action server with services. Be sure to familiarise yourself with the documentation.

{%
include figure
image_path="assets/images/algorithmic/behaviour-planner-2.PNG"
alt="behaviour-planner-2"
caption="behaviour-planner-2"
%}
