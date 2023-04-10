---
layout: default
title: 6.3 Firmware Setup
parent: 6. Electronics
grand_parent: VzBoT235 - Printed Version
has_toc: false
nav_order: 2
has_children: false
permalink: /vz235_printed/electronics/Firmware
---

# 6.3 Firmware Setup

Time to start flashing our Pi and Motherboard.

# Flashing the Pi.
Take your Pi's SDCard and put it in your PC/laptop. Now we're gonna use the program called Raspberry Pi Imager to flash the firmware for it onto our SDCard. You can get it here [Raspberry Pi Imager](https://www.raspberrypi.com/software/)

Once downloaded start the software You'll be greated by this wonder full screen.

![Mainpage](../../assets/images/manual/vz235_printed/electronics/firmware/Main%20page.PNG)

First we're gonna choose the correct OS. So press Choose OS and scroll down till you see Other specific-purpose OS like shown below.

![Specific_OS](../../assets/images/manual/vz235_printed/electronics/firmware/Specific%20OS.PNG)

Next select 3D Printing

![3dPrinting](../../assets/images/manual/vz235_printed/electronics/firmware/3DPrinting.PNG)

And Select Mainsail OS. and choose the 32Bit version.

![Mainsail](../../assets/images/manual/vz235_printed/electronics/firmware/Mainsail.PNG)

Now we've done that Press Choose Storage and select your SDCard from the list.

![Specific_OS](../../assets/images/manual/vz235_printed/electronics/firmware/Specific%20OS.PNG)

Next up press the Gear on the right bottom once everything is selected.

![Settings](../../assets/images/manual/vz235_printed/electronics/firmware/Settings.PNG)

And scroll down to the Wifi setup bit. Check the Configure wireless LAN box and put your wifi name in the SSID part and your wifi's Password in the Password: line. Next up select your country from the list and press Save.

![Wifi](../../assets/images/manual/vz235_printed/electronics/firmware/Wifi%20setup.PNG)

Now you've done that Press the big button saying Write and it's time to wait a bit. This can take some time. sometimes upto 15/20min. Just wait for it to say you can remove your SDCard once it's done and it's now time to plug it into your Pi and power it on.

![Specific_OS](../../assets/images/manual/vz235_printed/electronics/firmware/Writing.PNG)

# Installing Klipper.

Once you've booted up your Pi find the IP adress of it with your Router. This IP will be user specific so we can't help much there.

Once you have the IP it's time to start Putty from this website. [Putty](https://www.putty.org/)

If you've downloaded it start it up and you'll be greeted with this screen. Put your printes IP adress in the Host Name section and make sure port is set to 22 and SSH is checked. if you wanna save your printers settings enter a name in the Saved sessions box and press Save. Now press Open and you'll be greeted with a message just press yes there.

![Putty](../../assets/images/manual/vz235_printed/electronics/firmware/Putty.PNG)

Next up you'll be greeted with the Login screen. The username is default: pi and Password is default: raspberry. Once entered you'll be greeted with this screen.

![Login](../../assets/images/manual/vz235_printed/electronics/firmware/login.PNG)

First we're gonna be updating the Pi with some commands. You'll be asked to enter your password sometimes and that's the same as we used to login so: raspberry. 

Enter these 2 commands in the order shown bellow and wait for everything to finish.

``` sudo apt-get update``` 

``` sudo apt-get upgrade```

Now that we have a updated Pi it's time to setup the firmware for our Motherboard.

```cd ~/klipper/```

```make menuconfig```

You'll be greeted with this beautifull screen.

![menuconfig](../../assets/images/manual/vz235_printed/electronics/firmware/menuconfig.PNG)

First off we're gonna press the space bar on Enable Extra low-Level configuration options so we can see a bit more options.

You can navigate the screen with the arrow keys on your keyboard and Spacebar selects the option.

You'll see something like this now.

![low level](../../assets/images/manual/vz235_printed/electronics/firmware/extra_low_level.PNG)

Go down to Micro-controller Architecture and press the spacebar. you'll see a list of options for selecting the correct architecture. We're gonna be using the STM32. Press space to select it.

![stm32](../../assets/images/manual/vz235_printed/electronics/firmware/STM32.PNG)

Now go down to Processor Model and press space there. We're gonna be selecting the correct MCU we have on our Motherboard.

For the Mellow Super 8 V1.3 we need the STM32F407. And we next Select the Bootloader offset to be 32KiB Bootloader.

It should look like this.

![stm32](../../assets/images/manual/vz235_printed/electronics/firmware/F407Setup.PNG)

For the Mellow Super 8 Pro we need to use the STM32H743 with a 128KiB bootloader Offset. Like this.

![stm32](../../assets/images/manual/vz235_printed/electronics/firmware/H743.PNG)

Now you simply Press: Q and hit Y for Yes save configuration.

![stm32](../../assets/images/manual/vz235_printed/electronics/firmware/save.PNG)

Once that is done you simply type this command in putty and it will make the firmware file for you.

```make```

Once it's done with compiling the firmware you'll see something like this telling you the file is ready and where it is located.

![stm32](../../assets/images/manual/vz235_printed/electronics/firmware/firmwaredone.PNG)

# Putting the firmware on the Motherboard.

Now we're gonna use are next bit of software called WinSCP from this site [WinSCP](https://winscp.net/eng/download.php).

Once downloaded start it up and you'll see a screen like this.