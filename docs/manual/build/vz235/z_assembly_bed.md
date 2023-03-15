---
layout: default
title: 2. Z - Assembly & Bed
parent: VzBoT Vz235 - Printed
grand_parent: Manual
has_toc: false
nav_order: 2
has_children: false
permalink: /manual/vz235/z_assembly
---

# 2. Z - Assembly & Bed

## Overview
![Z Overview](/assets/images/manual/vz235/z_assembly/overview.png)
<br>
<br>

The proper alignment procedure of the VZ235 is the same as on the VZ330 only difference is the length of the alignment tools. Make sure to check out the YouTube video explaining how to align your Z-assembly, so it is both smooth and lines up with the possible travel of the printhead.
### Video tutorial

[![Z Overview](/assets/images/manual/vz235/z_assembly/z_assembly_video.png)](https://www.youtube.com/watch?v=JvF-UNoDB_I "Z Overview")

## BOM

| Material        | Quantity          | Notes |
|:-------------|:------------------|:------|
| M5/M6 10mm buttonhead           | 20 | Depending on the type of 2020 you use, you need M5 or M6 screws  |
| 385mm 2020 extrusion | 4   | Yellow  |
| 375mm 2020 extrusion           | 6      | Red   |
| 470mm 2020 extrusion           | 4 | Blue  |
| 385mm 2020 extrusion           | 1 | Only for 2WD, mount the same as Y gantry extrusions  |
| 2020 corner joints           | 18 | -  |
| 2020 blind corner joints           | 4 | -  |
| STL files ... | 2 | - |

## STL

| File name | Amount to print |
|-----------|-----------------|
| File 1 | 4 |

### Step 1

First assemble your bed assembly, make sure the bed frame is on a flat surface when assembling. Insert the linear bearings in their brackets and attach them to the bed frame. Do make sure the brackets are on the most outer position of the frame like shown below and that they are flat with the frame. Do not attach the printer bed to the frame yet.
<br>
<br>

![Bed Frame](/assets/images/manual/vz235/z_assembly/bed_frame.png)
<br>

### Step 2

Attach all rod holders finger tight (upper & lower) to the frame, don’t worry about the position just yet. You want to be able to shift them around. Then insert the rods into the bearings and attach the bed frame with the rods to the respective rod holders.

### Step 3

With the assembly in place attach the two alignment tools like shown below and tighten
<br>
<br>

![Alignment](/assets/images/manual/vz235/z_assembly/alignment.png)
<br>

### Step 4

Once you aligned the front corners you are going to put the bed in the lowest position and wiggle the bed around. Try to get the rod pretty nice and vertical to the frame and tighten the rear bottom rod holders and tighten them to the frame.

### Step 5

Now put the bed in the highest position and tighten the clamps for the upper rods and tighten the brackets to the frame. To keep the bed up you can use zip ties or ask someone to help.

### Step 6

Insert the bearings in the leadscrew brackets (press fit) and attach the brackets like shown below. Don’t forget to put the belt around the pulley before assembling the top part of the bracket.
<br>
<br>

![Leadscrew](/assets/images/manual/vz235/z_assembly/leadscrew.png)
<br>

Then attach the leadscrew support with the oldham couplers and leadscrew nut to the bed frame and assemble the parts loosely.
<br>
<br>

![Leadscrew attach](/assets/images/manual/vz235/z_assembly/leadscrew_attach.png)
<br>

### Step 7

To align the parts, measure the bracket is nicely in between the rod holders measure the distance and get it approximately centered. Turn the leadscrew a bit to help it self-align the upper leadscrew support on the bed and tighten the parts. The leadscrew should be nice and vertical. To check you can put the bed in the highest position and measure the distances between the leadscrew and z rod. The leadscrew should now be centered between both z rods.

### Step 8

Attach the single motor mount like shown below
<br>
<br>

![Single motor](/assets/images/manual/vz235/z_assembly/single_motor.png)
<br>

The top M3 screws are 30mm and lock the sliding mechanism in place. They also serve as reinforcement of the mount. Also attach the motor pulley and belt on the motor.

### Step 9

To synchronize the leadscrews, turn out the grub screws on the 40t pulleys and get the bed in the top position. Then retighten the grubscrews

### Step 10

Assemble the z switch and make sure when the bed rises the switch is triggered by the screw to avoid a bed crash at the first homing sequence.
<br>
<br>

![Endstop](/assets/images/manual/vz235/z_assembly/endstop.png)
<br>

### Step 11

Finally install the bed M3 supports, attach the bed with the countersunk M3’s and bed springs. If you are using a milled aluminum bed refer to the electronics/wiring section on how to properly assemble the silicone heater pad.