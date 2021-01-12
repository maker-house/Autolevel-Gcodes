# Autolevel-Gcodes
Autolevel Gcodes for adjusting Z probe offset and starting autolevel procedure, you need a 3D/Bltouch or any automatic probe.

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
1. Use G29.gcode to start autolevel procedure, it will automatically finish and save the points
2. Add "M420 S1; Load autolevel points" to your start gcode in your slicer, after the G28 line it should be something like: 
``` 
G28 ; Home all
M420 S1; Load autolevel points
``` 

# Español
# Autolevel-Gcodes
Códigos G de nivelacion automática para ajustar el desfase Z de la sondae iniciar el procedimiento de nivel automático, necesita un 3D / Bltouch o cualquier sonda automática.

## Uso

## Pre
1. Compruebe que la sonda esté correctamente cableada y que no presente errores
2. Precaliente la cama y el hot end a la temperatura de impresión, asegúrese de que la boquilla y la cama estén limpias

## Ajuste de desfase en Z de sonda
0. Hacer home

1. Utilice un papel para calibrar el desfase z, avance manualmente hacia la pocision Z0 hasta que el papel se frene, si llega a Z0 pero la boquilla está demasiado lejos, reduzca el desplazamiento Z, si el papel está demasiado apretado, aumente el desplazamiento z
2. Si no cuenta con home Z  en el menú, use el código G28 Z0.gcode (asi no necesita hacer home en todos los ejes, X e Y)
3. Repita 1-3 hasta que el papel se deslice entre la cama y la boquilla con poca dificultad.


## Nivelacion automática
Después de ajustar el desplazamiento Z
1. Use G29.gcode para iniciar el procedimiento de autonivelación, finalizará automáticamente y guardará los puntos
2. Agregue "M420 S1; Cargar puntos de nivel automático" a su gcode de inicio en su cortadora, después de la línea G28 debería ser algo como:
``` 
G28 ; Home all
M420 S1; Load autolevel points
``` 
