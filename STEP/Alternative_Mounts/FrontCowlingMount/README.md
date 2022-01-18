# Front Cowling Mount
Thanks to Jlas1 for making this.

The Front cowling mount allows using SlideSwipe without printing and installing a new cowling.

![Action](Images/action.gif)

## Pros and cons compared to integrated mount
| Pro | Con |
| ---- | ---- |
| + No cowling rebuild required | - Probe is further away from the nozzle (can probe less of the bed) |
|  | - Floppier and more fragile |
|  | - Less aesthetically pleasing

## BOM (Differences only)
### Screws
- 2x M3x40 Cap head screw

## Build
The build process is the same as normal, just substitute the cowling with the "FrontCowlingMount"

## Klipper Setup
The klipper setup is also almost the same, however we need a few changes, **do not try probing before this step**

## Pickup position
Move the X of the pickup position 8mm to the left, to do this change this part of the "SS_PICKUP_POS" macro from:
```
[gcode_macro SS_PICKUP_POS]
variable_x: 115
...
```
to:
```
[gcode_macro SS_PICKUP_POS]
variable_x: 107
...
```

## Probe offset
Increase the X-offset of the probe by 8mm (to 28mm):
```
[probe]
pin: ^PC14
x_offset: 28
...
```

## Change Mesh Leveling coordinates
Replace the whole "[bed_mesh]" section with this:
```
[bed_mesh]
speed: 200
horizontal_move_z: 25
mesh_min: 32,32
mesh_max: 88, 88
probe_count: 3,3
algorithm: bicubic
```

# That's it
I still recomend moving to the integrated mount next time you redo the cowling.