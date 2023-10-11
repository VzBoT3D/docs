---
layout: default
title: Bug in /dev/serial/by-id
parent: Troubleshooting
grand-parent: General info
slug: udev-bug
---

# Bug in /dev/serial/by-id

{: .note-title}
> Source
>
> [Original message](https://discord.com/channels/460117602945990666/460172848565190667/1102656480223690783) by @shiftingtech on the VORONDesign Discord server.  
> It has been edited here for the purpose of editoral clarification.

A bug has been introduced in the `udev` software package (part of the `systemd` package) present in Debian Bullseye (which includes Armbian and current MainsailOS) which prevents the symbolic links to serial devices in `/dev/serial/by-id/` from being created.

As of May 20th 2023, this bug has spread to PiOS based systems as well.

This bug may cause the following **issues**:

1. Your printer can't connect to the motherboard's microcontroller (MCU) anymore after a system update

    ![Klipper MCU can't connect](images/klipper_mcu-connect-error.png)

2. `ls /dev/serial/by-id` shows no devices or warns you the file does not exist

    ```bash
    $ ls /dev/serial/by-id
    ls: cannot access '/dev/serial/by-id': No such file or directory
    ```

## Am I affected?

Before asserting whether you are affected by this bug, assess whether your motherboard is being recognized and shows up as a device.

1. Connect your motherboard to the Pi using a suitable USB cable.
2. Run `lsusb` and observe the output for any devices containing "OpenMoko, Inc."

    ```bash
    $ lsusb
    Bus 001 Device 001 1234:ABCD OpenMoko, Inc.
    ```

❎ If your motherboard **does not** show up as such, it may be the case that:
{: .text-red-200}

- Your motherboard isn't connected to the Pi  
    *Have you tried plugging it in?*
- The Klipper firmware on your motherboard was flashed improperly  
    *Follow the correct instructions for flashing your board with firmware.*
- The Klipper firmware on your motherboard failed to flash  
    *Check the SD-card for evidence of the flashing process succeeding.*
- The Klipper firmware on your motherboard was not built for the right device  
    *Make sure you have selected the right options for your motherboard under `make menuconfig`*
- The USB cable connecting your motherboard to the Pi is defective  
    *Try a different USB cable.*
- Your motherboard is having other issues

✅ If your motherboard **does** show up as such, then proceed as follows:
{: .text-green-000}

Check whether you are affected by this bug by checking the version of the installed udev package by running `apt show udev` in the terminal.

The following versions are known to be affected:

- 247.3-7+deb11**u2**
- 247.3-7+rpi1+deb11**u2**

Please note the last section of the version string, including **u2**.

## Solution A

Replacing the corrupted file from the `udev` package with that from a version that is not affected.

1. Back up the existing file (in case you need it)  
    `sudo cp /usr/lib/udev/rules.d/60-serial.rules /usr/lib/udev/rules.d/60-serial.old`
2. Download the patched file from the systemd repository  
    `sudo wget -O /usr/lib/udev/rules.d/60-serial.rules https://raw.githubusercontent.com/systemd/systemd/main/rules.d/60-serial.rules`
3. Reboot the machine/Pi  
    `sudo reboot`

## Solution B

Installing a patched version of the software package from the Debian "Backports" software repositories.

{: .warning-title}
> Raspberry Pi OS (& Raspbian)
>
> Do not attempt Solution B on machines/Pi's running PiOS-based systems (previously named Rasbian)!  
> If you are unsure of what your operating system type is, stick to [Solution A](#solution-a).

To install the patched version of the systemd package (version 252.5-2~bpo11+1):

1. Copy and paste the following command as one line.  
    Use the "Copy" icon top-right of the code block to help you with this.

    ```bash
    cd ~;wget http://ftp.us.debian.org/debian/pool/main/s/systemd/libudev1_252.5-2~bpo11+1_`dpkg --print-architecture`.deb http://ftp.us.debian.org/debian/pool/main/s/systemd/udev_252.5-2~bpo11+1_`dpkg --print-architecture`.deb;APT_LISTCHANGES_FRONTEND=none sudo apt install --fix-broken ./libudev1_252.5-2~bpo11+1_`dpkg --print-architecture`.deb ./udev_252.5-2~bpo11+1_`dpkg --print-architecture`.deb; rm libudev1_252.5-2~bpo11+1_`dpkg --print-architecture`.deb udev_252.5-2~bpo11+1_`dpkg --print-architecture`.deb
    ```

    If all goes right, this command should be prompting or attempting to install only the two affected packages (udev and libudev).

    {: .danger}
    > If the command tries to install other packages or behaves unexpectedly (in particular, wanting to remove a large quantity of installed packages), stop the command using `CTRL`+`C` and *reassess the situation*.

2. Reboot  
    `sudo reboot`

You should now be able to see your device in `/dev/serial/by-id` and/or connect to your device in Klipper once again.
