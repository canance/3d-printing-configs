Source: https://www.youtube.com/watch?v=awsI9bMndJA&list=PLU2kePyB_WAZlCnA-fMbLDbGeFXTffiP9

Use the M280 cmd to find the correct angle for extended and retracted auto level servo arm.  Pick a spot on the bed and put the extruder tip within an index card height away from the bed.  Use G92 to set this as 0, 0, 0.  Then extend the auto level arm and put the endstop (engaged) on the same point.  Use M114 to get the X, Y, and Z coordinates.  Put them in configuration.h as the offset from the extruder.  Besure to flip the sign of each value.

M401 - extract

M402 - retract

M280 P0 S[angle] - set servo P0 to an angle

G92 X0 Y0 Z0 - 0 all axis

M119 - get endstop status

M114 - current x, y, and z