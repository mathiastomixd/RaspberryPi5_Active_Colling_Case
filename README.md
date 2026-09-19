# RaspberryPi5_Active_Colling_Case
An active colling case for your RaspberryPi5 with EDATEC Heatsink and Noctua Fan.

<img src="./Pictures/Side 1.jpg" width="1000">

## You need!
1. NF-A4x10 5V PWM: https://www.noctua.at/en/products/nf-a4x10-5v-pwm
2. ED_Pi5Case_O: https://edatec.cn/ac/ED_Pi5Case_O
3. M4 Screws: https://www.amazon.de/dp/B0B3CSQW4Y or you can 3D print one
4. JST SH 4-pin (Also known under Qwiic Connector) -> To any other Cable, we will solder it later
5. 3D printer or you can order it by a print company
6. Soldering iron for cables of the fan
7. Isolating tape or shrink tubes
#### Total Costs: 30€ - 50€

## Programm the temperatur freshholds and speeds of the fan:
1. Go into the config.txt file on your Raspberry Pi5: sudo nano /boot/firmware/config.txt
2. Go to the bottom of the file and paste the code I provide under "[all]": Code -> Extention
3. Save the file and close it: Strg + O, Enter and Strg + X
4. Reboot the Pi and wait until you can log in again: sudo reboot
<br>

## Settings for Cura Slicer
1. You should change your settings to your specific printer and material, <br>
but in fact there are some settings you need, especially for the supports. <br>
2. The 3D models are printed with the groove facing to the bottom, <br>
in general you doesn't need to change the ordination. <br>
<img src="./Pictures/Cura Side View.png" width="600">

### Support
Change everthing in **Support** to standard and add the settings below.<br>
**Support Structure** -> **Normal** <br>
**Support Placement** -> **Everywhere** <br>
**Support Overhang Angle** -> **55.0°** <br>
**Support Pattern** -> **Zig Zag** <br>
**Support Density** -> **10%** <br>
**Minimum Support Area** -> **40mm** -> Provides supports in large areas without the supports in the hexagons.

### Other settings you can copy if you want
**Quality** Layer Height <= 0.2mm <br>
**Walls** -> ZSeam Position should be placed <br>
**Infill** Infill Density >= 10% <br>
**Infill** Infill Pattern -> Lines <br>
**Build Plate Adhesion** -> Brim <br>
**Brim Width** -> 8mm <br>

## Connect the fan wires to the Raspberry Pi 5
To connect the fan wires we use the already existing jst header that is located on the board. <br>
1. Cut the wire of the fan to 7 cm
2. Strip the big insulation 2cm and from that the small insulation of the 4 wires to 1cm
3. Strip the wire of the JST-SH connector to 5cm and from that the small insulation of the 4 wires to 1cm
<br>
Noctura Fan Pinout<br>
<img src="./Pictures/Noctura-Pinout.jpg" width="300">
<img src="./Pictures/Raspberry JST SH Fan Pinout.jpg" width="300">
<br>
<br>
<br>
## Things I need to update in the future
#### ~~Explain the settings for 3D print espacially for the supports~~
#### How to solder the fan wires and JST SH Connector correct together
#### How to mount everthing together in a few simple steps
#### Tests on how effective is this really
