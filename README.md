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

## BOM

| Designator | Component | LCSC Part Number / Link | Description |
| :--- | :--- | :--- | :--- |
| U1 | STM32F722RET6 | C118207 | Main MCU |
| U4 | BMI270 | C2836813 | Gyro and accelerometer |
| U2 | AMS1117-3.3 | C5632159 | 3.3V regulator |
| X1 | X322525MOB4SI | C9006 | 25MHz crystal |
| X2 | Q13FC1350000400 | C32346 | 32.768kHz crystal |
| L1 | FCM1608KF-601T03 | C141723 | Ferrite bead |
| D1, D2 | XL-1608SURC-06 | C965799 | Status LEDs |
| D3, D4 | Schottky diode | C7370889 | Input diodes |
| SW1, SW2 | TS-1088-AR02016 | C720477 | BOOT and RESET buttons |
| C1, C2, C3 | 100nF | C1525 | Decoupling capacitors |
| C4, C7, C8, C9 | 20pF | C1554 | Crystal load capacitors |
| C5 | 22µF | C59461 | Regulator output capacitor |
| C6 | 10µF | C19702 | Regulator input capacitor |
| C10 | 2.2µF | C386031 | VCAP capacitor |
| C11, C12, C13 | 1µF | C52923 | Decoupling capacitors |
| C14 | 10µF | C15525 | Bulk capacitor |
| C15, C16, C17, C18, C19 | 100nF | C5142565 | Decoupling capacitors |
| R1 | 10kΩ | C54530535 | BOOT0 pull-down |
| R4, R5 | 5.1kΩ | C23186 | USB-C resistors |
| R2, R3 | 470Ω | C23179 | LED resistors |
| PCB | | | https://jlcpcb.com/ |

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


