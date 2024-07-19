---
title: "Low-cost Autonomous UAV"
excerpt: "A DIY drone capable of autonomous flight and object recognition, all for under $800!"
header:
  teaser: /assets/img/DroneOutside.jpg
gallery:
  - url: /assets/img/DroneTeam.jpg
    image_path: assets/img/DroneTeam.jpg
    alt: "placeholder image 1"
  - url: /assets/img/DroneOutside.jpeg
    image_path: assets/img/DroneOutside.jpg
    alt: "placeholder image 2"
  - url: /assets/img/DroneFloor.jpg
    image_path: assets/img/DroneFloor.jpg
    alt: "placeholder image 3"
  - url: /assets/img/DroneAir.jpg
    image_path: assets/img/DroneAir.jpg
    alt: "placeholder image 4"
---

## Project Overview: Building a Budget Autonomous Drone

For this project, I worked with a team of four other engineers to design and prototype a low-cost autonomous UAV for Lockheed Martin using off-the-shelf parts and open-source software. The idea was to make a modular drone that could handle perimeter surveillance autonomously, all while mminimizing costs.

**Key Goals:**
1. **Modularity**: Easy to adapt for different tasks.
2. **GPS Positioning**: Accurate location tracking.
3. **On-board Imaging and Sensing**: Capturing and processing live images.
5. **Autonomy**: Basic autonomous flight and object recognition.
6. **Cost-Efficiency**: Keep the project under $800.

## Our Journey from Start to Finish

**1. Research and Design**
   - Since we were all new to the drone world, we started with a lot of brainstorming and research to discover what goes into fabricating a drone. Then, along with our sponsor, Lockheed Martin, we defined the scope of our project, divided the project into deliverable chunks, and created a rough timeline for each deliverable.
   - We spent the first stretch of our project choosing the best hardware and software for our drone. We were provided with a Jetson Nano for on-board image processing as well as a Pixhawk 6C flight controller. Each team member chose a different component to research more in-depth, so each component had its own set of justifications we could share with our sponsor. 

**2. Prototyping**
   - The next deliverable was a physical drone. Once all of our selected parts arrived, we got to work assembling the frame, soldering the components together, and neatly wiring everything to the central Pixhawk controller.
   - While this seemed like the most straight-forward section of the project initially, we faced the most challenges during this time. We were confident in the performance of our selected parts, however, wiring together an assortment of components from different brands was difficult given the limited margin of error on a drone body. 

**3. Programming**
   - This phase involved writing the flight programs and developing the object detection systems. We knew attempting to program a custom drone interface would be unrealistic given our timeframe for this project (one semester), so we utilized ArduPilot for our autonomous flight patterns, and OpenCV along with YoloV8 for object tracking and recognition.
   - During this time, we also ensured we were as ready as we could be to test the drone once that time came. We calibrated the motors, ESCs, and GPS on our drone, and each member of the team took some time to research drone regulations and get certified in drone flying. Since we would be testing our drone on a school campus, we also had to contact a legal professional to ensure we were only flying and capturing video in permitted areas.

**4. Testing**
   - Testing was all about making sure everything worked as expected. It was a lot of trial and error, but seeing the drone take its first autonomous flight was worth it.
   - We first tested the drone manually to ensure our thrust and power calculations were correct, then programmed a series of autonomous flight patterns for the drone to attempt.
   - The drone was successfully able to fly autonomously between two set waypoints on a map, recognize objects in real-time, and return to its original take-off point once its battery was depleted.

## Challenges We Faced

**Part Delays:** Some of the parts we ordered took a long time to arrive, which delayed our timeline significantly. This was especially apparent when our only set of propellers broke while testing the drone, and we had to wait a full week for our new ones to arrive before we could resume testing.

**Unrealistic Initial Expectations:** We started off a bit too ambitious with our scope, originally planning to have a network of drones that could communicate with each other and send information back to a base station. As our project progressed in the early stages, we had to scale back and adjust our plans several times.

**Compatibility Issues:** Not all the off-the-shelf parts played nice together. We had to get pretty creative, rigging things up to make them work and designing custom 3D-modeled brackets to fit our frame.

## Budget and Constraints

- We had to keep our spending under $800, which was tight but doable with careful planning.
- Some components like the flight controller and on-board computer were provided (though still included in the budget).
- We also had to make sure we followed all local and FAA regulations.

## Wrapping Up

Despite the bumps along the road, we managed to build a functional, low-cost autonomous drone. It was a fantastic learning experience, testing our problem-solving skills and ability to work as a team. Our drone met the key objectives of being able to recognize objects and achieving basic autonomous flight, setting a great foundation for future improvements.

Check out our [project on GitHub](https://github.com/wal627/milo-the-drone) if you're interested!
Additionally, see our [full report](DroneFinalReport.pdf) for this project and our [component selection list](UAVComponentList.pdf)!

## Gallery
{% include gallery caption="Drone Gallery" %}

