---
title: "Hardware to display Reachy's IP address"
description: "How is Reachy's IP address displayed in the robot."
date: 2023-08-21T16:09:17+02:00
lastmod: 2023-08-21T16:09:17+02:00
draft: false
type: docs
images: []
toc: true
weight: 310
---

> Please note that the LCD display screen should be installed in the back of the torso of your Reachy. You will need to take off Reachy's tee shirt to see it.

{{< img-center "images/dashboard/installation/ip_lcd_display_reachy.jpg" 400x "Reachy's IP address display" >}}

## Hardware

To display Reachy's IP address, four components are needed:
* [LCD display](https://www.amazon.fr/AZDelivery-pouces-Arduino-Raspberry-microcontrôleur/dp/B01L9GC470/ref=sr_1_3?dchild=1&keywords=Adafruit%2Bgrayscale&qid=1626104484&sr=8-3&th=1)
* [Arduino Nano Every](https://docs.arduino.cc/hardware/nano-every)
* cables to solder between the LCD and the Arduino
* a micro USB cable to connect the Arduino to Reachy's NUC.

## Flashing the Arduino

The code for the Arduino can be found [here](https://github.com/pollen-robotics/reachy-dashboard/blob/main/arduino/serial_communication.ino). Basically, it just listens to messages containing the IP address coming from Reachy's NUC on the serial bus, recovers the IP and displays it on the LCD screen.

The [Arduino IDE](https://docs.arduino.cc/software/ide-v2) will be needed to flash the Arduino.

## Wiring
* GND pin of the LCD display goes with GND pin of the Arduino
* VCC pin of the LCD display goes with 5V pin of the Arduino
* SCL pin of the LCD display goes with A5 pin of the Arduino
* SDA pin of the LCD display goes with A4 pin of the Arduino
