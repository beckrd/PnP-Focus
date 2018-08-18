# PnP-Focus
Simplest Arduino-based focus controller

I want to share with you the Arduino-based focus controller named "PnP Focus". As the name implies, I want it to be as easy as "Plug and Play". No soldering. No hassle with firmware upload.
You simply 1) buy the readily available components, 2) stack them, and 3) upload the firmware by a single click. 

***************
Added by RDBeck
My PG27 motor has significant backlash and the code as proviced by aruangra does not provide for backlash compensation.
This fork adds backlash compensation which assumes inward focusing to keep the gears engaged.  The backlash parameter can 
be set by changing the value at line 92 (long Backlash = 24;  //change this line for different backlash).
*************** 
 
Features:
- Manual control
- LCD display
- Temperature sensor
- compatible with Moonlite ASCOM driver
- compatible with commercially available focuser motors.

I have tested with various motors from
- Robofocus
- Moonlite
- USB_Focus

All of them use the DB9 male connectors. It also works with the popular DIY stepper motors:
- 28BYJ-48  (5V and 12V)
- 17HS13-0404S-PG27 (12V)
 
Components required:
1) Arduino Leonardo board. ($5-$10)
2) Ardumoto L298P motor driver board ($9). Choose the board that use Pin 3, 11, 12, 13 for driving the motor.
3) 1602 LCD and keypad shield ($2-$10). I recommend the 1602 LCD and keypad shield by DFRobot ($10).
4) DS18B20 Temperature Sensor. I recommend the sensor by DFRobot ($4). The sensor is connected as shown in the figure below.
 
The total cost is less than $30.
 
Installation:
1) Visit https://github.com/aruangra/PnP-Focus , download the files and open in the Arduino IDE (downloadable from https://www.arduino.cc/en/Main/Software) or use the web IDE at the same location.
2) Then connect the micro usb cable between Arduino Leonardo and your PC.
3) Go to the Sketch/Upload menu item. The firmware will be uploaded to the Arduino board, and it is ready for use. 
 
How to use:
- You can use the ASCOM Moonlite focuser driver to control the motor.
- For manual control, the keys are as follows:
LEFTMOST:  Save the position to EEPROM. For manual control, the position is not saved. Use this key to save the position. 
LEFT: Move in
RIGHT: Move out
UP: Backlight On/Off
DOWN: Fast/Slow movement
 
Let me know if you have any question. Thank you.

Anat / RD Beck
