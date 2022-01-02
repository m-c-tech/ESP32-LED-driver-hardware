# ESP32-LED-driver-hardware
A board to drive RGBW and addressable LEDs using a NodeMCU-32S ESP32 WiFi microcontroller development board.

PCB design has been done in KICAD 6.0  
Mechanical enclosure design done in Autodesk Fusion 360  
The enclosure needs a heated nut-sert to be put in the lid, this is sized for M3 hardware.

The power input can take 5V to 12V up to 5A.

Pins used for driving LEDs:  
IO19 - White/SPI_Clock/Addressable  
IO18 - Red/SPI_Data/Addressable  
IO17 - Green/Addressable  
IO16 - Blue/Addressable  

For driving addressable LEDs:  
Remove 0R resistors from R1-R4  
Place 0R resistors on R5-R7  
Bridge JP1-JP3  

![PCB0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/PCB0.jpg)
![Enclosure0](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure0.PNG)
![Enclosure1](https://github.com/m-c-tech/ESP32-LED-driver-hardware/blob/main/Images/Enclosure1.PNG)