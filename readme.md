# Motorcycle Navigation Embedded System

## 

##### **OVERVIEW**



A navigation-assist device meant for motorcyclists that simplifies GPS instructions into minimal visual cues to reduce distractions while driving.

System receives simplified command and outputs:

* Directional signals (Right, left, straight)
* RGB Status feedback for turn urgency and rerouting.
* Simple instruction text on LCD display.



This system is being built using an **STM32 Nucleo-F446RE** microcontroller and a protoboard, 2 white LEDS, 1 RGB LED, and 330 ohm resistors.



##### Completed:



Basic GPIO functionality:

Built and tested GPIO helper functions for direction LEDs and RGB status output.

Implemented `HandleCommands()` to parse 3-part navigation commands:

`DIRECTION,DISTANCE,DISPLAY\_TEXT`

Verified command handling using hard-coded test commands.



UART Integration:

Added UART receive support from PC to STM32.

Command buffering implemented so characters are stored until Enter is pressed. 

Confirmed commands can be sent through PuTTY and processed by 'HandleCommands()'.

Verified LEDS update based on UART commands.

