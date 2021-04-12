---
layout: single
title: "Crazyswarm framework for synchronised flight"
excerpt: "ROS for System Integration: a (more) versatile work environment.."
image:
  header: /assets/images/infrastructure/crazyswarm.jpg
  teaser: /assets/images/infrastructure/crazyswarm.jpg
header:
  teaser: /assets/images/infrastructure/crazyswarm.jpg
  overlay_image: /assets/images/infrastructure/crazyswarm.jpg
categories: Infrastructure
tags:
- Hardware
- Drone swarming

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

#document_path: ../../assets/docs/crazyswarm_overview.pdf


---

# ![favicon](/assets/images/favicon.ico){: .aligned-left} Networking setup and benchmarking

# Summary
The main idea of a robotics OS is to avoid continuously reinventing the wheel, and to offer standardised functionalities performing hardware abstraction, just like a conventional OS for PCs, hence the analogous name.
I decided to do a software procedures tutorial that attempts to
-	simplify the ROS procedures in the interest of computation.
-	Give you some relativity in showing how many complicated networking concepts were circumvented at the DVIC.
-	Concrete coding evidence will prove the usefulness of ROS, in the context of the drone demoes at the De Vinci Innovation Center.
This tutorial is meant to cover the crazyswarm framework and how to use it for synchronised drone flight. This framework offers all the necessary components for controlling multiple drones remotely, by relating the drone flight controller of the Crazyflie to a set of controllers on the PC, but also by offering ways to send trajectories to the drones in realtime.

## Quick Links
Some key links The official changelog https://crazyswarm.readthedocs.io/en/latest/changelog.html
Set up (Read the docs yourself!) https://crazyswarm.readthedocs.io/en/latest/
Theoretical underpinnings: http://act.usc.edu/publications/Preiss_ICRA2017.pdf
To-the-point powerpoint: https://drive.google.com/file/d/15favAyrLLpC_O6nrAp-eIbZijFUMLgwV/view

# State of the art
This is also directed at interaction designers who look to fly multiple drones using their own choice of inputs. The main challenges in swarm robotics are addressed in this framework, namely the system latency in terms of system communication, and channel testing for the best signal possible
https://robots.ros.org/
All robots that use ROS so far.

## Real Time Operating System: RTOS
### Introduction
[The Bobble-Bot: GIF and different activities performed simultaneously]
Using an RTOS is often driven by the need to support a system with hard real-time requirements. Hard real-time systems have strict deadlines for when data must be processed and are considered to fail if an event fails to occur or is performed late.
But if you need to run more than one task, and possibly some kind of interprocess communication, it usually doesn't make sense to roll your own task scheduler and communication primitives: it is better to use an RTOS to do this. Avoiding reinventing the wheel reduces development time, debugging, and testing effort, especially in safety critical devices where you may need to demonstrate that all possible risks and faults have been addressed and mitigated.

### RTOS for quadrotors

[The Drone: GIF of activities and Ecosystem]

In each loop cycle, the vehicle reads its Inertial Measurement Unit (IMU) and runs the state estimator, trajectory evaluator, and position controller. Messages with external pose estimates arrive asynchronously and are fused into the state estimate on the next cycle.

## Robotic Operating System: ROS

It provides not only standard operating system services (hardware abstraction, contention management, process management), but also high-level functionalities (asynchronous and synchronous calls, centralised database, a robot configuration system, etc.).

The basic principle of a robot operating system is to run a great number of executables in parallel that need to be able to exchange data synchronously or asynchronously. For example, a robotics OS needs to query robot sensors at a set frequency (ultrasound or infra-red distance sensor, pressure sensor, temperature sensor, gyroscope, accelerometer, cameras, microphone, etc.), retrieve this data, process it (carry out what is known as a data merge), pass it to processing algorithms (speech processing, artificial vision, SLAM - simultaneous localisation and mapping, etc.) and lastly control the motors in return. This whole process is carried out continuously and in parallel. Moreover, the robotics OS needs to manage contention to ensure efficient access to robot resources.

[INSERT PRE-EXISTING ROS-GAZEBO // SOTA, HERE – BEST SO FAR, LINK UNDERNEATH.]

The concepts brought together in ROS under the name of “ROS Computation Graph”, enabling these objectives to be reached, are described below. These are concepts used by the system as it is running, whereas the ROS File System is a static concept (the stack, packages, nodes, etc.)

[See ROS Graph of DRONE LAB, including colourful annotations of other software.]

If you’d like a quick synthesis of ROS, with advantages and disadvantages compared to other systems, please head over to https://blog.generationrobots.com/en/ros-robot-operating-system-2/  . In this tutorial, we will assume you already understand the conceptual layers of ROS. We will be providing concrete evidence for the usefulness of ROS, specifically for the drone demoes at the De Vinci Innovation Center.

## Other general-purpose operating systems for robots

There are a few operating systems or robot middleware worth mentioning:
-	Microsoft Robotics Developer Studio: a multiplatform system, created by Microsoft. It is free and provides a simulation tool; however, it is only compatible with Windows and is programmed with a managed .NET language (preferably C#);
-	NAOQi: open source robotics system produced for the NAO robot by Aldebaran Robotics, and programmed in C++ or Python;
-	URBI : produced by the French company Gostai. URBI is a good multi-platform, open source and offers its own scripting language (URBIScript), although it is also programmed in C++.
There are many embedded systems specific to one particular robot, but this is taking us away from the multi-platform model.


# Applying ROS in the DVIC Drone Lab

Several onboard computers or boards connected via Ethernet, plus sometimes offboard computers for intensive computation tasks. A peer-to-peer architecture coupled to a buffering system and a lookup system (a name service called ‘master’ in ROS), enables each component to dialogue directly with any other, synchronously or asynchronously as required.

[GIF OF ADEM’S LAPTOP CONNECTING TO DRONE PLATFORM]
Caption: We can easily pair up a Linux distro to the Drone GPU to act as a controller.

As the number of drones increases, an interesting swarm feature is managing large numbers of drones. Crazyswarm offers command-line tools and a GUI for mass rebooting, firmware updates, firmware version query, and battery voltage checks over the radio. A power-save mode turns off the main microcontroller and LED ring while leaving the radio active, permitting powering on the Crazyflie remotely.

chooser.py GUI + [ROS Code]

In building applications, an API simplifies programming by abstracting the underlying implementation and only exposing objects or actions the developer needs. Imagine we want to turn on and off a drone through simple coding commands.
ROS’ philosophy can be summarised in the following five main principles:
-	Peer-to-Peer
-	Tools-based (microkernel)
-	Multi-language
-	Thin
-	Free and open source.

We will be providing concrete evidence for each point above, since they simplify the drone demoes at the De Vinci Innovation Center.
ROS gives us the tools to interact with individual drones in a fleet. ROS is built to act as an API, by setting up remote procedure calls (RPC) that interface with the drones’ STM32: via request-response and publish-subscribe. We investigate two ways ROS interfaces with the drones:

-	We could set up an API via a ROS Parameter Server
-	We could broadcast commands in real-time
-	We could launch a ROS Action Server for each drone separately
-	We can control different elements of the demo in a modular manner.

## a.	Quickly modifying the drone configurations

[maybe add what elements query this server?]
The Master includes a heavily-used component called the _Parameter Server_, also implemented in the form of XMLRPC, and which is, as the name implies, a kind of centralised database within which nodes can store data and, in so doing, share system-wide parameters.

## b.	ROS crazyflie_tools. A request-response thing.
[Let’s see that ROS] | [Classic API calls]

## c.	Each drone has a separate server, increasing system modularity
[drone server launchfiles]
Each Drone can make use of the ROS Action Servers separately.
The Master is a node declaration and registration service, which makes it possible for nodes to find each other and exchange data. The Master is implemented via XMLRPC.


## d.	Easy to modify elements of the drone demo on request

-	Thin
entangled to a lesser or greater degree with the robotics OS and are therefore hard to reuse subsequently, ROS developers intend for drivers and other algorithms to be contained in standalone executables. Ie. maximum reusability and, above all, keeps its size down
-	Free and open source
ROS passes data between modules using inter-process communications and, as a result, modules do not need to be linked within a single process, thereby making the use of different licences a possibility.
[would be great to compare Mediapipe ROS-version vs DIMITRI-version]
uses code (drivers and algorithms) from other open source projects:
  -	Player/Stage project simulators
	- Image processing and artificial vision libraries from OpenCV
	- Planning algorithms from OpenRave

For a full list of the available algorithms, visit: http://www.ros.org/wiki/StackList
