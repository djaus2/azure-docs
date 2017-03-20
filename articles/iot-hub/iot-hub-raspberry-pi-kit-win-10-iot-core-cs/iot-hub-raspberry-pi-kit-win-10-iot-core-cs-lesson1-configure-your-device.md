---
title: 'Connect Raspberry Pi (C) to Azure IoT - Lesson 1: Configure device | Microsoft Docs'
description: Configure Raspberry Pi 3 for first-time use and install the Windows 10 IoT-Core OS, a free operating system that is optimized for the Raspberry Pi hardware.
services: iot-hub
documentationcenter: ''
author: shizn
manager: timtl
tags: ''
keywords: 'install Windows 10 IoT-Core, Windows 10 IoT-Core download, how to install Windows 10 IoT-Core, Windows 10 IoT-Core setup, raspberry pi install Windows 10 IoT-Core, raspberry pi install os, raspberry pi sd card install, raspberry pi connect, connect to raspberry pi, raspberry pi connectivity'

ms.assetid: 8ee9b23c-93f7-43ff-8ea1-e7761eb87a6f
ms.service: iot-hub
ms.devlang: c
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/28/2016
ms.author: xshi

---
# Configure your device
## What you will do
Configure Pi for first-time use and install the Windows 10 IoT-Core operating system. Windows 10 IoT-Core is free to download. If you have any problems, look for solutions on the [troubleshooting page](iot-hub-raspberry-pi-kit-win-10-iot-core-cs-troubleshooting.md).
## What you will learn
In this article, you will learn:

* How to install Windows 10 IoT-Core on Pi.
* How to power up Pi by using a USB cable.
* How to connect Pi to the network by using an Ethernet cable or wireless network.
* How to add an LED to the breadboard and connect it to Pi.

## What you need
To complete this operation, you need the following parts from your Raspberry Pi 3 Starter Kit:

* The Raspberry Pi 3 board
* The 16-GB microSD card
* The 5-volt 2-amp power supply with the 6-foot micro USB cable
* The breadboard
* Connector wires
* A 560-ohm resistor
* A diffused 10-mm LED
* The Ethernet cable

![Things in your Starter Kit](media/iot-hub-raspberry-pi-lessons/lesson1/starter_kit.jpg)

You also need:

* A wired or wireless connection for Pi to connect to.
* A USB-SD adapter or mini-SD card to burn the OS image onto the microSD card.
* A computer running Windows, Mac, or Linux. The computer is used to install Windows 10 IoT-Core on the microSD card.
* An Internet connection to download the necessary tools and software.

## Install Windows 10 IoT-Core on the MicroSD card
Prepare the microSD card for installation of the Windows 10 IoT-Core image using **IoTDashboard**: [Take this link](IoTDashboard.md)

Insert the card:

![Insert the SD card](media/iot-hub-raspberry-pi-lessons/lesson1/insert_sdcard.jpg)

## Turn on Pi
Turn on Pi by using the micro USB cable and the power supply.

![Turn on](media/iot-hub-raspberry-pi-lessons/lesson1/micro_usb_power_on.jpg)

> [!NOTE]
> It is important to use the power supply in the kit that is at least 2A to make sure that your Raspberry has enough power to work correctly.

## Enable SSH
As of the November 2016 release, Windows 10 IoT-Core has the SSH server disabled by default. You need to enable it manually. You can refer to the [official instructions](https://www.raspberrypi.org/documentation/remote-access/ssh/) or connect a monitor and go to **Preferences -> Raspberry Pi Configuration** to enable SSH.

## Connect Raspberry Pi 3 to the network
You can connect Pi to a wired network or to a wireless network. Make sure that Pi is connected to the same network as your computer. For example, you can connect Pi to the same switch that your computer is connected to.

### Connect to a wired network
Use the Ethernet cable to connect Pi to your wired network. The two LEDs on Pi turn on if the connection is established.

![Connect by using an Ethernet cable](media/iot-hub-raspberry-pi-lessons/lesson1/connect_ethernet.jpg)

### Connect to a wireless network
Follow the [instructions](https://www.raspberrypi.org/learning/software-guide/wifi/) from the Raspberry Pi Foundation to connect Pi to your wireless network. These instructions require you to first connect a monitor and a keyboard to Pi.

## Connect the LED to Pi
To complete this task, use the [breadboard](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard), the connector wires, the LED, and the resistor. Connect them to the [general-purpose input/output](https://www.raspberrypi.org/documentation/usage/gpio/) (GPIO) ports of Pi.

![Breadboard, LED, and Resistor](media/iot-hub-raspberry-pi-lessons/lesson1/breadboard_led_resistor.jpg)

1. Connect the shorter leg of the LED to **GPIO GND (Pin 6)**.
2. Connect the longer leg of the LED to one leg of the resistor.
3. Connect the other leg of the resistor to **GPIO 0 (Pin 11)**.

Note that the LED polarity is important. This polarity setting is commonly known as Active Low.

![Pinout](media/iot-hub-raspberry-pi-lessons/lesson1/pinout_breadboard.png)

Congratulations! You've successfully configured Pi.

## Summary
In this article, you’ve learned how to configure Pi by installing Windows 10 IoT-Core, connecting Pi to a network, and connecting an LED to Pi. Note that the LED doesn't yet light up. The next task is to install the necessary tools and software in preparation for running a sample application on Pi.

![Hardware is ready](media/iot-hub-raspberry-pi-lessons/lesson1/hardware_ready.jpg)

## Next steps
[Get the tools](iot-hub-raspberry-pi-kit-win-10-iot-core-cs-lesson1-get-the-tools-win32.md)

