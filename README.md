# Flight-Controller-FC-D1

A custom designed, minimalistic STM32F722RET6 based flight controller built from scratch for custom drone and aerospace experimentation.

## What is this project?

Flight Controller D1: is a custom made circuit board designed specifically to act as an stabilization unit for stabilising platforms. It breaks away from bulky flight controllers by packing only the essential, minimal form factor powered by an STM32 microcontroller and a modern BMI270.

## Purpose & What it does

The primary purpose of this board is to process orientation data. 
- Attitude: Reads high speed gyro and accelerometer data via the BMI270 sensor to keep the aircraft stable.
- Motor Control: Provides 4 dedicated motor output attachments to drive electronic speed controllers (ESCs) or micro motors.

## Why does it exist?

Building an off the shelf drone is fun, but designing the core avionics from the ground up teaches you how hardware, firmware, and circuit layout actually interact in the real world. 

- Aerospace Passion: As a personal stepping stone for aerospace and rocketry drone payloads having total control over a custom flight controller design opens up endless possibilities for tailored form factors.
- Just for Fun: Pure engineering curiosity testing whether a self routed PCB built in KiCAD can successfully boot, communicate, and stabilize a flight platform. (As of now, it's a first prototype fingers crossed that everything works as intended!)

## Bill of Materials

| Designator | Component | Footprint | LCSC Part Number | Description |
| :--- | :--- | :--- | :--- | :--- |
| U2 | STM32F411CEU6 | QFN-48 (7x7mm) | C60420 | Main MCU |
| U4 | BMI270 | 14-LGA (3x2.5mm) | C2836813 | Gyro + Accel |
| U3 | ME6211C33M5G-N | SOT-23-5 | C82942 | 3.3V Voltage Regulator |
| J1 | USB4105-GF-A-120 | USB-C 16-Pin SMT | C5184243 | USB-C Receptacle |
| Y1 | 16MHz Crystal | SMD 3225-4P | C13738 | Crystal Oscillator |
| C5, C6 | 10µF | 0603 (1608 Metric) | C19702 | Ceramic Capacitor |
| C7 | 2.2µF | 0603 (1608 Metric) | C23630 | Ceramic Capacitor |
| D1, D2 | LED | 0603 (1608 Metric) | C2290 | Status / Power LEDs |
| R3 | 1MΩ | 0603 (1608 Metric) | C22935 | Resistor |
| R4, R5 | 5.1kΩ | 0603 (1608 Metric) | C23186 | USB-C Resistors |
| R6, R7 | 10kΩ | 0603 (1608 Metric) | C25804 | Config Resistors |
| R8, R9 | 1kΩ | 0603 (1608 Metric) | C21190 | LED Current Limiting Resistors |

## Tools & Technologies

- PCB Design: KiCAD
- Firmware: None yet but with STm32cube

## Schematics & PCB Layout

## Schematic

<img width="654" height="718" alt="image" src="https://github.com/user-attachments/assets/0ccd47c8-bb88-4641-b110-fde66d676c08" />
<img width="479" height="636" alt="image" src="https://github.com/user-attachments/assets/757a7c8d-2c98-4bb6-ac80-7dbd220b2024" />

## PCB

<img width="1214" height="832" alt="image" src="https://github.com/user-attachments/assets/121fea66-65ed-47fa-9150-e888cc171839" />
<img width="904" height="629" alt="image" src="https://github.com/user-attachments/assets/0155aa55-e14f-4b08-951f-af8e774156b9" />

## Extras

I liked this way more than id like to admit making this was really fun for me and it was just so freeing.

## Bonus

Before settling on the BMI270, early iterations used the older MPU6050. Transitioning away from it was a major hurdle due to its age and lack of modern integration support, making the shift to the BMI270 a much cleaner and more reliable choice for modern layouts.

<img width="431" height="397" alt="Old MPU6050 Iteration" src="https://github.com/user-attachments/assets/0b2d92ee-48ac-4365-8c29-1a148eaae829" />

Also an old version of the FC.

<img width="694" height="539" alt="Screenshot 2026-11-13 192732" src="https://github.com/user-attachments/assets/0f926eb9-1968-44eb-b124-582737e4d41a" />


