---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for the motor system that will turn the EV Scope so as to properly track celestial/distant objects.

### Power Management
*Table 1: Voltage Regulator*

**Voltage Regulator**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LM2575.png)<br> LM2575 Regulator<br>$2.16/each<br>[link to product](https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688)                 | \* Inexpensive<br>\* Provided by course<br>\* Can meet surface mount constraint of project<br>\*Simple<br>\* Already have/know how to use | \*Would be awkward to surface mount to a PCB |
| ![](AP7583Q-33FDZW-7.png)<br> AP7583Q-33FDZW-7 Regulator<br>$0.80/each<br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP7583Q-33FDZW-7/17736614)                 | \* Cheap<br>\* Surface Mount<br>\* 3.3V-5V<br>\*Simple                                               | \* Cheap<br>\* Don't already have |

**Rationale:** Seeing as we already have the LM2575, and it appears to be adequate for this project, it's as good a choice as any.

### Actuators

*Table 2: Gearmotor Table*

**Gearmotor**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](FIT0441.png)<br> FIT0441 Gearmotor<br>$19.90/each<br>[link to product](https://www.digikey.com/en/products/detail/dfrobot/FIT0441/6588579)                 | \* Simple [^1]<br>\* Brushless<br>\*Powerful                                                | \* May not have accuracy required<br>\* Incremental |
| ![](SER0070.png)<br> SER0070 Servo Motor <br>$24.88/each<br>[link to product](https://www.mouser.com/ProductDetail/DFRobot/SER0070?qs=6avfeC6zeS5mmJI6Z%252BxOKw%3D%3D)                 | \* Brushless<br>\* Servo Motor <br>\* Accurate and powerful                                               | \* Relatively Expensive<br>\* No datasheet |
| ![](324.png)<br> 324 Stepper Motor <br>$14.00/each<br>[link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/324/5022791)                 | \* Simple <br>\* 200 Steps per revolution (accurate)<br>\* Inexpensive                                               | \* Not super accurate <br>\* Not super powerful |

**Rationale:** The 324 Stepper motor is simple while maintaining high torque and easily optimized accuracy.

*Table 3: Motor Driver Table*

**Motor Driver**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TC647BEOATR.png)<br> TC647BEOATR Surface Mount Driver<br>$1.64/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC647BEOATR/562490)                 | \* Brushless<br>\* Meets surface mount constraint of project <br>\* Inexpensive                                               | \* Made specifically for fans<br>\* Needs parallel interface. |
| ![](MAX6650EUB+T.png)<br> MAX6650EUB+T Surface Mount Driver<br>$8.82/each<br>[link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/MAX6650EUB-T/1521889)                 | \* Brushless<br>\* Can cover multiple parallel motors <br>\* Uses I2C Interface                                               | \* Relatively Expensive<br>\* Utilizes tachometer (could be difficult to make small adjustments with). |
| ![](A3946KLPTR-T.png)<br> A3946KLPTR-T Surface Mount Driver<br>$3.42/each<br>[link to product](https://www.digikey.com/en/products/detail/allegro-microsystems/A3946KLPTR-T/1006258)                 | \* High voltage option <br>\* Brushless<br>\* Overheat protections <br>\* Uses MOSFET                                               | \* More complex<br>\* Utilizes higher voltage <br>\* Not compatible with stepper motor |
| ![](IFX9201SGAUMA1.png)<br> IFX9201SGAUMA1 Surface Mount Driver<br>$3.55/each<br>[link to product](https://www.digikey.com/en/products/detail/infineon-technologies/IFX9201SGAUMA1/5415542)                 | \* Works with PIC <br>\* Works with stepper motor <br>\* Uses SPI or PWM <br>\* We already have it                                               | \* Difficult to use with MPLAB <br>\* DOES NOT WORK WITH BOTH PIC AND MOTOR SIMULTANEOUSLY |
| ![](TMC2209.png)<br> TMC2209 Surface Mount Driver<br>$5.20/each<br>[link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/TMC2209-LA-T/10232491)                 | \* Works with PIC <br>\* Works with stepper motor <br>\* Uses UART and simple GPIO connections <br>\* Compatible, simultaneously, with chosen PIC and Motor | \* More complex device than others |

**Rationale:** The TMC2209 is simultaneously compatible with the selected motor, and the PIC; it offers ease of adjustment, and uses only GPIO pins unless the user wants to program it with UART (uneccessary).
