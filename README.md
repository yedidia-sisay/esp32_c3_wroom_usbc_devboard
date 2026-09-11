# ESP32-C3 Custom Development Board

A custom ESP32-C3 development board designed from the ground up in **KiCad**, covering schematic design, component selection, PCB layout, and routing.

The board is built around the **ESP32-C3-WROOM-02** and provides USB-C connectivity, regulated 3.3 V power, programming/debugging interfaces, GPIO expansion, and basic user controls.

## Overview

The goal of this project was to design a practical, compact ESP32-C3 development board rather than relying on an off-the-shelf development board.

The design integrates the ESP32-C3 module with the supporting power, USB, reset, boot, programming, and expansion circuitry required for a usable development platform.

## Features

* **ESP32-C3-WROOM-02** module
* **USB-C** connector
* USB 2.0 D+ / D− connectivity
* USB-C CC resistors
* USB ESD/TVS protection
* **5 V USB input**
* **3.3 V regulated supply**
* AP2112K-3.3 LDO
* Reset / CHIP_PU circuitry
* Boot-mode control
* User/status LED
* GPIO expansion headers
* Dedicated JTAG/UART access
* Exposed 3.3 V, 5 V, and GND connections
* Custom PCB layout and routing




## Hardware

### Main MCU

The board uses the **Espressif ESP32-C3-WROOM-02** module.

The module provides the main processing, USB connectivity, GPIO, UART, and debugging interfaces for the board.

The schematic exposes the ESP32-C3 GPIOs through headers so the board can be used for firmware development and hardware experimentation.

### USB-C

USB-C is used as the primary connection to the board.

The USB interface includes:

* VBUS power input
* USB D+
* USB D−
* CC1 / CC2 configuration resistors
* USB ESD/TVS protection
* Shield connection

The USB data lines connect directly to the ESP32-C3's native USB interface.

### Power

The board accepts **5 V from USB-C**.

A dedicated **AP2112K-3.3 LDO** generates the 3.3 V rail used by the ESP32-C3 and associated circuitry.
Decoupling capacitors are included around the power circuitry and ESP32-C3 supply.

### Reset and Boot

The board includes dedicated push buttons and supporting resistors for:

* ESP32 reset / CHIP_PU
* Boot-mode selection

This allows the module to be manually reset and placed into the required boot mode during firmware development.

### Programming and Debugging

The design exposes the ESP32-C3's programming/debugging signals through dedicated headers.

Interfaces available on the board include:

* UART
* JTAG
* GPIO
* 3.3 V
* 5 V
* GND

### GPIO Expansion

Two multi-pin headers provide access to the ESP32-C3 GPIOs.

This allows external sensors, peripherals, and prototype circuits to be connected without modifying the main PCB.

## PCB Design

The schematic and PCB were designed in **KiCad 10**.

The PCB design process included:

1. Component selection
2. Schematic capture
3. Electrical connectivity definition
4. Component footprint assignment
5. PCB placement
6. Power and signal routing
7. USB routing
8. Ground-plane implementation
9. Design-rule checking
10. Final PCB routing

The design was developed with the intention of producing a physically usable development board rather than being purely a schematic exercise.

# Project Status

**Hardware design completed.**

The schematic and PCB routing have been completed. The next stage is hardware fabrication and bring-up, followed by firmware testing and validation of the USB, power, GPIO, and programming interfaces.
## Author

**Yedidia Sisay**

Electrical Engineering | Embedded Systems | PCB Design

