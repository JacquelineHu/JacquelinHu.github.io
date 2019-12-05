---
layout: project
title: 'Companion Robots'
date: 14 May 2019
image: /assets/img/projects/companion_robots.jpg
screenshot: /assets/img/projects/companion_robots.jpg
#links:
#  - title: Website
#    url: https://hydecorp.github.io/hy-push-state/
#  - title: Source
#    url: https://github.com/hydecorp/hy-push-state
caption: Establish a companion robot on Raspberry Pi!
description: >
  Establish a companion robot on Python and Raspberry Pi.
accent_color: '#4fb1ba'
accent_image:
  background: 'linear-gradient(to bottom,#193747 0%,#233e4c 30%,#3c929e 50%,#d5d5d4 70%,#cdccc8 100%)'
  overlay:    true
---

# Companion Robots for the Elderly

## Background
Aging has grown to be a social problem in China. Survey shows that nearly 50% of the elderly believe that the lack of children's companion is the biggest problem in elderly care. On the other hand, for those young people, living habits, age differences, work pressure and other resons decline their opportunities to communicate with their parents.

iFamily is an emotional companion robot for the elderly. To improve its connectivity with the elderly emotionally, we conceive an idea of designing a personalized outlook which resembles the elderly's family. Here in our prototype, we manager to 3D print a cartoon outlook to represent our idea.

## Overall establishment
Our robot is bulit with Raspberry Pi and peripherals covered by 3D printed shell. We use Python to implement functions such as speech interactions and video calls. Here I'll breifly introduce every section and its implementation:
* <a href="#hardware">Hardware</a>  
* <a href="#speech interaction with people">Speech interaction with people</a>  
* <a href="#speech interaction with robots">Speech interaction with robots</a>  
* <a href="#video call">Video call</a>  

### Hardware
* 3D printed shell
* Raspberry Pi 3B+ + Linux / <a href="https://www.raspberrypi.org/downloads/">NOOBS</a> + SD card 32G
* 3.5 inch LCD
* Caremer
* Mobile speaker + recorder
* Actuator
* External power supply
![hardware](/assets/img/projects/components.png)

### Speach interaction
* **Package: PyAudio on Python**: recording, voice activity detection and voice play back
* **Package: RPi.GPIO**: actions implementation
* **Baidu API**: automatic speech recognition and text-to-speech
* **Turling API**: natural language generation

