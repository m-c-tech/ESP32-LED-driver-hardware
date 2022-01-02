# ESP32-LED-driver-hardware
A board to drive RGBW and addressable LEDs using a NodeMCU-32S ESP32 WiFi microcontroller development board.

PCB design done in KICAD 6.0  
Mechanical enclosure design done in Autodesk Fusion 360  

Enclosure:
Designed for 3D printing.
(L)56.6mm * (W)56.6mm * (D)26mm
The enclosure needs a M3 heated nut-sert to be put in the lid and a countersunk M3 machine screw.

Power:
Input voltage can be 5V to 12V up to 5A current.  
Input connector is a 2.1mm ID, 5.5mm OD, 9.5mm depth barrel jack plug.

Pinout used for common anode RGBW 5/12V LEDs:  
VDD  - Power +ve
IO19 - White  
IO18 - Red  
IO17 - Green  
IO16 - Blue  

Hardware changes for driving addressable LEDs:  
Remove 0R resistors from R1-R4  
Place 0R resistors on R5-R7  
Bridge JP1-JP3  

Pinout used for WS281x addressable LEDs:  
VDD  - Power +ve (ensure your power supply is correct for your LED voltage)
IO19 - LED data 1  
IO18 - LED data 2  
IO17 - LED data 3  
IO16 - Ground  

Pinout used for APA102 addressable LEDs:  
VDD  - Power +ve (ensure your power supply is correct for your LED voltage)
IO19 - LED data  
IO18 - LED clock  
IO17 - Unused  
IO16 - Ground  

![PCB0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/PCB0.jpg)
![Enclosure0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure0.PNG)
![Enclosure1](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure1.PNG)