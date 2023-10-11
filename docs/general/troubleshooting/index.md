---
layout: default
title: Troubleshooting
parent: General info # temporarily here to clean up the sidebar links
---

# Troubleshooting

Troubleshoot common problems with your printer

## Printer homes in the wrong corner

Ensure your stepper motors are set up to rotate in the correct direction.  
[\[Stepper\] - Configuration reference](https://www.klipper3d.org/Config_Reference.html#stepper) (Klipper docs)

Ensure the endstop positions for all axes are set correctly.  
See `position_endstop:` under your `[stepper]` configuration section.

## Prints are mirrored

You most likely have your motors set up wrong or mirrored. Make sure the physical motors match their counterpart configuration in your `printer.cfg` configuration file.

[Verify stepper motors - Configuration checks](https://www.klipper3d.org/Config_checks.html#verify-stepper-motors) (Klipper docs)

## Printer won't home

Are the endstops connected? The stock VzBot uses mechanical endstops for homing.

Klipper Docs have more information on checking endstop status and/or configuring sensorless homing

* [Verify endstops - Configuration checks](https://www.klipper3d.org/Config_checks.html#verify-endstops) (Klipper docs)
* [Sensorless homing - TMC drivers](https://www.klipper3d.org/TMC_Drivers.html?h=sensorless#sensorless-homing) (Klipper docs)

## Printer is losing position

This can sometimes be caused by lost steps due to excessive speed, acceleration or both.  
Ensure your printer is not set up to use StealthChop. SpreadCycle is preferred, as it has better accuracy and less likelihood of losing steps.

* [Tuning motor current - TMC drivers](https://www.klipper3d.org/TMC_Drivers.html?h=sensorless#tuning-motor-current) (Klipper docs)
* [Setting "spreadCycle" vs "stealthChop" Mode - TMC drivers](https://www.klipper3d.org/TMC_Drivers.html?h=sensorless#setting-spreadcycle-vs-stealthchop-mode) (Klipper docs)

[**Next:** Maintenance &rarr;](./maintenance){: .btn .btn-doc}
