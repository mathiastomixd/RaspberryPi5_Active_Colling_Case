# RaspberryPi5_Active_Cooling_Case
An active cooling case for your RaspberryPi5 with EDATEC Heatsink and Noctua Fan.

<img src="./Pictures/Camera/Side 1.jpg" width="800">

## You need!
1. NF-A4x10 5V PWM: https://www.noctua.at/en/products/nf-a4x10-5v-pwm
2. ED_Pi5Case_O: https://edatec.cn/ac/ED_Pi5Case_O
3. M4 Screws: https://www.amazon.de/dp/B0B3CSQW4Y or you can 3D print one
4. JST SH 4-pin (Also known under Qwiic Connector) -> To any other Cable, we will solder it later
5. 3D printer or you can order it by a print company
6. Soldering iron for cables of the fan
7. Isolating tape or shrink tubes
#### Total Costs: 30€ - 50€

## Settings for 3D print
1. You should change your settings to your specific printer and material, <br>
but in fact there are some settings you need, especially for the supports. <br>
2. The 3D models are printed with the groove facing to the bottom, <br>
in general you doesn't need to change the orientation. <br>
<table>
  <tr>
    <td><img src="./Pictures/3D model and printed/Cura Side View.jpg" width=425></td>
    <td><img src="./Pictures/3D model and printed/3D printed case.jpg" width=425></td>
  </tr>
</table>

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
<br>
## Connect the fan wires to the Raspberry Pi 5
To connect the fan wires we use the already existing jst header that is located on the board. <br>
Depending on the color of your cabels on your **JST SH** adapter you need to solder it together.<br>
<br>
Solder the wires according to the diagram provided below:<br>
<table>
  <tr>
    <td><img src="./Pictures/Diagramme/NocturaPinout.jpg" width="425"></td>
    <td><img src="./Pictures/Diagramme/Raspberry JST SH Fan Pinout.jfif" width="425"></td>
  </tr>
</table>

## Guide for correct cabel connection
1. Cut the wire of the fan to 7 cm
2. Strip the big insulation 2cm and from that the small insulation of the 4 wires to 1cm
3. Strip the wire of the JST-SH connector to 5cm and from that the small insulation of the 4 wires to 1cm
4. Twist and solder the wires like shown in the pictures
5. Insulate the cabels with the technic I show in the pictures
<table>
  <tr>
    <td><img src="./Pictures/Cabel soldering and insulation/Twist.jpg" width=425></td>
    <td><img src="./Pictures/Cabel soldering and insulation/Solder.jpg" width=425></td>
  </tr>
</table>
<table>
  <tr>
    <td><img src="./Pictures/Cabel soldering and insulation/Insulation 1.jpg" width=200></td>
    <td><img src="./Pictures/Cabel soldering and insulation/Insulation 2.jpg" width=200></td>
    <td><img src="./Pictures/Cabel soldering and insulation/Insulation 3.jpg" width=200></td>
    <td><img src="./Pictures/Cabel soldering and insulation/Insulation 4.jpg" width=200></td>
  </tr>
</table>
<br>

## Programm the temperatur freshholds and speeds of the fan:
1. The raspberry pi should already have a running OS and we programm via the powershell
2. Go into the config.txt file on your Raspberry Pi5: sudo nano /boot/firmware/config.txt
3. Go to the bottom of the file and paste the code I provide under "[all]": Code -> Extention
4. Save the file and close it: Strg + O, Enter and Strg + X
5. Reboot the Pi and wait until you can log in again: sudo reboot
<br>

## Things I need to update in the future
#### ~~Explain the settings for 3D print espacially for the supports~~
#### ~~How to solder the fan wires and JST SH Connector correct together~~
#### How to mount everthing together in a few simple steps
#### ~~How to programm the fan settings on the pi via powershell~~
#### Tests on how effective is this really
