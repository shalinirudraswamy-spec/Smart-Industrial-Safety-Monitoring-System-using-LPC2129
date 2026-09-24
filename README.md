# Smart Industrial Safety Monitoring System using LPC2129

## Project Overview

The Smart Industrial Safety Monitoring System is an ARM7-based embedded system developed using the LPC2129 microcontroller. The system is designed to monitor industrial safety conditions such as temperature, worker movement, and fire detection.

The system uses an LM35 temperature sensor, PIR motion sensor, and flame sensor. The LPC2129 processes the sensor inputs and displays the system status on a 16x2 LCD. The sensor information is also transmitted to a PC/Laptop through UART. LED indicators provide visual status indication.

## Hardware Components

- LPC2129 ARM7 Microcontroller
- LM35 Temperature Sensor
- PIR Motion Sensor
- Flame Sensor
- 16x2 LCD Display
- 3 LEDs
- UART
- 5V Power Supply
- PC/Laptop

## Pin Connections

| Component | LPC2129 Pin |
|---|---|
| LM35 Temperature Sensor | P0.28 |
| PIR Motion Sensor | P0.30 |
| Flame Sensor | P0.5 |
| LED1 | P0.17 |
| LED2 | P0.18 |
| LED3 | P0.19 |

## Required Functions

1. GPIO Initialization
2. UART Display
3. ADC Initialization
4. Read ADC
5. Temperature Conversion
6. PIR Sensor Read
7. Flame Sensor Read
8. LCD Display
9. LED Indication

## Working Principle

The LM35 temperature sensor provides an analog output to the LPC2129 ADC.

The PIR sensor provides a digital input to detect worker movement, while the flame sensor provides a digital input for fire detection.

The LPC2129 processes all sensor inputs and provides the following outputs:

- Temperature and system status on the 16x2 LCD
- Sensor information through UART terminal
- System condition through LED indicators

## Normal Condition – SAFE

Example:

```text
Temperature : 30°C
PIR Sensor  : Worker Not Detected
Flame Sensor: No Fire
Machine Status: SAFE
LED Status  : GREEN LED ON