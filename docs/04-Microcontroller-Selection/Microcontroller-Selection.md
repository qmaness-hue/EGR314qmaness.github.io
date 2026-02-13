---
title: Module's Selected Microcontroller
---

## Intro

The following section contains information regarding the selected microcontroller necessary for the motor system that will turn the EV Scope so as to properly track celestial/distant objects.

**Role and Responsibilities**

The role of this subsystem of the EV Scope is to accurately recieve instruction from the human interface and camera (in some cases), and then interpret that information and make movements to accomplish the given need. The motor needs to accurately move in the manner that the user wishes--meaning that the motor both has to accurately interpret data from the camera and data from the human interface, and subsequently make precise movement to accomplish the task.

The microcontroller I selected for the motor system will be the DIP microcontroller provided in class. Based on my research, the motor driver and gearmotor I plan to use are compatible with the PIC18F47Q10. The motor driver I selected--the MAX6650EUB+T--utilizes the I2C interface. This interface is the one I personally have the most experience with, and therefore suits the DIP well. All parameters appear to match up, as I did the component selection with the DIP given in class in mind.
