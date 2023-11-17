---
comments: true
title: Missing macros
description: Add missing load/unload macros to Kingroon KLP1
---

KLP1 v2.1 came with missing LOAD and UNLOAD filament macros. Add these to your `printer.cfg` or its own file 

```cfg
[gcode_macro LOAD_FILAMENT]
gcode:
    M104 S220
    M105    
    M109 S220
    G91 
    G1 E100 F300
    G90

[gcode_macro UNLOAD_FILAMENT]
gcode:
    M104 S220
    M105    
    M109 S220
    G91
    G1 E30 F3000
    G1 E-27 F9000
    M106 S255
    M104 S62
    M105    
    M109 S62
    G1 E-50 F300
    M106 S0
    M84
```