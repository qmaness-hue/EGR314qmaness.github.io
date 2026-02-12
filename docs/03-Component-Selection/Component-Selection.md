---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

### Sensor

(**remove this note/placeholder**: if applicable, this is where your  **SELECTED** sensor is shown. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Sensor"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#sensor) selection.

### Actuator

(**remove this note/placeholder**: if applicable, this is where your **Selected** the actuator items go, which includes both the driver and motor. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Actuator"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#actuator) selection.

-----------
> Remove the following before submitting! Use them to present the selected components

### Style 1

> This is the example found in the assignment, uses more html

*Table 1: Example component selection*

**Motor Driver**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TC647BEOATR.png)<br> TC647BEOATR Surface Mount Driver<br>$1.64/each<br>[link to product](https://www.digikey.com/en/products/detail/microchip-technology/TC647BEOATR/562490)                 | \* Inexpensive[^1]<br>\* Brushless<br>\* Meets surface mount constraint of project <br>\* Inexpensive                                               | \* Made specifically for fans<br>\* Needs parallel interface. |
| ![](MAX6650EUB+T.png)<br> MAX6650EUB+T Surface Mount Driver<br>$8.82/each<br>[link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/MAX6650EUB-T/1521889)                 | \* Brushless<br>\* Can cover multiple parallel motors <br>\* Uses I2C Interface                                               | \* Relatively Expensive<br>\* Utilizes tachometer (could be difficult to make small adjustments with). |
| ![](A3946KLPTR-T.png)<br> A3946KLPTR-T Surface Mount Driver<br>$3.42/each<br>[link to product](https://www.digikey.com/en/products/detail/allegro-microsystems/A3946KLPTR-T/1006258)                 | \* High voltage option [^1]<br>\* Brushless<br>\* Overheat protections <br>\* Uses MOSFET                                               | \* More complex<br>\* Utilizes higher voltage |

**Rationale:** A clock oscillator is easier ....

**Motor Driver**

| **Component**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TC647BEOATR.png)<br> FIT0441 Gearmotor<br>$19.90/each<br>[link to product](https://www.digikey.com/en/products/detail/dfrobot/FIT0441/6588579)                 | \* Simple [^1]<br>\* Brushless<br>\*Powerful                                                | \* May not have accuracy required<br>\* Incremental |
| ![](MAX6650EUB+T.png)<br> MAX6650EUB+T Surface Mount Driver<br>$8.82/each<br>[link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/MAX6650EUB-T/1521889)                 | \* Brushless<br>\* Can cover multiple parallel motors <br>\* Uses I2C Interface                                               | \* Relatively Expensive<br>\* Utilizes tachometer (could be difficult to make small adjustments with). |
| ![](A3946KLPTR-T.png)<br> A3946KLPTR-T Surface Mount Driver<br>$3.42/each<br>[link to product](https://www.digikey.com/en/products/detail/allegro-microsystems/A3946KLPTR-T/1006258)                 | \* High voltage option [^1]<br>\* Brushless<br>\* Overheat protections <br>\* Uses MOSFET                                               | \* More complex<br>\* Utilizes higher voltage |

### Style 2

> Also acceptable, more markdown friendly

**External Clock Module**

1. XC1259TR-ND surface mount crystal

    ![](image1.png)

    * $1/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Inexpensive                               | Requires external components and support circuitry for interface |
    | Compatible with PSoC                      | Needs special PCB layout.                                        |
    | Meets surface mount constraint of project |

**Rationale:** A clock oscillator is easier ...
