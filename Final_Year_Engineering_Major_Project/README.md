# Flight Controller PCB Design Using KiCad

## Project Overview
This project involves designing a **Flight Controller PCB** using **KiCad**. The PCB is intended for drone and UAV applications, providing essential functionalities like sensor integration, power management, and communication interfaces for flight control.

## System Architecture
The PCB consists of multiple modules interconnected for efficient data processing and motor control:

- **Microcontroller Unit (MCU)**:
  - STM32H753VITx (Flight Control Computer - FCC)
  - STM32F405RGTx (Navigation Computer - NAVC)
- **Power Management**:
  - 3.3V and 5V voltage regulators
  - Battery monitoring and current sensing (INA219AIDCNR)
  - Reverse polarity protection
- **Communication Interfaces**:
  - I2C, SPI, UART
  - USB debugging and programming
  - CAN bus (future expansion)
- **Sensor Integration**:
  - Inertial Measurement Unit (IMU) - BMI088
  - Magnetometer - IIS2MDCTR
  - Barometer - MPRLS0025PA00001A
  - GPS Receiver - u-blox MAX-8Q
  - Temperature Sensor - TMP100
- **Peripheral Control**:
  - PWM outputs for ESC/motor control
  - General-purpose GPIOs for expansion
  - Debugging LEDs and status indicators

## PCB Design
- **Schematic Files**:
  - `FCC.kicad_sch` - Flight Control Computer
  - `NAVC.kicad_sch` - Navigation Computer
  - `FCCPeripherals.kicad_sch` - Flight Control Peripherals
  - `NAVCPeripherals.kicad_sch` - Navigation Peripherals
  - `Power.kicad_sch` - Power Distribution
  - `Connections.kicad_sch` - Interconnects and external interfaces
- **PCB Layout File**:
  - `Flight_controller_Project.kicad_pcb`
- **Manufacturing Files**:
  - Gerber files and drill files for PCB fabrication
  - BOM (`.csv/.xml`) for component listing

## Workflow
1. **Schematic Design** – Define circuit connections in KiCad.
2. **PCB Layout** – Optimize routing and placement for minimal interference.
3. **Gerber File Generation** – Export necessary manufacturing files.
4. **Fabrication & Assembly** – Order PCBs and assemble components.
5. **Testing & Debugging** – Verify power, communication, and sensor readings.
6. **Firmware Development** – Program MCU for flight control operations.

## Applications
- Autonomous UAV and drone flight control
- GPS-based navigation systems
- Sensor fusion and real-time data processing
- Research and prototyping of flight stabilization algorithms

## Future Enhancements
- Implement CAN bus communication for robust inter-device connectivity.
- Integrate additional sensors for improved stability and performance.
- Develop an RF-based remote control module for manual override.
- Optimize power management for extended battery life.

This project provides a deep understanding of **flight electronics, embedded systems, and PCB design**.
