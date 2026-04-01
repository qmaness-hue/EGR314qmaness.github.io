---
title: Module's Selected Microcontroller
---

## Intro

The following section contains information regarding the selected microcontroller necessary for the motor system that will turn the EV Scope so as to properly track celestial/distant objects.

**Role and Responsibilities**

The role of this subsystem of the EV Scope is to accurately recieve instruction from the human interface, and then interpret that information and make movements to accomplish the given need. The motor needs to accurately move in the manner that the user wishes--meaning that the motor has to accurately interpret data from the human interface, and subsequently make precise movement to accomplish the given task.

## Selected Microcontroller

The microcontroller I selected for the motor system is the surface mount version of the PIC18F57Q43, a microcontroller provided in class. The motor driver and gearmotor I selected are compatible with the PIC18F57Q43. The motor driver I selected--the TMC2209--utilizes the GPIO and UART (uneccessary) interface. The UART with MPLAB interface is covered in depth during class, making it a well understood software. All parameters appear to match up, as I did the component selection with the microcontroller given in class in mind.

**MPLAB Pin Configuration**
![](TQFP48.png)

The selected motor driver (TMC2209) is compatible with the selected PIC18F57Q43 microcontroller. In the figure above, you can see all allocations needed for communications between the drivers, LEDs, and the debugging button with the PIC.

## Driver-Microcontoller Communications
**Pinout for TMC2209**
![](TMC2209_pinout.png)

**Pinout for Driver 1**

| **Pin**                                                   | **Pin Function**                                                                                         | **Connection**                                                                                                       |
| -------------------------- | -------------------------------------------------------- | ------------------------------------------------------- |
| Pin 1 (OB2) | Motor Coil B Output 2 | Motor |
| Pin 2 (ENN) | Enable not input | Not Connected |
| Pin 3 (GND1) | Ground 1 | Ground |
| Pin 4 (CPO) | Charge pump capacitor output | CPI |
| Pin 5 (CPI) | Charge pump capacitor input | CPO |
| Pin 6 (VCP) | Charge pump voltage | VS |
| Pin 7 (SPREAD) | Chopper mode selection | Not Connected |
| Pin 8 (5VOUT) | Output of internal voltage regulator | GND1 |
| Pin 9 (MS1_AD0) | Microstep resolution configuration | Ground |
| Pin 10 (MS2_AD1) | Microstep resolution configuration | Ground |
| Pin 11 (DIAG) | Diagnostic output (HIGH = error) | GPIO RD2 |
| Pin 12 (INDEX) | Provides index pulse | Not Connected |
| Pin 13 (CLK) | Clock input | Ground |
| Pin 14 (PDN_UART) | Optional UART Input/Output | UART3 RF1 |
| Pin 15 (VCC_IO) | Supply voltage for digital pins | Voltage Regulator |
| Pin 16 (STEP) | STEP input | GPIO RF0 |
| Pin 17 (VREF) | Analog reference voltage | Not Connected |
| Pin 18 (GND2) | Ground 2 | Ground |
| Pin 19 (DIR) | Direction input | GPIO RA6 |
| Pin 20 (STDBY) | Standby input | Ground |
| Pin 21 (OA2) | Motor Coil A Output 2 | Motor |
| Pin 22 (VS) | Voltage supply for motor | Voltage Regulator |
| Pin 23 (BRA) | Sense resistor connection for coil A | Ground |
| Pin 24 (OA1) | Motor Coil A Output 1 | Motor |
| Pin 25 (NC) | Unused | Not Connected |
| Pin 26 (OB1) | Motor Coil B Output 1 | Motor |
| Pin 27 (BRB) | Sense resistor connection for coil B | Ground |
| Pin 28 (VS) | Voltage supply for motor | Voltage Regulator |
| Pin 29 (EPAD) | Exposed die pad | Ground |

**Pinout for Driver 2**

| **Pin** | **Pin Function** | **Connection** |
|-----|-------------|------------|
| Pin 1 (OB2) | Motor Coil B Output 2 | Motor 2 |
| Pin 2 (ENN) | Enable not input | Not Connected |
| Pin 3 (GND1) | Ground 1 | Ground |
| Pin 4 (CPO) | Charge pump capacitor output | CPI |
| Pin 5 (CPI) | Charge pump capacitor input | CPO |
| Pin 6 (VCP) | Charge pump voltage | VS |
| Pin 7 (SPREAD) | Chopper mode selection | Not Connected |
| Pin 8 (5VOUT) | Output of internal voltage regulator | GND1 |
| Pin 9 (MS1_AD0) | Microstep resolution configuration | Ground |
| Pin 10 (MS2_AD1) | Microstep resolution configuration | Ground |
| Pin 11 (DIAG) | Diagnostic output (HIGH = error) | GPIO RB3 |
| Pin 12 (INDEX) | Provides index pulse | Not Connected |
| Pin 13 (CLK) | Clock input | Ground |
| Pin 14 (PDN_UART) | Optional UART Input/Output | UART4 RA0 |
| Pin 15 (VCC_IO) | Supply voltage for digital pins | Voltage Regulator |
| Pin 16 (STEP) | STEP input | GPIO RC2 |
| Pin 17 (VREF) | Analog reference voltage | Not Connected |
| Pin 18 (GND2) | Ground 2 | Ground |
| Pin 19 (DIR) | Direction input | GPIO RB5 |
| Pin 20 (STDBY) | Standby input | Ground |
| Pin 21 (OA2) | Motor Coil A Output 2 | Motor 2 |
| Pin 22 (VS) | Voltage supply for motor | Voltage Regulator |
| Pin 23 (BRA) | Sense resistor connection for coil A | Ground |
| Pin 24 (OA1) | Motor Coil A Output 1 | Motor 2 |
| Pin 25 (NC) | Unused | Not Connected |
| Pin 26 (OB1) | Motor Coil B Output 1 | Motor 2 |
| Pin 27 (BRB) | Sense resistor connection for coil B | Ground |
| Pin 28 (VS) | Voltage supply for motor | Voltage Regulator |
| Pin 29 (EPAD) | Exposed die pad | Ground |
