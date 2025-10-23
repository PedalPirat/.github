# PedalPirat Repository Summary

## Project Overview
PedalPirat is an ambitious **Open Source Bike Platform** that aims to create the ultimate smart bike by integrating multiple wireless protocols including ANT+, CAN, Bluetooth, and Power Delivery technologies.

## Core Mission
The project seeks to revolutionize cycling technology by creating a vendor-independent, open-source platform that enhances bike functionality, safety, and user experience.

## Project Goals
The PedalPirat project pursues several innovative objectives:

1. **Power Management**: Replace proprietary batteries with a central powerbank that can be charged by a hub dynamo
2. **Interoperability**: Enable vendor-independent component integration (e.g., Shimano levers with SRAM AXS)
3. **Enhanced Security**: Implement light control, radars, and AI-powered cameras for rider safety
4. **E-Bike Integration**: Bring e-bike technology to traditional bikes (e.g., Rohloff E-14)
5. **Smart Automation**: Automated shifting and reporting of cars parked in bike paths
6. **Fun Features**: Including heated handlebar tape
7. **Data Management**: Comprehensive data fusion and logging capabilities

## Current Integrations
The project currently supports:
- **Rohloff E-14** (via CAN bus)
- **Shimano GRX Di2 wired Levers** (via CAN/Contact)
- **ANT+ Devices**: 
  - Quarq TyreWiz 2.0
  - Quarq DZero DUB
  - RockShox Reverb AXS
  - HR-Belt
  - Additional ANT+ compatible devices

## Custom Hardware Architecture

### Main Controller / Mecha Comet Extension
- **MCU**: nRF54H20 with USB and CAN connectivity
- **GPS**: u-blox MAX-M10S
- **IMU**: Bosch BHI385 Smart Sensor
- Connects to rear MCU and Rohloff system

### Rear Controller
- **MCU**: nRF54H20 with CAN bus
- Rohloff E-14 integration
- Bikone BB Torque Sensor connectivity
- Rear light control

### Input Controls
- Brake sensor input
- Turn signals
- Snapshot/Report functionality
- Shift Up/Down controls
- Bike computer control
- Joystick/other inputs

### Turn Signal System
Planned models:
- Ergon-Endcap
- Surly Moloko Extension
- Rear Light integration
- LIN-based communication protocol

### Light Controller
Designed for LiteMove RX-E90 High-Low Beam:
- Lumissil IS32LT3183A controller
- High beam control
- On/Off functionality

## Integrated Commercial Hardware

### Computer Platform
- **Mecha Comet**: Linux handheld with touchscreen for bike computer functionality

### Bike Components
- **Bikone BB Torque Sensor (BSA)**: Measures power and crank position for optimal shift timing
- **Forumslader Aheadlader V6**: Powerbank with hub dynamo charger, provides 5V and 12V outputs
- **Rohloff E-14**: Electronic shifting system
- **Quarq TyreWiz 2.0**: Tire pressure monitoring system

### Electronic Components
**Microcontrollers & Processors**:
- Nordic Semi nRF54H20 MCU
- Melexis LED Controller
- Lumissil LIN Controller
- u-blox MAX-M10S GPS
- Bosch BHI385 Smart Sensor
- TI USB-PD Powerbank Eval Board
- MPS Powerbank Eval Board
- Rotary Sensor

**Imaging**:
- AI Camera for smart rear-view functionality

## Software Stack

### Operating System
- **Zephyr Project**: Real-time operating system (RTOS) for microcontroller programming

### Applications
- **Pi Zero Bike Computer**: Open-source bike computer software

## Communication Protocols
The project utilizes multiple industry-standard protocols:
- **ANT+**: For fitness device communication
- **CAN**: Controller Area Network for automotive-grade reliability
- **LIN**: Local Interconnect Network for automotive lighting

## Development Timeline

The project was initiated on **October 17, 2025** and has seen rapid development:

1. **October 17, 2025**: Initial repository creation
2. **October 22, 2025**: Major documentation updates including:
   - Addition of project goals and architecture diagram
   - Integration of hardware specifications
   - Documentation of commercial component integrations
   - Addition of automation features (shifting and car reporting)
   - Multiple refinements to README formatting and content
   - Link additions for various components

The project has been actively maintained by **Johannes Gedicke** (gedicke-dev), with 18 commits focused on building comprehensive documentation and project architecture.

## Innovation Highlights

1. **Vendor Independence**: Breaking down proprietary barriers in bike component ecosystems
2. **AI Integration**: Using machine learning for safety features like detecting parked cars on bike paths
3. **Unified Power System**: Centralized power management for all bike electronics
4. **Multi-Protocol Support**: Seamless integration of ANT+, CAN, Bluetooth, and LIN protocols
5. **Open Source Approach**: Making advanced bike technology accessible to everyone

## Technical Architecture
The system uses a distributed architecture with:
- Front controller managing GPS, IMU, and user interface
- Rear controller handling drivetrain and power sensing
- CAN bus for reliable inter-controller communication
- Multiple wireless protocols for sensor integration
- Linux-based bike computer for advanced features

## Project Status
The project is in **active planning and documentation phase**, with comprehensive hardware specifications defined and integration pathways documented. The focus has been on creating a solid foundation for implementation with clear documentation of all components and their interactions.

## Repository Structure
The main repository contains:
- Comprehensive README.md with full project documentation
- PedalPiratController.drawio.png: System architecture diagram
- Well-organized sections covering goals, integrations, hardware, and software

---
*This summary was generated on October 23, 2025, based on the content and commit history of the PedalPirat/PedalPirat repository.*
