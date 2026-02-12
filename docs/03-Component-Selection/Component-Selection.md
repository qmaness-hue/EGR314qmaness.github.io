---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

### Actuator

(**remove this note/placeholder**: if applicable, this is where your **Selected** the actuator items go, which includes both the driver and motor. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Actuator"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#actuator) selection.

-----------
> Remove the following before submitting! Use them to present the selected components

*Table 1: Motor Driver Table*

**Motor Driver**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TC647BEOATR.png)<br> TC647BEOATR Surface Mount Driver<br>$1.64/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC647BEOATR/562490)                 | \* Inexpensive[^1]<br>\* Brushless<br>\* Meets surface mount constraint of project <br>\* Inexpensive                                               | \* Made specifically for fans<br>\* Needs parallel interface. |
| ![](MAX6650EUB+T.png)<br> MAX6650EUB+T Surface Mount Driver<br>$8.82/each<br>[link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/MAX6650EUB-T/1521889)                 | \* Brushless<br>\* Can cover multiple parallel motors <br>\* Uses I2C Interface                                               | \* Relatively Expensive<br>\* Utilizes tachometer (could be difficult to make small adjustments with). |
| ![](A3946KLPTR-T.png)<br> A3946KLPTR-T Surface Mount Driver<br>$3.42/each<br>[link to product](https://www.digikey.com/en/products/detail/allegro-microsystems/A3946KLPTR-T/1006258)                 | \* High voltage option [^1]<br>\* Brushless<br>\* Overheat protections <br>\* Uses MOSFET                                               | \* More complex<br>\* Utilizes higher voltage |

**Rationale:** The MAX driver may be more expensive than alternatives, but it makes up for it by being adjustable, accurate, and easy to use.

*Table 2: Gearmotor Table*

**Gearmotor**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](FIT0441.png)<br> FIT0441 Gearmotor<br>$19.90/each<br>[link to product](https://www.digikey.com/en/products/detail/dfrobot/FIT0441/6588579)                 | \* Simple [^1]<br>\* Brushless<br>\*Powerful                                                | \* May not have accuracy required<br>\* Incremental |
| ![](SER0070.png)<br> SER0070 Servo Motor <br>$24.88/each<br>[link to product](https://www.mouser.com/ProductDetail/DFRobot/SER0070?qs=6avfeC6zeS5mmJI6Z%252BxOKw%3D%3D)                 | \* Brushless<br>\* Servo Motor <br>\* Accurate and powerful                                               | \* Relatively Expensive<br>\* No datasheet |
| ![](324.png)<br> 324 Stepper Motor <br>$14.00/each<br>[link to product](https://www.digikey.com/en/products/detail/adafruit-industries-llc/324/5022791)                 | \* Simple [^1]<br>\* 200 Steps per revolution (accurate)<br>\* Inexpensive                                               | \* Not super accurate <br>\* Not super powerful |

**Rationale:** The FIT DC gear motor is relatively simple while maintaining high torque and easily optimized accuracy.
