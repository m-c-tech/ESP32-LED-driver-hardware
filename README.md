# ESP32-LED-driver-hardware
A board to drive RGBW and addressable LEDs using a NodeMCU-32S ESP32 WiFi microcontroller development board.

PCB design has been done in KICAD 6.0
Mechanical enclosure design done in Autodesk Fusion 360

The power input can take 5V to 12V up to 5A.

Pins used for driving LEDs:
IO19 - White/SPI_Clock/Addressable
IO18 - Red/SPI_Data/Addressable
IO17 - Green/Addressable
IO16 - Blue/Addressable

For driving addressable LEDs:
Remove 0R resistors from R1-R4 and place them on R5-R7
Bridge JP1-JP3
