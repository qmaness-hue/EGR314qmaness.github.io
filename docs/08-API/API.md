---
title: Motor Subsystem API
---

# Motor Subsystem API

This document defines the communication interface for the Dual-Motor Subsystem.  
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
| Variable Name             | enable_type       | enable_flag        | reserved           |
| Variable Type        | uint8              | uint8              | uint8              |
| Min value        | 0x02               | 0 (off)            | 0                   |
| Max Value        | 0x03                | 1 (on)            | 0
| Example    | 0x02               | 1                  | 0                  |

---

## 3. SET SPEED Command

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Variable Name             | speed_type       | speed_value        | reserved           |
| Variable Type        | uint8              | uint8              | uint8              |
| Min Value        | 0x04                | 0                  | 0                  |
| Max Value        | 0x05                | 255                | 0                |
| Example    | 0x04               | 125                | 0                  |

---

## 4. STOP Command

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Variable Name             | stop_type       | Reserved           | Reserved           |
| Variable Type        | uint8              | uint8              | uint8              |
| Min Value         | 0x06              | 0                   | 0                  |
| Max Value         | 0x06              | 0                  | 0                   |
| Example    | 0x06               | 0                  | 0                  |

---

## Messages Sent (Responses)

## 1. ACK (Acknowledgment)

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Variable Name             | status_code        | command_echo       | Reserved           |
| Variable Type        | uint8              | uint8              | uint8              |
| Min Value         | 0x09              | 0x00                | 0                  |
| Max Value        | 0x10                | 0x01              | 0                  |
| Example    | 0x10               | 0x01 (MOVE)        | 0                  |

---

## 2. STATUS Message

| Field            | Byte 1              | Byte 2              | Byte 3              |
|------------------|--------------------|--------------------|--------------------|
| Variable Name             | position_code        | current_x_position | current_y_position |
| Data Type        | uint8              | uint8              | uint8              |
| Min Value        | 0x11                | 0                  | 0                  |
| Max Value        | 0x11                | 100              | 100                |
| Example    | 0x11               | 50                | 50                 |

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
