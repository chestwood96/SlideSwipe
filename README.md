# SlideSwipe 1.0 (magnetic probe for the voron v0.1)
## Introduction
I liked the idea of the [SideSwipe](https://github.com/oldfar-t/Side-Swipe-Magnetic-Probe) probe but didn't like that it would require either printing with the door open or loosing Y travel, so I made my own take on the idea.

Taking probe             |  Stowing probe
:-------------------------:|:-------------------------:
![This is an image](Images/take.gif)  |  ![This is an image](Images/putBack.gif)

## Pros and cons compared to SideSwipe
| Pro | Con |
| ---- | ---- |
| + Fully integrated | - Requires new cowling (and the accompanying rebuild of everything on it) |
| + Cables well hidden | - More complex (more parts, more steps) |
| + No loss in y area with the door closed |  |
| + Bed can't hit the arm |  |
| + Hot-swappable switches (ok, fair that's a bit of a gimmick)

## BOM
### Parts
- 1x MG90s Metal gear servo (the SG90 plastic gear ones work too but are not reccomended)
- 1x Omron(or omron size) mouse switch (I am using a kailh GM4.0 switch, but it's only marginally better than all the other switches I tested)
- 5x 6x3mm round magnets (I used the cheapest crappiest ones I could find of aliexpress, need to be at least 2.7mm thick)
- 1x 300mm servo extender cable (or make your own)
- 1x 1.5m of stranded wire with <1.2mm od (I tested 30awg silicone wire and 26awg ptfe wire)
- 2x JST-XH housing (only one housing and 2 crimping terminals if you don't want to wire to the 5pin probe port on the SKR mini E3 v2)
- 7x JST-XH female crimping terminal
- 1x (optional but reccomended) JST-PH or JST-XH 2pin male and female connector pair
- 3x 16mm piece of 4od2id PTFE tube (does not need to be the nice stuff)
- 1x 7mm piece of 4od2id PTFE tube (does not need to be the nice stuff) 
### Screws
- 7x M3x6 Socket head screw (cap head probably works too, one needs to be at least slightly attracted to magnets)
- 2x M3x8 Cap head screw
- 2x M3 nut
### Tools
- Some superglue
- Tools to crimp JST-XH (and optionally JST-PH)
- A multimeter

## Printing
All parts are designed to print in the orientation they come in and not require supports (If you have really bad overhang performance you can add a bit of support for the probe but it should not be necessary).

Designed to print in ABS at 0.4mm outer layer width and 0.2mm layer height.

I recommend ironing for the following parts, the rest can be printed without:
- Arm1
- Arm2
- ProbeCarrierTop
- ProbeCarrierBottom
- RailMountTop

If you are going to do accents, I reccomend printing the following parts in the accent color:
- Arm1
- Arm2
- Probe

## Build
![Parts](Images/Parts.jpg)
### Probe
![ProbeParts](Images/ProbeParts.jpg)

Crimp two short (about 5cm but cutting off is easier than adding...) pieces of wire and put them in the outer-most places in the JST-XH 5pin housings. I recomend testing the cripms at this point.
![ProbeCrimp](Images/ProbeCrimp.jpg)

Thread the wires through the holes, then put the connector in the probe. Make sure it's the right way around. Don't put it in all the way jet.
![ProbeInsert](Images/ProbeInsert.jpg)

Add some superglue to the back of the connector and carefully push it all the way in while making sure the wires are not pinched. Make sure superglues does not get anywhere it shouldn't.
![ProbeWires1](Images/ProbeWires1.jpg)

Shorten the wires, so they stand a little over the edge (5-10mm is fine).
![ProbeWires2](Images/ProbeWires2.jpg)

Strip as much of the wire as you can. You probably can't use normal wire strippers for that.
![ProbeWires3](Images/ProbeWires3.jpg)

Put the stripped wires in the magnet holes. Make sure the not stripped parts are in the grooves, so they don't get in the way.
![ProbeWires4](Images/ProbeWires4.jpg)

Add somesuper glue to the rim of the holes and put the magnets in the holes **with the same polarity facing up**. Make sure the glue does not get on the wires too much and there is none on the top of the magnets. Also, try to get them as parallel with each other as possible (pressing them against a flat surface while drying helps). 

Test continuity between the magnet and the jst pins.
![ProbeMagnets](Images/ProbeMagnets.jpg)

After the glue dried insert the microswitch so the plunger is in the middle of the probe.

With the switch inserted there should be continuity between the magnets unless the switch is pressed.
![ProbeSwitch](Images/ProbeSwitch.jpg)

Screw on M3x6 screw into the hole of the side of the probe. (make sure the screw is at least somewhat attracted to a magnet)
![ProbeScrew](Images/ProbeScrew.jpg)
![ProbeScrew2](Images/ProbeScrew2.jpg)

The screw is not only attracted to magnets in one direction (because of influence from the magnet above it). Install the retention magnet in the probe carrier in the right orientation (using the probe as tool for installing it can help). Then add some glue to the back of the magnet to hold it in place (there is a hole in the part to allow easier gluing and removal of the magnet)
![ProbeCarrier](Images/ProbeCarrier.jpg)
![ProbeCarrier2](Images/ProbeCarrier2.jpg)

The probe should now stick in the carrier and not just fall out.
![ProbeCarrier3](Images/ProbeCarrier3.jpg)

### Cowling
![CowlingParts](Images/CowlingParts.jpg)

In this guide I am putting a connector (jst-ph) on the cowling for easier removal, you can use any other small enough connector or wire it directly (you just need to make the wires long enough to go through the umbilical and to your mainboard plus a little slack, so you can take the cowling of at least somewhat)

Crimp your connector to two short pieces of wire to your connector and feed them through the wire holes in the back of the cowling. Check your crimps.
![CowlingWires](Images/CowlingWires.jpg)

Cut them so about 3-4cm of wire are standing out of both holes, then strip about 2cm of those.
![CowlingWires2](Images/CowlingWires2.jpg)

Pull the wires back until there is only stripped wire in the holes and curl the rest of the wire in the holes.
![CowlingWires3](Images/CowlingWires3.jpg)

Put some superglue on the rims of the holes and push the magnets in the holes **in the right orientation to match the probe**. Try to get those too as parallel to each other as possible by pushing them against a flat surface.

Make sure there is no glue on the top of the magnets and check continuity between the magnets and the wires.

![CowlingMagnets](Images/CowlingMagnets.jpg)

If the magnets were put in the right way the probe should stick to the cowling. Test the continuity between the wires, there should be continuity between the wires unless the switch is pressed or the probe is removed.
![CowlingAndProbe](Images/CowlingAndProbe.jpg)

### Probe holder
Find the servo arm that fits the arm the best and cut off anything else on that arm if there is anything.
![ArmServoArm](Images/ArmServoArm.jpg)
![ArmServoArm2](Images/ArmServoArm2.jpg)

Zero the servo (and check that it has at least over 90° of travel and isn't a continuously rotating one) and install the chosen arm, so it points a little over 90° when at the max point (picture is the max point).
![ArmServoArm3](Images/ArmServoArm3.jpg)

Pull the servo wire through the hole.
![ArmServoMount](Images/ArmServoMount.jpg)

Insert the servo into the mount and fix it using 2 M3x6 screws
![ArmServoMount2](Images/ArmServoMount2.jpg)
![ArmServoMount3](Images/ArmServoMount3.jpg)
![ArmServoMount4](Images/ArmServoMount4.jpg)

Insert the short piece of PTFE in the left hole of "RailMountTop".
![ArmServoMount5](Images/ArmServoMount5.jpg)

Insert one of the longer pieces of ptfe into one of the holes of "Arm2"(the solid one).
![Arm1](Images/Arm1.jpg)

Put "Arm2" and "Arm1" onto the servo carrier like shown.
![Arm2](Images/Arm2.jpg)

Screw "RailMountTop" onto the servo carrier using 2 M3x6 screws.
![Arm3](Images/Arm3.jpg)

Put the other two longer pieces of ptfe into the remaining two holes in the arms.
![Arm4](Images/Arm4.jpg)

Put "ProbeCarrierTop" and "ProbeCarrierBottom" on the arms and screw them down using 2 M3x6 screws.
![Arm5](Images/Arm5.jpg)
![Arm6](Images/Arm6.jpg)

Add nuts in the pockets on the inside of the mount.
![ArmNuts](Images/ArmNuts.jpg)

That should be the physical build done.
![Arm7](Images/Arm7.jpg)

## Installation
### Installing the new cowling
The installation is the same as with the regular one, refer to the manual for that.

### Installing the probe arm
put the servo wire into the groove of the extrusion and tip the mount into it. Fix the assembly using the screws on the side.

Adjust the height to where it can grab the probe, but the arm does not hit the printhead then fix it in place.

Rout the servo wire through the slot in the front extrusion upwards into the slot of the top extrusion. The stock wire should be just long enough to pass through the panel though you'll probably have to remove the connector housing for that.

## Wiring
In this example I am hooking up to the "BL-Touch" connector of the SKR mini e3 v2.0

If you are fancy you can crimp that onto a 5 pin jst-xh plug, otherwise you can just plug it straight into the header.

Here a crude diagram of how this could be wired up. If you wired it differently, you'll need to pay special attention during the klipper setup.
![Wiring](Images/Wiring.JPG)

## Klipper setup

Put this in your klipper config. (If your wired it differently, adjust the pins for the probe and the servo)
```
[homing_override]
axes: z
gcode:
    SET_KINEMATIC_POSITION Z=0
    G1 Z5
    G28 X Y
    Query_Probe
    SS_CONDITIONAL_TAKE_PROBE
    G1 X40 Y110
    G28 Z
    G91
    G1 Z1
    G90

[probe]
pin: ^PC14
x_offset: 20
y_offset: 0
z_offset: 10
speed: 20.0
samples: 2
sample_retract_dist: 5.0
lift_speed: 30.0
samples_tolerance: 0.01
samples_tolerance_retries: 15
deactivate_on_each_sample: 0

[bed_mesh]
speed: 200
horizontal_move_z: 25
mesh_min: 25,25
mesh_max: 95, 95
probe_count: 3,3
algorithm: bicubic

[servo probeServo]
pin: PA1
minimum_pulse_width: 0.000544

[gcode_macro SS_PICKUP_POS]
variable_x: 115
variable_y: 50
variable_z: 30
gcode:
  M118 pickup pos X:{printer["gcode_macro SS_PICKUP_POS"].x} Y:{printer["gcode_macro SS_PICKUP_POS"].y} Z:{printer["gcode_macro SS_PICKUP_POS"].z}

[gcode_macro SS_DEPLOY]
gcode:
    SET_SERVO SERVO=probeServo ANGLE=160
    G4 P500 # wait for deploy
    #SET_SERVO SERVO=probeServo WIDTH=0 # OFF
    
[gcode_macro SS_RETRACT]
gcode:
    SET_SERVO SERVO=probeServo ANGLE=20
    G4 P500 # wait for retract
    SET_SERVO SERVO=probeServo WIDTH=0 # OFF

[gcode_macro SS_TAKE_PROBE]
gcode:
    G1 Z{printer["gcode_macro SS_PICKUP_POS"].z} F5000
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x - 20} Y{printer["gcode_macro SS_PICKUP_POS"].y} F5000
    SS_DEPLOY
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x}
    G1 Y{printer["gcode_macro SS_PICKUP_POS"].y + 50}
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x - 20}
    SS_RETRACT

[gcode_macro SS_STOW_PROBE]
gcode:
    G1 Z{printer["gcode_macro SS_PICKUP_POS"].z} F5000
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x - 20} Y{printer["gcode_macro SS_PICKUP_POS"].y + 50} F5000
    SS_DEPLOY
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x}
    G1 Y{printer["gcode_macro SS_PICKUP_POS"].y} F2000
    G1 X{printer["gcode_macro SS_PICKUP_POS"].x - 20} F5000
    SS_RETRACT

[gcode_macro SS_CONDITIONAL_TAKE_PROBE]
gcode:
    {% set P = printer.probe.last_query %}
    {% if P %}
        SS_TAKE_PROBE
    {% endif %}

[gcode_macro SS_CONDITIONAL_STOW_PROBE]
gcode:
    {% set P = printer.probe.last_query %}
    {% if not P %}
        SS_STOW_PROBE
    {% endif %}

[gcode_macro G29]
gcode:
    G91
    G1 Z1
    G90
    Query_Probe
    SS_CONDITIONAL_TAKE_PROBE
    BED_MESH_CALIBRATE
    SS_STOW_PROBE

[force_move]
enable_force_move: True
```

and replace your z endstop with the probe:
```
endstop_pin: probe:z_virtual_endstop
```

Also add the following to your print start (either in klipper or in your slicer) to make sure it won't try to print with the probe attached (the query_probe first is important):
```
    Query_Probe
    SS_CONDITIONAL_STOW_PROBE
```

After the calibration you should be able to use the G29 macro to mesh level your bed.

### Calibrating the servo angles
Using the servo command, find good values where the servo reliably hit the deployed and stowed position. The mechanism mechanically limits the travel but having the servo trying to push against it the whole time isn't great for it, so try to find some values that don't go way over the limits.

Once you have found the right values, update the "SS_DEPLOY" and "SS_RETRACT" macros with your new values.

### Calibrating the pickup position
This should already be somewhat acurate but if it isn't find the pickup position and update the "SS_PICKUP_POS" macro accordingly.

## First tests
### Check the probe and config
Let's see if klipper can see the probe, the "QUERY_PROBE" command is our friend here:
With the probe attached (by hand for now) it should return "open", with the button pressed it should return "triggered" and with the probe removed it should also return "triggered". If this is not true for your setup don't proceed and go check your wiring and config.

If theat worked out put the probe in the probe carrier and let's do a test run. The homing override uses the probe so all we'll have to do to see if it works is run G28.

It should now home x and y and then pick up the probe and probe for Z, be ready to cut power if something weird happens.

To make sure everything has settled, I like to do a couple hundred probes before I do stuff like calibrating the Z-offset.

```
PROBE_ACCURACY samples=100
```

## Calibrate Z-Offset and start printing
Use your favourite method of calibrating the z-offet and start printing.