# Piezoelectric Footstep Power Generation System

This project focuses on sustainable energy harvesting by converting the kinetic energy generated from human walking into usable electricity. 

Built around an **Arduino Uno**, the system utilizes **piezoelectric transducers** to capture mechanical stress from footsteps, rectify the output, and store the energy in a **lithium-ion battery**. This stored energy is then used to power low-voltage electronics, demonstrating a viable method for renewable energy generation in high-traffic areas.


## Hardware Components

| Category | Component | Details |
| :--- | :--- | :--- |
| **Control Unit** | Arduino Uno | Microcontroller for system logic. |
| **Harvesting** | Piezoelectric Transducers | Sensors to capture kinetic energy. |
| **Visualization** | LCD Display | I2C-based Liquid Crystal Display. |
| **Energy Storage** | Li-Ion Battery | 18650 type battery. |
| **Rectification** | Diodes | 1N4007 (for converting AC to DC). |
| **Regulation** | Circuitry | Transistor (BC547), Resistors (100kΩ, 10kΩ), Capacitors (10µF). |
| **Prototyping** | Breadboard & Wires | For assembly and connections. |


![licensed-image](https://github.com/user-attachments/assets/6fbaeb78-2837-4fa1-8e3b-d18d3b6b59bd)

## System Architecture

The system operates in three distinct stages to harvest and utilize energy:

1.  **Kinetic Conversion** Piezoelectric sensors are arranged in a specific array. When pressure is applied via footsteps, these sensors generate an AC (Alternating Current) voltage signal.

2.  **Rectification & Storage** Since the sensors output AC, the signal is passed through a bridge rectifier (using diodes) to convert it into DC (Direct Current). This energy is filtered using capacitors and stored in the 18650 Li-Ion battery.

3.  **Utilization** The stored power is regulated to operate the system's load, which includes the I2C LCD display (showing real-time voltage stats) and other small peripherals like LEDs or sensors.

---

## Deployment Guide

Follow these steps to replicate the project:

### 1. Assembly
Construct the hardware connections following the schematic provided in `Circuit.txt`. Ensure the piezoelectric sensors are connected in parallel/series (depending on your voltage requirements) and properly shielded.

### 2. Firmware Upload
1.  Open the Arduino IDE.
2.  Connect your Arduino Uno via USB.
3.  Upload the `main.ino` file to the board.

### 3. Operation
1.  Install the sensor plate (containing the transducers) in a walkway or under a doormat.
2.  Walk on the plate to begin generating energy.
3.  Observe the LCD display for real-time voltage generation and battery status.

---

## Future Improvements

-  **Optimization:** Refine the piezoelectric array configuration for higher voltage efficiency per step.
-  **Supercapacitors:** Integrate supercapacitors for faster charge/discharge cycles compared to Li-Ion batteries.
-  **Ruggedization:** Develop a durable, weather-resistant enclosure for the sensor pad to ensure long-term durability in outdoor environments.



