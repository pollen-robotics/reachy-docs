---
title: "Disconnected force sensor"
description: "Reconnect the load sensor of the gripper."
date: 2023-07-26T08:47:07+02:00
lastmod: 2023-07-26T08:47:07+02:00
draft: false
images: []
type: docs
toc: true
---

TODO: update

Each arm of Reachy is equipped with a load sensor to measure how much force is applied by the gripper to the object. It allows to know when the gripper is holding an object.

The load sensor is in two part: the sensor itself and an electronic board reading its values and connected to Reachy's internal computer.


{{< img-center "images/help/system/load_sensor_full.jpg" 400x "Load sensor full" >}}

The sensor is placed between the two 3D printed pieces composing Reachy's gripper.

{{< img-center "images/help/system/sensor_in_gripper.jpg" 400x "Load sensor in gripper" >}}

The electronic board is placed between the gripper and wrist_roll motors of the arms.

{{< img-center "images/help/system/load_sensor_schematic.png" 400x "Load sensor schematic" >}}

{{< img-center "images/help/system/load_sensor_views.png" 400x "Load sensor views" >}}

The board is connected to Reachy's computer by a long 8 black wires cable plugged by the back.

When we refer in the documentations as the load sensor being disconnected, we refer to the cable between the board and Reachy's computer as disconnected. It's usually the case, the wires between the sensor and the board are rarely desoldered.

You can check an example of the disconnected cable below.

{{< img-center "images/help/system/load_sensor_disconnected.jpg" 400x "Load sensor disconnected" >}}

Be aware that there is a way for the connector. On the cable there is a short and a long side. 

{{< img-center "images/help/system/module_views.png" 400x "Load sensor module view" >}}

