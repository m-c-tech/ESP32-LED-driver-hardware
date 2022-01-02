# ESP32-LED-driver-hardware
A board to drive WRGB and addressable LEDs using a NodeMCU-32S ESP32 WiFi microcontroller development board.  

The goal for this project was to make an ESPHOME and Home Assistant compatible LED strip controller.  
Price is an important factor as well as ease of use and flexibility in its applications.  
[ESPHome](https://esphome.io/) is a software tool that can generate code for the ESP32 microcontrollers by using configuration files.  
This gives great flexibility with over-the-air updates and easy to understand setup.  
The ESP32 microcontroller is highly flexible with WiFi and bluetooth along with many GPIOs, ADCs, touch sensors, etc.  
Development boards for the ESP32 can be gotten for very cheap from various online sellers, pay close attention to the dev board pinouts as they can vary.  
This PCB design incorporates multiple resistor configurations to allow for differing types of LEDs to be driven, common anode, SPI, one wire.


PCB design done in KICAD 6.0  
Mechanical enclosure design done in Autodesk Fusion 360.  
The bill of materials comes to roughly 20.70AUD per unit at quantaties of 20.  
This includes the ESP32 dev board ($6.75), components from digi-key ($7.80), PCBs from fab house ($2.27), 3D printer plastic ($1.60), plus a few other items.  

Enclosure:  
Designed for 3D printing.  
Dimensions - (L) 56.6mm * (W) 56.6mm * (D) 26mm  
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
Remove 0R resistors from R1-R4.  
Place 0R resistors on R5-R7.  
Bridge JP1-JP3.  

Pinout for up to 3 strings of WS281x addressable LEDs:  
VDD  - Power +ve (ensure your power supply is correct for your LED voltage)  
IO19 - LED data 1  
IO18 - LED data 2  
IO17 - LED data 3  
IO16 - Ground  

Pinout used for 1 string of SPI addressable LEDs:  
VDD  - Power +ve (ensure your power supply is correct for your LED voltage)  
IO19 - LED data  
IO18 - LED clock  
IO17 - Unused  
IO16 - Ground  

![PCB0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/PCB0.jpg)
![Enclosure0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure0.PNG)
![Enclosure1](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure1.PNG)