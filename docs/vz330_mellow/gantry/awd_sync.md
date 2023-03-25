---
layout: default
title: 4.2 AWD Motor sync
parent: 4. Gantry
grand_parent: VzBoT330 - Mellow Kit
has_toc: false
nav_order: 2
has_children: false
permalink: /vz330_mellow/gantry/awd_motor
---

# 4.2 AWD Motor sync
## Overview

![Overview](../../assets/images/manual/vz330_mellow/gantry/awd/overview.png)

## Belt routing

The belt routing for an AWD setup should look like the following

![Overview](../../assets/images/manual/vz330_mellow/gantry/awd/belt.png)

### Videos for belt routing

[![Build routing](../../assets/images/manual/vz235_printed/gantry/belt_routing_video.png)](https://www.youtube.com/watch?v=Ibi27Toh-pg&t=2s "Build routing")

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

## Video for tensioning

[![Build tensioning](../../assets/images/manual/vz235_printed/gantry/belt_tentioning_video.png)](https://www.youtube.com/watch?v=qNMXW6MUV5E&t=401s "Build tensioning")
<br>
<br>

### Step 1
Set belt tension like on a normal 2WD VZ330.

### Step 2
Loosen the grubscrews on one of each set of motors, make sure the grub screws will not be
on the flat side of the stepper shaft.
<br>
**This is important the grub screw should NOT be screwed to flat side of the shaft, otherwise a synchronisation is impossible to achive*

### Step 3
Boot up the printer and order “enable stepper”.

### Step 4
Tighten the stepper grub screws and disable steppers again.