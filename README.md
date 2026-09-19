# water-level-indicator

An embedded C++ firmware to automatically track and measure the water level in a tank or vessel in real-time. The application triggers various visual/audio indicators according to the level thresholds crossed and prevents overflow/dry running of the tank.


## Key Features

The water-level-indicator application has the following features:

Multi-Level Threshold Detection

Monitors and tracks the water level crossing the low, medium, and high thresholds.

Automated Alerts

The system has indicators that get triggered automatically when the tank level reaches certain thresholds.

Debounced Inputs

The free surface oscillations of the water level are damped and filtered out to avoid false indications.

Modular Embedded C++ Implementation

The C++ code has been modularized and decoupled for better maintainability and easy debugging.

## Hardware Connections

The following table describes the connections between the microcontroller and the various hardware peripherals:

Peripheral Type Pin Type Arduino Pin Description

Low Level Sensor / Contact Digital / Analog In A0 / D2 Low Level Detect Input

Mid Level Sensor / Contact Digital / Analog In A1 / D3 Mid Level Detect Input

High / Full Level Sensor Digital / Analog In A2 / D4 High Level Detect Input

Status LEDs (Green/Yellow/Red) Digital Out D8, D9, D10 Level Status Indicators

Alarm Buzzer Digital / PWM Out D11 Overflow Alarm Buzzer

## Working

The embedded application works by:

Sampling the water-level sensor and determining its current state or level.

Actuating the status indicators (LEDs and buzzer) as specified for the corresponding level.

## Repository Structure

The water-level-indicator project has the following key files:

File Description

src/main.cpp or src/sketch.ino Embedded C++ code to implement the water-level-indicator application.

README.md Project overview documentation and direct link to interactive prototype.
##License
This project is licensed under the MIT License.
