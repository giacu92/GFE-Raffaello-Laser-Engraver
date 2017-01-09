# GFE-Raffaello-Laser-Engraver
This repo contains all the files of my Arduino Nano based Laser Engraver firmware for Arduino.

* Author: Giacomo Mammarella
* email: giacomo.mammarella@student.univaq.it

# File list:
* [grbl09j_GFE.hex](https://github.com/giacu92/GFE-Raffaello-Laser-Engraver/blob/master/grbl09j_GFE.hex): is the hex file precompiled for my Arduino Nano controller Board.
* [Laser engraver V2.sch](https://github.com/giacu92/GFE-Raffaello-Laser-Engraver/blob/master/Laser%20engraver%20V2.sch): the Cadsoft Eagle 6.5 schematic file for the board.
* [Laser engraver V2.brd](https://github.com/giacu92/GFE-Raffaello-Laser-Engraver/blob/master/Laser%20engraver%20V2.brd): the Cadsoft Eagle 6.5 board file.
* Nano grbl.png: useful as connections reference guide.

# .hex file characteristics: grbl09j_GFE.hex 
* Changed defaults for the GFE Raffaello Laser Engraver to match motor and machine parameters.
* Changed homing cycle: $H now ignores the z-axis and perform homing cycle for 2 axis machines.
* Mapped PWM Spindle control (pin: D11) on the range from 0 (1/255, Laser still ON!) to 12.000 (DC). The value 12.000 was chosen to match bCNC parameter for spindle max speed. 

# Realize the board, BOM:
To realize the board you'll need the following parts. And the links to buy 'em:
* [Arduino Nano Compatible board](http://www.banggood.com/ATmega328P-Arduino-Compatible-Nano-V3-Improved-Version-With-USB-Cable-p-933647.html) from Banggood.com
* [Mini DC-DC Converter](http://www.banggood.com/Mini-DC-DC-Converter-Step-Down-Module-Adjustable-Power-Supply-p-920327.html) from Banggood.com
* 2 x [A4988 Stepper Driver](http://www.banggood.com/5Pcs-3D-Printer-A4988-Reprap-Stepper-Motor-Driver-Module-p-952527.html) i got mine from Banggood.com too, bought in pack of 5 for about $8,00.
* 2 x [3 poles DIP Switches](http://www.aliexpress.com/item/DIP-switch-3-way-2-54mm-DIP-Switches-3P/939142709.html) from Aliexpress.com
* 1 x [2.1mm DC Jack Female Plug Connector](http://www.aliexpress.com/item/DC-Power-adapter-dc-jack-connector-DC005-5-5-X-2-1-mm-50-pcs-lot/32352870494.html?spm=2114.01020208.3.19.BoIzX5&ws_ab_test=searchweb201556_3,searchweb201644_2_10001_10002_10005_10006_10003_10004_62,searchweb201560_6,searchweb1451318400_6149), but I got mine from a local Hardware Store
* 2 x 100uF/25V Electrolitic Capacitor from Hardware Store
* 3mm red led, 1N4001 diode and a 4,7k resistor for the led.

# Connections:
![Arduino Nano](https://github.com/giacu92/GFE-Raffaello-Laser-Engraver/blob/master/Nano%20grbl.png)
![Board](http://i65.tinypic.com/30ws0wm.png)
