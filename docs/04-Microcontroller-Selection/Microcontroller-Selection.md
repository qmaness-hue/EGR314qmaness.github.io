---
title: Module's Selected Microcontroller
---

## Intro

The following section contains information regarding the selected microcontroller necessary for the motor system that will turn the EV Scope so as to properly track celestial/distant objects.

**Role and Responsibilities**

The role of this subsystem of the EV Scope is to accurately recieve instruction from the human interface and camera (in some cases), and then interpret that information and make movements to accomplish the given need. The motor needs to accurately move in the manner that the user wishes--meaning that the motor both has to accurately interpret data from the camera and data from the human interface, and subsequently make precise movement to accomplish the task.

**MPLAB Pin Configuration**
![](PDIP40.png)

The selected motor driver is compatible with the selected DIP-PIC18F47Q10 microcontroller. In the figure above, you can see all allocations needed for SPI communications between the driver and the DIP. There are pins allocated for UART for ease of interaction, as well as GPIO pins for LEDs for debugging.

**Pinout for IFX9201SGAUMA1**
![](IFX9201SGAUMA1pinout.png)
| **Pin**                                                                                                                                                                                      | **Pin Function**                                                                                                                                    | **Connection**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Pin 1 (DIR)   | Defines direction of motor current | PIC GPIO RB4 |
| Pin 2 (VSO) | Supply for SO Output |Voltage Regulator|

| **Pin and Pin Function**                                                                                                                                                                                      | **Connection**                                                                                                                                    | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Pin 1 (DIR)<br>Defines direction of motor current| \* PIC GPIO RB4 |
| Pin 2 (VSO)<br>Supply for SO Output| Voltage Regulator|

The microcontroller I selected for the motor system will be the DIP microcontroller provided in class. Based on my research, the motor driver and gearmotor I plan to use are compatible with the PIC18F47Q10. The motor driver I selected--the MAX6650EUB+T--utilizes the I2C interface. This interface is the one I personally have the most experience with, and therefore suits the DIP well. All parameters appear to match up, as I did the component selection with the DIP given in class in mind.
