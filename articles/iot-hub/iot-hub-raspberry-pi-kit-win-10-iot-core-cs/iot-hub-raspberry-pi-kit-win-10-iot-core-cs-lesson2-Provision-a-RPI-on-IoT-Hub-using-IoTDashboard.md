---
title: 'Connect Raspberry Pi (C) to Azure IoT - Lesson 2: Azure tools (Windows) | Microsoft Docs'
description: Install Python and the Azure command-line interface (Azure CLI) on Windows 7 and later versions.
services: iot-hub
documentationcenter: ''
author: djaus
manager: na
tags: ''
keywords: 'iot cloud service, azure cli'

ms.assetid: a3c083b5-0d76-46af-bc77-2ad7d8aadc1e
ms.service: iot-hub
ms.devlang: C#
ms.topic: article
ms.tgt_pltfrm: rpi
ms.workload: na
ms.date: 03/28/2016
ms.author: djaus

---
# Provision a Raspberry PI on IoT Hub using IoTDashboard
> [!div class="op_single_selector"]
> * [Windows 7 and later](iot-hub-raspberry-pi-kit-win-10-iot-core-cs-lesson2-get-azure-tools-win32.md)

## About
There are many ways to skin a cat. We will take the easy way; use IOT Dashboard
You could go to the Azure Portal, after regregistering, and directly create your IoT Hub, as well as register a new device on it. If you want to do this see:
* [Create an IoT Hub on the Portal](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal) Just down to *"Change the settings of the IoT hub"*. The Linux RPI C version on which these labs are based uses Python and CLI

See options [here](http://pumpingco.de/different-ways-to-register-devices-to-the-azure-iot-hub/)


## What you will do
Provision a RPI runnning IoT-Core on Azure IoT Hub using IoTDashbaord

## What you will learn
In this article, you will learn:
* Create an IoT Hub
* Setup TPM on the RPI
* Provision a RPI running IoT-Core

## What you need
* A Windows computer with an Internet connection.
* An active Azure subscription. If you don't have an Azure account, create a [free Azure trial account](http://azure.microsoft.com/pricing/free-trial/) in just a few minutes.
* IoTDashboard as per Lesson 1
* Booted RPI with Windows 10 IoT-Core as per Lesson 1

## Create (Free) account on Azure
* Start IoTDashboard
* Click on Connect to Azure
* Sign in if you already have an account OR
    * Click on I don't have an accont ..
    * "Follow the bouncing ball .. (Start Free Option)"
    * Sign in in IoTDashboard when created

## Provison your RPI
* "Provision your device" will show once logged into Azure, on IoTDashboard
* Action "Create a new IoT Hub" if you haven't already or select your existing on.  Note you can only have one free IoT Hub.
* Action "Create a new Device" if you haven't already or select yoru existing one. Note you can only have one Device with the free IoT Hub.
* Select your device to provision
* If TPM is already setup on your device, a check will be done. If all is OK, it checks a few thinsgs, action the provisioning.
* Probably at thhis stage though  it will prompt you with respect to TPM (see red box):

![IoTDashboard TPM](media/IoTDashboard/TPM.png)

* Select Software TPM (No Security). TPM is implemented in hardware, that the RPI doesn't have, so w emulate it.
    * See [Is IoT Security an Oxymoron](http://embedded101.com/Blogs/David-Jones/entryid/780/is-iot-security-an-oxymoron)
*  Once rebooted, action the Provisioning

## Examine TPM on RPI
* In IoTDshboard, select your device from My Devices, right-click on it and Open Device ManaPortalger
* Click on TPM Configuration.


![Device Portal TPM](media/IoTDashboard/TPM-device-portal.png)


## Summary
You've installed the Azure CLI. Your next task to create your Azure IoT hub and device identity by using the Azure CLI.

## Next steps
[Create your IoT hub and register Raspberry Pi 3](iot-hub-raspberry-pi-kit-win-10-iot-core-cs-lesson2-prepare-azure-iot-hub.md)

