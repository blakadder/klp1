---
comments: true
title: Part Cooling Fan Speed
description: Enable Variable Speed on Part Cooling Fan
---

You **do not** need to replace the stock part cooling fan to have variable speeds. The solution to this is to edit the `MKS_THR.cfg` file and find the `[fan]` section and edit the stock values to match the below. 

```cfg
[fan]
pin:MKS_THR:gpio1
max_power: 1.0
kick_start_time: 0.5
off_below: 0.01
cycle_time: 0.05
```

This will mean the fan will operate properly and you should be able to change the speeds. I hope this helps!