# DIY Robotic ARM

## Introduction
The goal of this mini-project is to modify the open source
[PyBot Robotic Arm](https://www.jjrobots.com/scara-robotic-arm-by-jjrobots/) from [JJRobots](https://www.jjrobots.com/)
by replacing their [custom electronic board](https://www.jjrobots.com/product/devia-robotics-control-board-v1-0/) by
combining multiple boards available on the market.

## Links to the original project
Documentation:
* [Original project home page](https://www.jjrobots.com/scara-robotic-arm-by-jjrobots/)
* [Assembly guide](https://www.jjrobots.com/scara-robotic-arm-assembly-guide/)
* [Gripper assembly guide](https://www.jjrobots.com/robotic-arm-gripper-2-degrees-of-freedom/)
* [Details about electronics](https://www.jjrobots.com/robotic-arm-electronics-how-to-control-the-robotic-arm/)
* [Shop where to buy a kit](https://www.jjrobots.com/product/pybot-robotic-arm/)
* [Original electronic board (not used in this project)](https://www.jjrobots.com/product/devia-robotics-control-board-v1-0/)
* [Schematics of the original electronic board](https://www.jjrobots.com/wp-content/uploads/2019/09/DEVIA-board-SCHEMATIC.pdf)

Downloads:
* [STL files for the 3D printed parts](https://www.jjrobots.com/wp-content/uploads/2019/09/pyBot-3D-parts-models-.stl-file-format.zip)
* [Arduino code](https://www.jjrobots.com/wp-content/uploads/2019/10/PyBotArm_v1.zip)
* [Python code](https://www.jjrobots.com/wp-content/uploads/2020/02/PyBot-PYTHON-CODE-V32.zip)

> Note: [this page](https://www.jjrobots.com/pybot-control-app-code-arduino-code/) contains the instructions to download
> and install the applications.

## Alternative electronic board
The following parts are assembled in order to replace the original electronic board:
* An [OCROBOT ALPHA D21G18A](http://www.ocrobot.com/doku.php?id=ocrobot:alpha:d21g18a:main): a board providing an
  ARM Cortex M0 microcontroller (
  [schematics](http://www.ocrobot.com/lib/exe/fetch.php?media=ocrobot:alpha:d21g18a:alpha_d21g18a_r1.pdf)).
* A [RAMPS 1.6](https://github.com/bigtreetech/ramps-1.6) board (
  [schematics](https://github.com/bigtreetech/ramps-1.6/blob/master/Ramps1.6/hardware/R6Schematic%20diagram.pdf) and
  [connectors schematics](https://reprap.org/wiki/File:RAMPS1-6connectors.jpg)).
* 3x [A4988 stepper motor drivers](https://www.pololu.com/file/0J450/A4988.pdf).
* A [D1 Mini ESP8266 wifi module](https://wiki.wemos.cc/products:d1:d1_mini) (
  [AT commands datasheet](https://cdn.sparkfun.com/datasheets/Wireless/WiFi/Command%20Doc.pdf)).
* A [GY-53 VL53L0X LIDAR](http://wiki.sunfounder.cc/index.php?title=GY-53_VL53L0X_Laser_ToF_Flight_Time_Range_Sensor_Module_Serial_PWM_Output).
* A voltage conversion board 12V to 5V to 3.3V [BENQ CA-1253](https://www.aliexpress.com/item/32790146418.html).

In order to assemble all these boards, I have designed [this PCB with EasyEDA](https://easyeda.com/marcpl/pybot-alt-board).

## External links
* [Tutorial about how to control a stepper motor with an Arduino and an A4988 driver](https://howtomechatronics.com/tutorials/arduino/how-to-control-stepper-motor-with-a4988-driver-and-arduino/)
* [Tutorials about LEDs](https://learn.edwinrobotics.com/tutorial-how-to-breadboard-led/) and
  [sample](https://datasheet.lcsc.com/szlcsc/1810231815_Everlight-Elec-333-2SURD-S530-A3-L_C99758.pdf)
  [datasheets](https://datasheet.lcsc.com/szlcsc/1809211715_Everlight-Elec-333-2SYGD-S530-E2-L_C99697.pdf) for LEDs.