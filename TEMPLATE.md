---
title: Motion Interface Tutorial
date: 2025-05-19
authors:
  - name: Majd Abu-Shamiyeh
---

![ESP32+MPU-6050](images/ESP32-MPU6050-Module-Accelerometer-Gyroscope-Temperature-Sensor-Arduino.webp)

## Introduction
This tutorial is aiming to teach how to interface an accelerometer sensor with an ESP32 Dev Board to detect motion. The motivation behind this tutorial is to help measure forces in all directions which allow to detect shakes, tilts and falls. I want readers to understand how to detect any type of motion and understand how to link the accelerometer with the Dev Board and how they can work correspondingly.

### Learning Objectives

- Understanding the basic functionalities of a three-axis acclerometer
- Configure and ESP32 board to communicate with a sensor
- How to read data and interpret the sensor
- How to impliment motion detection (shaking, tilting and ext.)
- Alarm motion event using LED indicator/sound.

### Background Information
Accelerometers are useful in measuring accelration in m/s^2. The MPU-6050 is an effective sensor that can communicate with board using I^2C or SPI to offer a slution.
I am using an MPU-6050 because it offers a combination of a 3‑axis accelerometer and a 3‑axis gyroscope in one chip. It is a 16-bit ADC and offers high resolution. It can store a high amount of data and can be supported ESP32 libraries. However, the only drawback is it's high power usage. An ADXL345 is an alterantive that uses low power but only detects linear motion, unlike an PU-6050 which is more effective in all types of motions (ex.rotational). 

## Getting Started

### Required Downloads and Installations
1. Arduino IDE
    - visit Arduino page
    - download latest version of Arduino IDE
    - Launch Arduino
2. ESP32 Board Support for Arduino
  -  https://youtu.be/HY8MFMrGo3k?si=LE2I5AAdRno9ZNeh
3. MPU6050 library download
  - https://youtu.be/I6cBs3yStf8?si=gQ7pF3agDsci_hiU

### Required Components

List your required hardware components and the quantities here.

| Component Name              | Quanitity |
| --------------              | --------- |
| ESP32 DevBoard              |      1     |
| MPU 6050 Acceleroneter      |      1     |
|Jumper Wires                 |     4      |
|USB-C                        |     1      |
|Breadboard                  |      1     |
### Required Tools and Equipment
- Computer with USB-C port
- Breadboard
- Jumper Wires

## Part 01: Sensor Wiring and Communiaction

### Introduction

Wiring the MPU 6050 sensor to the SP32 dev board to allow them to communicate

### Objective

Connect to power and confirm the MPU-6050 adress to prove connection.

### Background Information
- Understand how ESP32 Dev board functionality in relation to Arduino
- Learn how to connect MPU 6050 with board
- Volage compatibility, ensure both devices are compatable to avoid damages
- Debugging to confirm that the address is of the MPU 6050  sucessfully stored
- Wiring and lining pins up for pairing the devices.

### Components

- ESP32 Dev Board
- MPU 6050
- Jumper wires

### Instructional
1. Place components on breadboard (MPU-6050 and ESP32) so that they are alligned appropriately and GND pins allign with power rails.
2. Conmect ESP32 3V3 pin to MPU-6050 VCC pin
3. Connect ESP32 GND pin to MPU-6050 GND pin
4. Connect ESP32 SDA pin to MPU-6050 SDA pin
5. Connect ESP32 SCL pin to MPU-6050 SCL pin
6. Connect MPU-6050 pin to GND and set it's address
7. Upload I^2C sketch and verify that device is found using serial monitor

## Example

### Introduction

The I^2C scanner confirms that the MPU-6050 is connected and the sensor is communicating with the board effectively.

### Example

Example Output on Scanner:
I2C scanner
Found I2C device at "adress"
Found 1 devices

### Analysis

Found I2C device at "adress" tells the user that the MPU-6050 has been found and it's responding. Found device ensures that no errors have been found and the device is successfully connected.

## Additional Resources
Arduino Guide: https://www.arduino.cc/en/Guide/
MPU-6050 Datasheet: https://invensense.tdk.com/wp-content/uploads/2015/02/MPU-6000-Datasheet1.pdf
### Useful links

(https://www.youtube.com/watch?v=RiYnucfy_rs)

