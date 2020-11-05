---
layout: archive
permalink: /about/
title: "Drones at the DVIC"
header:
  overlay_image: /assets/images/backgrounds/paris-skyline.jpg
#classes: wide

last_modified_at: 2019-06-11T11:22:24-05:00
toc: false

gallery_software:
  - url: https://autonomousdronedevelopers.github.io/algorithms/intro-autonomy/
    image_path: /assets/images/frontpage/software/1.PNG
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/algorithms/drone-bot-design/
    image_path: /assets/images/frontpage/software/2.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/behaviour-planning/
    image_path: /assets/images/frontpage/software/3.PNG
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/performance/linux-and-ros-background/
    image_path: /assets/images/frontpage/software/4.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/drone-control-architecture/
    image_path: /assets/images/frontpage/software/5.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/trajectory-generation/
    image_path: /assets/images/frontpage/software/6.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

gallery_hardware:
  - url: https://autonomousdronedevelopers.github.io/infrastructure/flying-the-crazyflie/
    image_path: /assets/images/frontpage/hardware/1.PNG
    alt: "flying-the-crazyflie"
    title: "flying-the-crazyflie"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/optitrack/
    image_path: /assets/images/frontpage/hardware/2b.PNG
    alt: "optitrack"
    title: "optitrack"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/drone-guards-and-tips/
    image_path: /assets/images/frontpage/hardware/3.PNG
    alt: "drone-guards-and-tips"
    title: "drone-guards-and-tips"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/arena-maintenance/
    image_path: /assets/images/frontpage/hardware/4.PNG
    alt: "arena-maintenance"
    title: "arena-maintenance"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/diy-drone-guide/
    image_path: /assets/images/frontpage/hardware/5.PNG
    alt: "diy-drone-guide"
    title: "diy-drone-guide"

  - url: https://autonomousdronedevelopers.github.io/infrastructure/snapdragon-flight-pro/
    image_path: /assets/images/frontpage/hardware/6.PNG
    alt: "snapdragon-flight-pro"
    title: "snapdragon-flight-pro"

gallery_interface:
  - url: https://autonomousdronedevelopers.github.io/algorithms/intro-autonomy/
    image_path: /assets/images/frontpage/interface/1.PNG
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/algorithms/drone-bot-design/
    image_path: /assets/images/frontpage/interface/2.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/behaviour-planning/
    image_path: /assets/images/frontpage/interface/3.PNG
    alt: "fpv drone"
    title: "fpv drone"

  - url: https://autonomousdronedevelopers.github.io/performance/linux-and-ros-background/
    image_path: /assets/images/frontpage/interface/4.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/drone-control-architecture/
    image_path: /assets/images/frontpage/interface/5.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

  - url: https://autonomousdronedevelopers.github.io/algorithms/trajectory-generation/
    image_path: /assets/images/frontpage/interface/6.PNG
    alt: "Custom line-sensors"
    title: "Custom line-sensors"

    gallery_net:

      - url: https://autonomousdronedevelopers.github.io/arena/arena1
        image_path: /assets/images/frontpage/arena/arena1.jpg
        alt: "Custom line-sensors"
        title: "Custom line-sensors"

      - url: https://autonomousdronedevelopers.github.io/arena/arena2
        image_path: /assets/images/frontpage/arena/arena2.jpg
        alt: "Custom line-sensors"
        title: "Custom line-sensors"

    gallery_gpu:

      - url: https://autonomousdronedevelopers.github.io/arena/arena3
        image_path: /assets/images/frontpage/arena/arena3.jpg
        alt: "Custom line-sensors"
        title: "Custom line-sensors"
---


<h2>Official site of the DVIC Drone Lab.</h2>

<h1>We are an upcoming tech lab at La Defense, Paris. </h1>

<h2>The DVIC Drone Lab operates at a Fablab in the De Vinci Innovation Center. We develop drones and robotic systems. We have a drone arena which we use for experimentation and testing.</h2>

<iframe width="727" height="409" src="https://www.youtube.com/embed/d1gjkAIj0SM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<h1> </h1>
<h1>The platform is in beta stage and we welcome anyone interested in using it.</h1>

<h2>Our robots are localized with sub-millimetre level precision. To achieve this, the drone arena is fitted with a system of infrared cameras. The drone can be flown according to this information and executes figures in a tight latency loop of 28 ms. </h2>

<iframe width="727" height="409" src="https://www.youtube.com/embed/zLfq-wvAdsE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<h1> </h1>
The overhead camera records each test, and you can watch the stream in realtime on [Twitch](https://dashboard.twitch.tv/u/autonomousdronedevelopers).

<h2>Drones are localized and flown end-to-end from Python and C++ code. In the tradition of robotics research laboratories, infrared cameras are used to detect exact drone position. These cameras are integrated into the Crazyswarm control framework from the University of Southern California. Using this infrastructure, Crazyflie drones receive commands from our local GPU. Models can be trained and tested from the lab GPU. You can find more details on all these technologies under the Technologies tab. </h2>


{% include gallery id="gallery_gpu" caption="See [GPU specs](https://fr.msi.com/All-in-One-PC/Gaming-24GE-2QE)" %}

See [an introduction to the crazyswarm framework](https://autonomousdronedevelopers.github.io/infrastructure/crazyswarm-synchronisation/).

See [an intro to the crazyflie drone ](https://autonomousdronedevelopers.github.io/infrastructure/flying-the-crazyflie/).

{% include gallery id="gallery_net" caption="See [an introduction to Optitrack motion capture](https://autonomousdronedevelopers.github.io/infrastructure/optitrack/)." %}

<h1>Resources (under development).</h1>
<h2>The platform is in beta stage and we welcome anyone interested in using it.</h2>

<h2>Software.</h2>

<h2>We are exploring technologies for various projects.</h2>

{% include gallery id="gallery_software" layout="fourth" class="full" caption="" %}

<h2>Hardware.</h2>

<h2>We have equipment for drone conception, maintenance and other development.</h2>

{% include gallery id="gallery_hardware" layout="fourth" class="full" caption="" %}

<h2>An interface.</h2>

<h2>We are currently developing virtual-to-real infrastructure to visualise robots in their environment.</h2>

<iframe width="727" height="409" src="https://www.youtube.com/embed/tNqYDqC6wo4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

{% include gallery id="gallery_interface" layout="fourth" class="full" caption="" %}

<!--SOFTWARE STACK -->
<!--
{%
include figure
image_path="assets/images/backgrounds/common-stack.PNG"
alt="dev-tutorials"
caption=" "
%}

<h2>Hardware.</h2>
{%
include figure
image_path="assets/images/backgrounds/equipment.PNG"
alt="dev-tutorials"
caption=" "
%}

<h2>An interface.</h2>
{%
include figure
image_path="assets/images/backgrounds/v2r.PNG"
alt="dev-tutorials"
caption=" "
%}
-->




<!-- PHOTOS OF PROJECTS
{%
include figure
image_path="assets/images/backgrounds/projects.PNG"
alt="dev-tutorials"
caption=" "
%} -->

<!-- ORGANISE WELL BEFORE MAKING PUBLIC
https://trello.com/b/Jfb8EjCc/stage-dvic
-->
<!-- PRIVATE
Contact us at autonomousdrones@gmail.com and we will be in touch with you shortly.
-->
