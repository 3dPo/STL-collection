                   .:                     :,                                          
,:::::::: ::`      :::                   :::                                          
,:::::::: ::`      :::                   :::                                          
.,,:::,,, ::`.:,   ... .. .:,     .:. ..`... ..`   ..   .:,    .. ::  .::,     .:,`   
   ,::    :::::::  ::, :::::::  `:::::::.,:: :::  ::: .::::::  ::::: ::::::  .::::::  
   ,::    :::::::: ::, :::::::: ::::::::.,:: :::  ::: :::,:::, ::::: ::::::, :::::::: 
   ,::    :::  ::: ::, :::  :::`::.  :::.,::  ::,`::`:::   ::: :::  `::,`   :::   ::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  :::::: ::::::::: ::`   :::::: ::::::::: 
   ,::    ::.  ::: ::, ::`  :::.::    ::.,::  .::::: ::::::::: ::`    ::::::::::::::: 
   ,::    ::.  ::: ::, ::`  ::: ::: `:::.,::   ::::  :::`  ,,, ::`  .::  :::.::.  ,,, 
   ,::    ::.  ::: ::, ::`  ::: ::::::::.,::   ::::   :::::::` ::`   ::::::: :::::::. 
   ,::    ::.  ::: ::, ::`  :::  :::::::`,::    ::.    :::::`  ::`   ::::::   :::::.  
                                ::,  ,::                               ``             
                                ::::::::                                              
                                 ::::::                                               
                                  `,,`


http://www.thingiverse.com/thing:2065461
Prusa i3 MK2 Upgrade kit for E3D Titan Extruder by S±E by Spoegler-Engineering is licensed under the Creative Commons - Attribution - Share Alike license.
http://creativecommons.org/licenses/by-sa/3.0/

# Summary

Update 07.04.2019
Fan shroud for Noctua 40mm hotend. This enables upgrade to MK2.5.
Shroud looks funny due to constraints given by existing design. Installed and working fine.
Remark 09.01.2018
Use a heat sock for the heater block to avoid thermal runaway when using a fan (https://e3d-online.com/v6-socks-pro-pack-of-3)
Update 11.05.2017
updated the assembly instruction
Update 25.04.2017
Extruder mount v1.1 with slightly enlarged hole for beeing able to adjust gear play
All parts in STEP (*.stp) format provided in download section (downlaod as *.rar)
Update 12.03.2017
fan mount V1.2 - Increased air flow throughput
fan mount V1.2x - for bigger fan GB1205PKV1-8AY

Enjoy the advantages of E3D Titan geared extruder with your Prusa i3 MK2
- Increase force on filament by factor 3 to brute force every material without clogging
- Print with tiny 0.15mm nozzle for outstanding detail quality
- For more see http://e3d-online.com/Titan-Extruder

Download - Print - Assemble - Update Firmware (optional) - Print better!

We love to see this thing getting a lot of interest! Thanks, we have fun :)
Feel free to place further comments, ideas and proposals for improvement.
This version is installed on our Prusa i3 MK2. It fits and works absolutely flawless.

You'll need:
- Prusa i3 MK2
- E3D Titan Geared Extruder
- THIS
- cable ties, M3 nuts and hex-socket screws M3x40, x20, x16, x12
- 1-2 beers (optional)

Optional nozzle fan mount for axial fan 40x40mm for better visibility of nozzle included.

Find attached:
- STL files
- brief assembly instruction
- G-codes (ABS h0.25) - radial fan mount V1.0. Newer v1.2 not included
- Firmware

Contact
spoegler.engineering@gmail.com

BTC donations accepted
1Q5BGKPuR6X8ukKLjqMniW3nbSwm14uQaf

ETH donations accepted
0x8262f4CC4372473eb7B1bF686403152E83D15347

# How I Designed This

## Concept

- Easiest / most direct way to upgrade to E3D Titan
- As few modifications as necessary
   - Firmware
   - Usage of original
      - E3D v6 nozzle + silicone sock
      - E-motor
      - PINDA sensor
      - Hotend fan
      - Nozzle fan
      - Bearings / bearings fixation (cable ties)
      - Belt fixation
   - Usage of standard parts
      - E3D cooling fan shroud (the blue injection molded)
         - Can also be printed (it’s included)
         - Metric screws and nuts M3
   - Keep original positions X Y Z
      - Nozzle
      - PINDA sensor
   - As less restriction of x-axis travelling distance as possible : 240mm instead of 250mm
      - More possible when omitting filament tightening knob and using allen key screw instead
- Printability
   - All parts printable with Prusa i3 mk2
   - No support material required
   - All parts with 1 print (fill build plate)
   - As less material as necessary
- Easy assembly
   - Fast change of hotend/nozzle
   - As few fixation points as necessary
   - proper cable management
- Quality
   - Robust design
- Flexibility
   - Usage of axial nozzle fan possible


# Custom Section

## Current available versions

Extruder mount - V1.0
X-carriage - V1.0
> Radial fan mount - V1.1 (improved printability)
> Radial fan mount - V1.2 Increased air flow throughput
> Radial fan mount - V1.2x for bigger fan GB1205PKV1-8AY
Axial fan mount - V1.0
Tightening knob - V1.0
Indicator - V1.0

All downloads will be updated to the newest versions.

# Custom Section

## Firmware

>> please check comment section as some encountered issues with the provided firmware <<

Thanks devilhunter84 for pointing out (comment section):
"You also don't need to change a thing in the firmware, you can use Prusa's Stock firmware (yay for updates)
Just do these little workarounds instead of using a custom firmware:
•	reverse the polarity of the stepper motor, meaning plug it into the mini Rambo in reverse. This causes the extruder to go into the right direction.
use the gcode in your Slic3r settings
M907 X640 Z830 E800 ; set Titan Extruder Current
to give the Titan stepper more juice. the extruder with that big wheel now consumes more mAh, so give it a couple of mAh's more to avoid skipped steps. (just don't do silent/high power from the menu anymore or the extruder will skip again)
M92 X100.00 Y100.00 Z400.00 E837 ; set Titan E steps
this will use the correct stepping if you also got the 0.9 degree motor like me with the Titan. (for 1.8 stepping use your 418.5)"

----------

Firmware update:
Use exact Arduino version 1.6.10 to update firmware!
Direct download link:
https://www.arduino.cc/download_handler.php?f=/arduino-1.6.10-windows.zip
Firmware modifications based on Version 3.0.9:
- Steps per unit extruder 161.3 --> 418.5 (gear ratio)
- Direction of extruder : INVERT_E0_DIR true --> INVERT_E0_DIR false (gear)
- Unload filament speed F7000 --> F3000 (motor speed) - not realy necessary, but works better for my MK2
- Renamed all "fpos_t" to "fpost" to avoid errors when compiling see http://forums.reprap.org/read.php?146,691608,724250#msg-724250)