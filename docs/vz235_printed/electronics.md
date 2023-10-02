---
layout: default
title: 6. Electronics
parent: Vz235 - Printed Version
has_toc: false
nav_order: 6
has_children: true
permalink: /vz235_printed/electronics
---

# 6. Electronics

## Overview

![Overview](../../assets/images/manual/vz235_printed/electronics/overview.png)

This is a general overview of the parts recommended for a VzBot build. Everyone is free to use their own choice of parts. STL-files for other screens etc are not natively provided and may be found in the community mod section on GitHub and Discord.

We trust everyone to use their own best judgement when wiring their printer, we do not recommend to do this without professional help if you are inexperienced in electronics.

## BOM

| Material         | Quantity | Notes |
| :--------------- | :------- | :---- |
| LED strip 310mm  | 3        |       |
| Mainboard        | 1        |       |
| BTT Pi TFT50     | 1        |       |
| PSU 24V          | 1        |       |
| PSU 48V          | 1        |       |
| Wires            | -        |       |
| C14 power switch | 1        |       |
| Power cord       | 1        |       |

## STL's

| File name                | Amount to print | Notes              |
| ------------------------ | --------------- | ------------------ |
| [LED strip bracket][]    | 3               | print in vase mode |
| [Power switch bracket][] | 1               |                    |
| [Front screen cover][]   | 1               |                    |
| [Rear screen cover][]    | 1               |                    |
| [Screen mount][]         | 1               |                    |
| [Door stopper][]         | 1               |                    |

## Video tutorial

Vz235 Build Part 4: The electronics  
![Vz235 Build Part 4: The electronics](https://www.youtube.com/watch?v=bEGVnYrXJG4&t)

\[...\] *Drilling, cutting and such are not applicable to Mellow kit*

[00:00](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=0s) Intro  
[01:59](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=119s) Layout  
[09:30](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=570s) Design & Print  
[10:11](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=611s) Motherboard mount  
[14:59](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=899s) Stepper motor drivers  
[17:57](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1077s) Install fuses  
[18:46](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1126s) SPI & UART mode  
[19:38](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1178s) Fan port setup  
[21:29](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1289s) Pi USB power  
[22:28](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1348s) Sensorless homing  
[26:53](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1613s) Power supplies  
[29:40](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1780s) DIN rail  
[30:05](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=1780s) CPAP fan prep  
[36:47](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2207s) Mount CPAP fan  
[37:09](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2229s) Cable guides  
<!-- [39:02] Overview of back panel layout -- worth a screenshot -->
[40:11](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2411s) Mount backplate  
[41:05](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2465s) Design intermission  
[45:01](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2701s) CPAP tube routing

[46:19](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2779s) Wiring: overview  
[48:55](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=2779s) Wiring: tools  
[51:54](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3114s) Wiring: Mains / AC  
[54:23](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3263s) Wiring: Bed  
[56:14](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3374s) Wiring: 24v & 48v DC  
[59:21](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3561s) Wiring: Motors  
[01:01:46](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3706s) Wiring: Sensors, fans, endstops, ...  
[01:02:46](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3766s) Endstop switches X, Y, Z

[01:03:35](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3815s) Print head  
[01:04:36](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3876s) Pi peripherals  
[01:05:48](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=3948s) Bottom skirts  
[01:08:00](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4080s) Back panel installed

[01:09:05](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4145s) Wiring: Camera  
[01:12:16](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4336s) Wiring: CPAP PWM wire  
[01:13:04](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4384s) Wiring: LED, Chamber sensor  
[01:14:09](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4449s) Wiring: Pi Screen  
[01:15:45](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4545s) **Wiring: ⚠️ 24v correction**

[01:16:30](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4590s) First turn-on: fixing issues  
[01:18:12](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4692s) Second time's the charm??  
[01:20:04](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4804s) Enclosure panels, RSCS

[01:21:12](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4872s) A/B Motors AWD recap  
[01:22:13](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4933s) Firmware? dreams  
[01:22:37](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4957s) Vez happy man :) 🍻  
[01:23:00](https://www.youtube.com/watch?v=bEGVnYrXJG4&t=4980s) Closing remarks  

[Door stopper]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
[Front screen cover]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
[LED strip bracket]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
[Power switch bracket]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
[Rear screen cover]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
[Screen mount]: https://github.com/VzBoT3D/VzBoT-Vz235/blob/main/Assemblies%20%26%20STL/Frame/Frame%20brace.stl
