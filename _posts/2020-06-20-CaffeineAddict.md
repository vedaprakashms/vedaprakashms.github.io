---
title: "Do Not Let Computer Doze Off - CaffeineAddict"
author: Ved
categories: software
layout: post
permalink: /software/CaffeineAddict
---
## Introduction
It was a long day, working on a project which required system to not enter sleep mode as my computer was working on a very large file to scan to server. Apart from my system working on its own i did not have any other work to be accomplished that day. My office admin rules does not allow us to change the power settings. I knew i had to take the matters into my own programing hands without breaking any rules. Thus Caffeine Addict was born to fuel up the computer not to enter into sleep mode.

## Background
A computer enters into a sleep mode when its unattended for a long time (time is the variable from mins to hours) to conserve power, although this can be changed in many systems, some company group policies make it nearly impossible to change this setting without breaking the office rules. So the only method for the system to not enter sleep mode is to be *continuously work on keyboard and|or mouse* OR **FAKE IT**.

## Technique used to not let computer Doze off
 Keyboard and Mouse are HID (Human interface devices) devices, that means the computer are bound to trust them as they are locally plugged in. Most of the keyboards keys vary between 80+ keys to 104+ keys. There are keys which are physically not present on any keyboard but still are part of keyboard. These keys can be programmatically emulated so that the computer thinks its getting pressed from the keyboard itself.
 Mouse movement are nothing but co-ordinates on the display screen, thus this could also be emulated to move the mouse from one co-ordinate to another. 

## What is achieved?
 After a through research on the topic, i was not alone who faced this issue. There was thousands if not millions who were looking for similar solution. Some of them had come up with a ingenious method of setting laser mouse on a desk book and let the light dance to **Fake** the mouse movement. there are two problems  with this solution, 1) If we are using a wireless mouse we are simply consuming battery power. 2) Faking the mouse movement by keeping it on a book is a pattern which can be recognized, and companies have also started to look into the same. So I came up with a Software solution. The solutions is simple *use the keys that are not on keyboard so that normal work does not get effected when keyed into the computer* and *move the mouse cursor to random co-ordinates* and *do this at random* (I know generating a true random in computer science is impossible[^random]), But remember *human is a creature of habit* 

## Implementation
***01)*** I had to choose a couple of keys whose key press should not trigger any command on a healthy computer but showoff that there was a key press. For this either i had to choose a combination of keys or the keys which are not present on any keyboard manufactured thus eliminating any potential command input to the computer. This was easily achieved as any standard keyboard contains only function keys till F12, but actually function keys go on till F19[^Func_keys] . So the missing Fkeys from F13 to F19 can be utilized for our job, and i chose F14 and F15.

***02)*** Now I had to chose the mouse movement co-ordinates, this was also simple, i can choose along the top pixel of the display or side pixels of the display as this would just contain the borders of the application, and nothing bad would happen with just the movement along those lines.

***03)*** Generating the random, this is where i was struck for some time. As i too was struck with the true random issue. but i quickly remembered that *human is a creature of habit* and moved on to generate pseudo random numbers. 

***04)*** The actual programing, again here i was in cross roads between multiple things:
- Many companies won't allow external EXE files to be run.
- Many companies won't allow Macros to be run on MSoffice suit.
- Many companies won't allow Visual basic scripts to be run on the system. 

I started to think what are the stats that all 3 conditions are applied in any single company. That would be less than 5%. I can take a chance with 95% people benefiting with this solutions, and give away the source code to the rest 5% that they can tweak to their willing. 

***05)*** Thus i started to program in Python, MS Office excel VBA and VB script. the entire code could be accessed on this github repository [CaffeineAddict](https://github.com/vedaprakashms/CaffeineAddict). 

***06)*** To code in python i used already existing library *"win32api, win32con, time, random, sys"* and followed the same analogy as stated above.

***07)*** To code in VB script i came up with a solution of opening a notepad and start typing in that.

***08)*** To execute in excel i searched on internet to come up with mouse movements and those were emulated via VBA.

***09)*** The Python code being the most efficient and complex so that any pattern could not be determined at a sudden. I converted that to a executable using python to exe converters such as py2exe etc.. 

***10)*** The exe file is now independent and can be used without any harm.
### Usage
```console

x:\> CaffeineAddict.exe 10

```
The above command shall run CaffeineAddict for 10 mins. 

[^random]: [Can a computer generate a truly random number?](http://engineering.mit.edu/engage/ask-an-engineer/can-a-computer-generate-a-truly-random-number/)
[^Func_keys]: [Function_key](https://en.wikipedia.org/wiki/Function_key)