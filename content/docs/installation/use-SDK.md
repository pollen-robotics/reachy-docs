---
title: "Use Reachy SDK"
description: "Control the robot from any computer using the SDK."
lead: ""
date: 2023-08-09T14:45:28+02:00
lastmod: 2023-08-09T14:45:28+02:00
draft: false
images: []
menu:
  docs:
    parent: "installation"
    identifier: "use-SDK-6b4b45c7d26249a03b10020505ad7574"
weight: 220
toc: true
---

If you want to control Reachy using its **Python SDK**, you only need to install it on the computer you want to use. The SDK is a pure Python library so it can be easily installed on any computer running **Python >= 3.6**.

```python
from reachy_sdk import ReachySDK

reachy = ReachySDK(host='reachy.IP.address')
```

**Ready to start using the Python SDK? Check out the [Python SDK documentation]({{< ref "sdk/getting-started/introduction" >}})!**  

{{< my-button-new-page link="/sdk/getting-started/introduction" label="Getting started with Reachy Python SDK" >}}