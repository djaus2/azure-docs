---
title: 'Connect Raspberry Pi (C) to Azure IoT - Lesson 1: Configure device | Microsoft Docs'
description: Configure Raspberry Pi 3 for first-time use and install the Windows 10 IoT-Core OS, a free operating system that is optimized for the Raspberry Pi hardware.
services: iot-hub
documentationcenter: ''
author: djaus
manager: na
tags: ''
keywords: 'install Windows 10 IoT-Core, Windows 10 IoT-Core download, how to install Windows 10 IoT-Core, Windows 10 IoT-Core setup, raspberry pi install Windows 10 IoT-Core, raspberry pi install os, raspberry pi sd card install, raspberry pi connect, connect to raspberry pi, raspberry pi connectivity'

ms.assetid: 8ee9b23c-93f7-43ff-8ea1-e7761eb87a6f
ms.service: iot-hub
ms.devlang: C#
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/28/2016
ms.author: djaus done

---
# Configure your device
## What you will do
Add an LED to the breadboard and connect it to Pi

## What you will learn
In this article, you will learn:

* How to add an LED to the breadboard and connect it to Pi.

## What you need
To complete this operation, you need the following parts from your Raspberry Pi 3 Starter Kit:

* The Raspberry Pi 3 board as setup previously
* The breadboard
* Connector wires
* A 560-ohm resistor
* A diffused 10-mm LED
* The Ethernet cable


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
[Create and deploy the blink application](iot-hub-raspberry-pi-kit-win-10-iot-core-cs-lesson1-deploy-blink-app.md)



