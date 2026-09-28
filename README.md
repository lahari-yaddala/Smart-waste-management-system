# Smart-waste-management-system

# Smart Waste Management System Using Arduino

## Project Overview

The Smart Waste Management System is an Arduino-based project designed to automatically segregate wet and dry waste using sensors and a servo motor.

An ultrasonic sensor detects the presence of waste, while a moisture sensor measures its moisture content. Based on the sensor reading, the Arduino controls a servo motor to direct the waste into the appropriate bin.

**Note:** This repository contains a reconstructed reference implementation. The moisture threshold and servo positions must be calibrated for the actual hardware.

## Components Required

- Arduino Uno
- HC-SR04 Ultrasonic Sensor
- Moisture Sensor
- Servo Motor
- Breadboard
- Jumper Wires
- Wet and Dry Waste Bins
- Power Supply

## Working Principle

1. The ultrasonic sensor detects waste placed near the bin.
2. When waste is detected within 10 cm, the Arduino reads the moisture sensor.
3. If the moisture reading indicates wet waste, the servo rotates toward the wet-waste compartment.
4. Otherwise, the servo rotates toward the dry-waste compartment.
5. After a short delay, the servo returns to its initial position.

## Pin Connections

| Component | Arduino Pin |
|-----------|-------------|
| Ultrasonic TRIG | D9 |
| Ultrasonic ECHO | D10 |
| Moisture Sensor AO | A0 |
| Servo Signal | D11 |
| Sensor VCC | 5V |
| Sensor GND | GND |

Connect the servo to a suitable power supply and ensure that the servo power supply and Arduino share a common ground.

## Software Requirements

- Arduino IDE
- Arduino Servo Library

## Algorithm

1. Initialize the ultrasonic sensor, moisture sensor and servo motor.
2. Measure the distance using the ultrasonic sensor.
3. If an object is detected within 10 cm, read the moisture sensor.
4. Compare the moisture reading with the calibrated threshold.
5. Rotate the servo toward the appropriate waste compartment.
6. Return the servo to its initial position.
7. Repeat the process.

## Applications

- Automated waste segregation
- Smart dustbins
- Educational IoT and embedded systems projects
- Sensor-based automation

## Future Improvements

- Add a bin-level monitoring sensor.
- Integrate ESP32 for remote monitoring.
- Add an LCD to display the waste category.
- Improve classification using additional sensors.

## Project Status

Reference Arduino implementation provided. Original prototype testing and demonstration results are not included in this repository.

## Author

Yaddala Lahari  
Electronics and Communication Engineering  
SRM University-AP
