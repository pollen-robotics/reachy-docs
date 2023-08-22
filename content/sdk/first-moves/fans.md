---
title: "Controlling the fans"
description: "How to control the fans inside Reachy's arms and head."
lead: ""
date: 2023-07-25T17:38:42+02:00
lastmod: 2023-07-25T17:38:42+02:00
draft: false
type: docs
images: []
toc: true
---

This section assumes that you went through the [Hello World]({{< ref "sdk/getting-started/hello-world" >}}) so that you know how to connect to the robot.

Reachy is equipped with fans to cooldown the joints when they are working. Each arm has three fans and two fans are in the head.

First, connect to your Reachy.

```python
from reachy_sdk import ReachySDK

reachy = ReachySDK(host='192.168.0.42')  # Replace with the actual IP

reachy.fans
>>> <Holder
	<Fan name="l_shoulder_fan" state="off">
	<Fan name="l_elbow_fan" state="off">
	<Fan name="l_wrist_fan" state="off">
	<Fan name="r_shoulder_fan" state="off">
	<Fan name="r_elbow_fan" state="off">
	<Fan name="r_wrist_fan" state="off">
	<Fan name="l_antenna_fan" state="off">
	<Fan name="r_antenna_fan" state="off">
>
```

As explained in the [safety page]({{< ref "sdk/first-moves/safety#check-the-temperatures" >}}), the temperature of each joint is controlled internally in Reachy and if it reaches a certain value, the corresponding fan turns on. 
However, you might want to turn them on sooner so that the joints work longer on a demanding task.

The *reachy.fans* object contains each fan. You can have access to each fan individually or to all at once.

{{< img-center "images/sdk/first-moves/fans_attributes.png" 400x "" >}}

```python
for fan in reachy.fans.values():
  print(fan)
>>> <Fan name="l_shoulder_fan" state="off">
<Fan name="l_elbow_fan" state="off">
<Fan name="l_wrist_fan" state="off">
<Fan name="r_shoulder_fan" state="off">
<Fan name="r_elbow_fan" state="off">
<Fan name="r_wrist_fan" state="off">
<Fan name="l_antenna_fan" state="off">
<Fan name="r_antenna_fan" state="off">
```
Each *Fan* object has two attributes: 
* *name* string with the fan's name, 
* *is_on* boolean, False when the fan is off and True when it is on.
and two methods:
* *on()* which turns the fan on,
* *off()* which turns the fan off.

{{< img-center "images/sdk/first-moves/single_fan_attribute.png" 400x "" >}}

Thus you can easily turn on a fan.

```python
reachy.fans.r_wrist_fan.on()

reachy.fans.r_wrist_fan.is_on
>>> True

reachy.fans.r_wrist_fan.off()
```
