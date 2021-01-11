# Autolevel-Gcodes
Autolevel Gcodes for adjusting Z probe offset and starting autolevel procedure

## Usage

## Pre
1. Check probe is correctly wired and not in error
2. Preheat bed and hot end to printing temperature, ensure nozzle and bed are clean

## Probe offset Z adjust
0. Home all 

1. Use a paper to calibrate z offset, move close to Z0, if it reaches Z0 but nozzle is too far, decrease Z offset, if paper is too tight increase z offset
2. If no individual Z home in menu, use G28 Z0.gcode (so no need to re-home X and Y axes) 
3. Repeat 1-3 until paper slides between bed and nozzle with little difficult


## Autolevel
After adjusting Z offset
1. Use G28 Z0.gcode to start autolevel procedure, it will automatically finish and save the points
2. Add "M420 S1; Load autolevel points" to your start gcode in your slicer, after the G28 line it should be something like: 
``` 
G28 ; Home all
M420 S1; Load autolevel points
``` 
