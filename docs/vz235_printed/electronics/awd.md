---
layout: default
title: 6.1 AWD specific
parent: 6. Electronics
grand_parent: VzBoT235 - Printed Version
has_toc: false
nav_order: 1
has_children: false
permalink: /vz235_printed/electronics/awd_specific
---

# 6.1 AWD specific

To take best advantage of having 4 motors on X and Y, it is advised to run each motor on individual stepper drivers. Both Klipper & RRF fortunately now natively supports QuadXY. So you will have to download and install your favorite firmware as described in their respective guides.

For Klipper it is recommended to use the provided .cfg file as base or inspiration to make a configuration to suit your own build. It is recommended to copy & paste the given TMC settings as much as possible for the best results both in terms of speed and quality. Although feel free to experiment, because after all that is what VzBoT is all about!

[Credits for the Klipper adaptation to suit 4 motor CoreXY or QuadXY go to TypQxQ on Github]

[https://github.com/TypQxQ/klipper/tree/Multiple_Steppers_on_CoreXY](https://github.com/TypQxQ/klipper/tree/Multiple_Steppers_on_CoreXY)
