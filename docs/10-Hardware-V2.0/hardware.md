---
title: Hardware V2.0
---

## Overview
If a "Hardware Version 2.0" were to be created with the experience I now have, these would be the changes implemented.

## Changes

### Voltage Regulator
Although the voltage regulator functioned and delivered a regulated voltage, it could have been done much better. 
* The **diode footprint** was too small for the necessary diode, and had extremely small and therefore fragile pads. Choosing a better fooprint would be the most optimal solution.
* The **inductor** I placed on the voltage regulator has the incorrect rating, leading to it regulating to +3.3V instead of the necessary +5V.
* The **jumper cables** could have been placed so that one can remove/add the +9V from/to the circuit.

### Ribbon Cables
The footprint for the ribbon cables is mirrored, therefore making them function incorrectly when connected to other ribbon cables. Ideally I would have made them so that they are arranged correctly and can therefore be used without the use of jumper cables.

### Stepper Motors and Motor Drivers
The stepper motors are rated for 12 volts, but I seemed to have forgotten this when creating the schematic and PCB. I should have made it so that the motor drivers--which have built-in voltage regulation that the user can adjust--regulate their voltage input of +5V (ideally) into the 12 volts necessary for the motors to properly function. Not doing so proved to be a fatal mistake, as the motor drivers couldn't take the 12 volts necessary, leading to the drivers breaking and therefore the whole motor system no longer functioning.

### Microcontroller
The microcontroller functions perfectly, but this only became true after some changes were made to the PCB. The regulated voltage and ground pin required for the PIC to work were never actually connected on the manufactured PCB; this was due to a discrepancy between the numbering on the schematic and PCB files, which led to there never being a trace made between the voltage supply pin of the PIC and the +5V. I later fixed this by manually connecting a wire between the voltage supply and the PIC, as well as between the missing ground pin and the system's ground.
Ideally, I would have never had this issue if I made sure to keep numbering consistent between the PCB and schematic files.
