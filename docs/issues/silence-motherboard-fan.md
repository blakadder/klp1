---
comments: true
title: Part Cooling Fan Speed
description: Enable Variable Speed on Part Cooling Fan
---

The motherboard fan is not properly configured out of the box.

You can replace its section in `printer.cfg` to make it quieter:

```cfg
[temperature_fan Pi_fan2] 
#Temperature controlled fan for the main board
pin: PA2
kick_start_time: 0.500
sensor_type: temperature_host
control: pid
pid_kp: 10
pid_ki: 0
pid_kd: 0
# Temperature which it will try to target
target_temp: 60.0
# Absolute limits for temperature
min_temp: 0
max_temp: 90
# Adjust the interval for the fan speed to the range 0%-100%
max_speed: 1.0
min_speed: 0.0
```