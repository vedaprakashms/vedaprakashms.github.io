---
title: Making DIY Arduino "Simpino".
author: Ved
categories: hardware
layout: post
permalink: /hardware/DIY_Simpino
---
## About Simpino. 
The concept of "Simpino" or simple Arduino came into my mind as I was looking for simple single sided arduino with USB capabilities that could be etched on a PCB board at home, and i could not find one that fit the single sided board description. The few i could find on the internet were either removing the USB part, and the controller can be programmed via In Circuit Serial Programmer[^ICSP], thus the controller shall be missing the UART capabilities i.e. Rx & Tx and cant be programed by bootloader. or using another micro controller as intermediatory device of V-USB, which adds huge costs. 

## Simpino's design.
Simplino's design is minimalistic it contains a microcontroller, TTL logic controller, voltage regulator and other minimal components like resistor, capacitor and LEDs on a single sided board and some headder pins/sockets, Complete component list is noted below with quantities. 
Below is the Circuit diagram, the circuit diagram is divided into multiple sections. The circuit diagram is self explanatory. But i shall be going over each sections. The circuit diagram image is a scalable vector graphic so don't worry you can open the image in a new page and get to zoom in as much as you want to get a clear picture. Those who need a offline copy here is a <a href = "..\assets\Hardware_projects_images\Simpino\simpino.pdf" target="_blank"> PDF Link</a> too.
<a href = "..\assets\Hardware_projects_images\Simpino\simpino.svg" target="_blank"><img alt="Template Generate" src="..\assets\Hardware_projects_images\Simpino\simpino.svg"></a>





[^ICSP]: [link to ICSPs](https://en.wikipedia.org/wiki/In-system_programming)