---
title: "Finding Reachy's IP"
description: "Find Reachy's IP address to connect to it."
date: 2023-07-25T18:49:56+02:00
lastmod: 2023-07-25T18:49:56+02:00
draft: false
images: []
type: docs
menu:
  SDK:
    parent: "getting-started"
weight: 120
toc: true
---

The last required step before actually programing your Reachy is to find its IP address. 

A small LCD screen should be installed in Reachy's back to display Reachy's IP address. You will need to take down its tee-shirt to see the LCD screen.

{{< img-center "images/sdk/getting-started/ip_lcd_display_reachy.jpg" 400x "" >}}

The instructions to display the IP address to the LCD screen is provided by the [dashboard] which is started at boot with the service [reachy_dashboard.service].

If the LCD screen is not working, check out the page [Find my IP section] to learn other ways to get the IP address.

> Note: Using the SDK locally also avoids network potential latency or bandwidth issue. Yet, it may not be as convenient as working directly from your usual laptop. You need to plug a screen, keyboard and mouse directly on Reachy's computer.

You can check that everything is working as expected by running the following Python code:

```python
from reachy_sdk import ReachySDK

# Replace with the actual IP you've found.
reachy = ReachySDK(host='the.reachy.ip.found.')
```