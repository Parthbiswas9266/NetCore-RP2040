# NetCore RP2040 | Ethernet Development Board

<p align="center">
  <img src="3D%20Renders/3D_PCB1_2026-10-31.png" alt="NetCore RP2040 3D PCB Render" width="75%">
</p>

<p align="center">
  <b>A Compact RP2040-Based Ethernet Development Platform</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCU-RP2040-blue">
  <img src="https://img.shields.io/badge/Ethernet-W5500-orange">
  <img src="https://img.shields.io/badge/Speed-10%2F100%20Mbps-green">
  <img src="https://img.shields.io/badge/USB-Type--C-blue">
  <img src="https://img.shields.io/badge/License-MIT-yellow">
</p>

## Overview

**NetCore RP2040** is a compact Ethernet-enabled development board built around the Raspberry Pi RP2040 microcontroller and the WIZnet W5500 hardware TCP/IP Ethernet controller.

Designed with space efficiency and embedded networking applications in mind, the board integrates wired Ethernet connectivity, USB Type-C programming and power, external QSPI flash storage, and essential debugging and expansion interfaces into a compact PCB.

By offloading TCP/IP processing to the W5500, the RP2040 can focus on application-level processing while maintaining reliable wired network connectivity through a dedicated SPI interface.

NetCore RP2040 is intended as a hardware platform for embedded networking, IoT devices, Ethernet-enabled controllers, monitoring systems and compact industrial communication applications.

## Key Features

- **RP2040 Microcontroller:** Dual-core ARM Cortex-M0+ processor.
- **W5500 Ethernet Controller:** Hardware TCP/IP offloading with 10/100 Mbps Ethernet support.
- **Integrated RJ45 MagJack:** HR911105A connector with built-in Ethernet magnetics.
- **16MB QSPI Flash:** W25Q128JVSIQ external flash memory.
- **USB Type-C:** Native USB connectivity for programming, debugging and 5V power.
- **Dedicated Ethernet Supply Filtering:** Ferrite bead and local decoupling for improved supply noise management.
- **Compact Expansion Interface:** Essential I²C, UART, GPIO and power connections.
- **Debugging Support:** SWD interface and onboard status indicators.
- **Space-Optimized PCB:** Compact component placement for embedded applications.

## Hardware Architecture

The hardware is organized into three primary functional sections.

### 1. Processing Unit

The processing section is built around the Raspberry Pi RP2040 microcontroller.

| Component | Part Number | Description |
|---|---|---|
| MCU | RP2040 | Dual-core microcontroller |
| External Flash | W25Q128JVSIQ | 128Mbit / 16MB QSPI flash |
| MCU Clock | 27MHz reference | Clock circuitry |
| Debug Interface | SWD | Programming and debugging |

### 2. Power Management

The board accepts 5V power through its USB Type-C connector and generates the required 3.3V operating rail.

Key components:

- BL1117-33CX linear voltage regulator.
- Input and output decoupling capacitors.
- Local power filtering.
- Dedicated supply conditioning for the Ethernet subsystem.

### 3. Ethernet Subsystem

The networking section uses the WIZnet W5500 hardwired TCP/IP Ethernet controller.

| Component | Part Number | Description |
|---|---|---|
| Ethernet Controller | W5500 | Hardware TCP/IP controller |
| RJ45 Connector | HR911105A | Integrated Ethernet magnetics |
| Ethernet Crystal | 25MHz | W5500 reference clock |
| Ferrite Bead | Y1160808U300 | Ethernet supply filtering |

The RP2040 communicates with the W5500 through the SPI1 interface, with dedicated reset and interrupt signals.

The W5500 provides hardware TCP/IP functionality and supports up to eight independent hardware sockets.

## Expansion Interface

A compact 2 × 4 pin connector provides access to essential external interfaces.

Available signals include:

- I²C SDA
- I²C SCL
- UART TX
- UART RX
- 3.3V
- GND
- VBUS
- GPIO3

Refer to the schematic for the exact connector pinout.

## PCB Design

The PCB layout focuses on minimizing board dimensions while maintaining clear functional separation between processing, power management and Ethernet circuitry.

Design considerations include:

- Compact component placement.
- Optimized SPI signal routing.
- Localized power decoupling.
- Dedicated Ethernet supply filtering.
- Integrated Ethernet magnetics.
- Accessible USB programming interface.
- Compact expansion and debugging connections.

## Project Files

All major hardware design and manufacturing deliverables are available in this repository.

| Directory | Contents |
|---|---|
| `3D Renders/` | 3D PCB render and design overview PDF |
| `SCHEMATICS/` | Complete schematic PDF |
| `BOM & CLP/` | Bill of Materials and Pick & Place files |
| `GERBER/` | PCB fabrication Gerber archive |

### Quick Access

- [3D PCB Render](3D%20Renders/3D_PCB1_2026-10-31.png)
- [Design Overview PDF](3D%20Renders/NetCore%202040.pdf)
- [Complete Schematic](SCHEMATICS/SCH_Schematic1_2026-10-31.pdf)
- [Bill of Materials (BOM)](BOM%20%26%20CLP/BOM_Board1_PCB1_2026-10-31.csv)
- [Pick and Place File](BOM%20%26%20CLP/PickAndPlace_PCB1_2026_10_31.csv)
- [Gerber Manufacturing Files](GERBER/NetCore%202040.zip)

## Technical Specifications

| Parameter | Specification |
|---|---|
| Project Name | NetCore RP2040 |
| Microcontroller | Raspberry Pi RP2040 |
| Processor | Dual-core ARM Cortex-M0+ |
| Ethernet Controller | WIZnet W5500 |
| Ethernet Speed | 10/100 Mbps |
| Ethernet Connector | HR911105A |
| External Flash | 16MB QSPI |
| USB Interface | USB Type-C |
| Input Voltage | 5V USB |
| Operating Logic Voltage | 3.3V |
| Expansion | I²C / UART / GPIO |
| EDA | EasyEDA Pro |
| PCB Layers | As per Gerber design |

## Potential Applications

NetCore RP2040 can serve as a hardware foundation for:

- Ethernet-enabled IoT devices.
- Embedded web servers.
- Network-connected monitoring systems.
- Industrial communication interfaces.
- Ethernet-based control applications.
- TCP/IP networking experiments.
- Compact embedded gateways.

## Development Tools

- **EDA Software:** EasyEDA Pro
- **Microcontroller:** Raspberry Pi RP2040
- **Ethernet Controller:** WIZnet W5500
- **Hardware Documentation:** Schematic, BOM and Gerber files
- **PCB Manufacturing:** Standard FR4 PCB fabrication

## License

This project is distributed under the **MIT License**.

See the [LICENSE](LICENSE) file for details.

## Author

**Parth Biswas**

Embedded Systems & PCB Design Engineer

Interested in embedded hardware development, PCB design, Ethernet networking, IoT and industrial electronics.

---

<p align="center">
  <b>NetCore RP2040</b>
  <br>
  <i>Compact Hardware. Connected Possibilities.</i>
</p>
