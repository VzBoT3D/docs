---
layout: default
title: 3.2 AWD Motor sync
parent: 3. Gantry
grand_parent: VzBoT330 - Mellow Kit
has_toc: false
nav_order: 2
has_children: false
permalink: /vz330_mellow/gantry/awd_motor
---

# 3.1 Y limit switch
## Overview

![Overview](../../assets/images/manual/vz330_mellow/gantry/awd/overview.png)

## Setup and tuning

After finishing the build one must take care to properly set up the AWD system. It is
important to “sync the motors”. In order to achieve this it is advised to use the following
macro’s in klipper: <br>

```
[gcode_macro enable_stepper]
gcode:
 SET_STEPPER_ENABLE STEPPER=stepper_x ENABLE=1
 SET_STEPPER_ENABLE STEPPER=stepper_x1 ENABLE=1
 SET_STEPPER_ENABLE STEPPER=stepper_y ENABLE=1
 SET_STEPPER_ENABLE STEPPER=stepper_y1 ENABLE=1
```

```
[gcode_macro disable-steppers]
gcode:
 m84
```

### Step 1
Set belt tension like on a normal 2WD VZ330.

### Step 2
Loosen the grubscrews on one of each set of motors, make sure the grub screws will not be
on the flat side of the stepper shaft.

### Step 3
Boot up the printer and order “enable stepper”.

### Step 4
Tighten the stepper grub screws and disable steppers again.