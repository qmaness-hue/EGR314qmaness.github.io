---
title: Motor Subsystem API
---

# Motor Subsystem API

This document defines the communication interface for the Motor Subsystem.  
All messages follow a fixed 3-byte structure.

---

## Messages Received (Commands)

## 1. MOVE Command — Translate Coordinate Input to Motor Movement

|           | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Variable Name             | command_type       | x_coordinate       | y_coordinate       |
| Variable Type        | uint8              | int16 / uint8      | int16 / uint8      |
| Min Value    | 0x00     | 0      | 0      |
| Max Value    | 0x01     | 255    |255     |
| Example    | 0x01               | 100                | 50                 |

---

## 2. MOTOR ENABLE Command

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Command Type       | Enable Flag        | Reserved           |
| Description      | Enables motors     | 1 = ON, 0 = OFF    | Not used           |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0x02               | 1                  | 0                  |
| Notes            | Safety control     | Required           | Set to 0           |

---

## 3. SET SPEED Command

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Command Type       | Speed Value        | Reserved           |
| Description      | Sets motor speed   | Speed level        | Not used           |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0x03               | 200                | 0                  |
| Notes            | PWM / step rate    | Range: 0–255       | Set to 0           |

---

## 4. STOP Command

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Command Type       | Reserved           | Reserved           |
| Description      | Stops all motion   | Not used           | Not used           |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0x04               | 0                  | 0                  |
| Notes            | Immediate halt     | Set to 0           | Set to 0           |

---

## Messages Sent (Responses)

## 1. ACK (Acknowledgment)

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Status Code        | Command Echo       | Reserved           |
| Description      | Confirms command   | Echo of Byte 1     | Not used           |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0x10               | 0x01 (MOVE)        | 0                  |
| Notes            | Success response   | Matches command    | Set to 0           |

---

## 2. STATUS Message

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Status Code        | Current X Position | Current Y Position |
| Description      | Reports position   | X position         | Y position         |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0x11               | 100                | 50                 |
| Notes            | Periodic update    | Scaled value       | Scaled value       |

---

## 3. ERROR Message

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Name             | Status Code        | Error Code         | Reserved           |
| Description      | Indicates failure  | Type of error      | Not used           |
| Data Type        | uint8              | uint8              | uint8              |
| Example Value    | 0xFF               | 0x01               | 0                  |
| Notes            | Error handling     | See table below    | Set to 0           |

---

## Error Codes

| Code | Meaning                  |
|------|--------------------------|
| 0x01 | Invalid Command          |
| 0x02 | Invalid Parameter        |
| 0x03 | Motor Disabled           |
| 0x04 | Out of Range             |
| 0x05 | Hardware Failure         |

---

# Example Message Flow

### Valid MOVE Command
