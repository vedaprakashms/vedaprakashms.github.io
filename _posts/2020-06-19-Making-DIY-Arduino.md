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












[^ICSP]: [link to ICSPs](https://www.google.com)