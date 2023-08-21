---
title: "What is the dashboard?"
description: "Introduction to Reachy's dashboard."
date: 2023-07-25T16:34:27+02:00
lastmod: 2023-07-25T16:34:27+02:00
draft: false
images: []
type: docs
menu:
  dashboard:
    parent: "introduction"
weight: 100
toc: true
---

We developed Reachy's dashboard to give you an overview of the state of your Reachy (which motors are detected, what services are running, what are the motors temperatures...) as well as giving you the possiblity to access quickly some features (changing a robot's part compliance for example).

This tool has been thought to help you **start easier with the robot** and **facilitate quick debugging**.

What it provides?
* **Easy setup when you just received your Reachy** </br> 
Reachy will emit its own wifi network *Reachy-AP* to which you will be able to connect. From this you can easily connect Reachy to your wifi network and [get started with the robot]. No need to plug a computer screen, keyboard and mouse to the robot.

* **First debug step without having to open a terminal** </br>
If you are not able to connect to Reachy using its Python SDK, it probably means that something went wrong when Reachy's software started. Whether it is because one of Reachy's cable is disconnected or because Reachy's motors has not been turned on, the dashboard will try to tell you what is going on with Reachy without having to type any code.
If the problem is not as simple, you also have access to Reachy's services logs to get more information on the problem your robot is encountering.

* **Easy access to basic information from the robot** </br> 
Monitor motor positions and temperatures, change motors compliance or activate Reachy's fans in one click.

* **Manage network connection** </br> 
Handle wifi network connection, manage Reachy's hotspot to connect to the robot even when there is no Internet available.

* **And much more!** </br> 
Because the dashboard is open source like [Reachy's hardware and software](https://www.pollen-robotics.com/opensource/), you can customize the dashboard and create your own features!

## Access the dashboard

**From the robot:**  
Access the dashboard at `127.0.0.1:3972` from any web browser.

**From any other device (computer, phone, tablet, ...) on the same network as the robot:**  
Access the dashboard at `<robot-ip>:3972` from any web browser.

## Features Overview

The dashboard is composed of five pages:
* [**Debug**]: indicates if a cable was disconnected or if Reachy's motors were off when Reachy booted,
* [**Dashboard**]: displays the present position and temperature of each joint, allows you to control Reachy's fans and the joints compliance,
* [**Services**]: lets you check which services are running in your robot. You can restart, stop each service and access their logs easily,
* [**Wifi**]: lets you manage Reachy's wireless connection. You can connect your robot to a new wifi network or control its hotspot.
* [**Applications**]: lets you manage Reachy's autonomous applications. Just with Reachy's services, you start, stop and access the logs for each application that you installed. For now, only the [Hello world] and [Face tracking] applications are available.

On each page, the configuration of the robot will also be displayed (e.g. whether your robot is a full kit, starter kit, ...)

More information is available for each page in the [content section].
