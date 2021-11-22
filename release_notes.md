---
title: Release notes
nav_order: 99
---

![Microchip logo](https://raw.githubusercontent.com/wiki/Microchip-MPLAB-Harmony/Microchip-MPLAB-Harmony.github.io/images/microchip_logo.png)
![Harmony logo small](https://raw.githubusercontent.com/wiki/Microchip-MPLAB-Harmony/Microchip-MPLAB-Harmony.github.io/images/microchip_mplab_harmony_logo_small.png)

# Microchip MPLAB® Harmony 3 Release Notes

## Harmony 3 Network application examples for SAMRH71 family v3.8.0

### Development kit and demo application support

Following table provides number of peripheral library examples available for different development kits.

| Development Kits  | MPLABx applications |
|:-----------------:|:-------------------:|
| SAM RH71 Evaluation Kit | 13 |

### New Features

- Added application examples for SAMRH71 evaluation kit:
    - Berkeley TCP Client
    - Berkeley TCP Server
    - Berkeley UDP Client
    - Berkeley UDP Server
    - Berkeley UDP Relay
    - IPERF Demo
    - TCP Client
    - TCP Client Server
    - Client Server
    - TCP Server
    - UDP Client
    - UDP Server
    - UDP Client Server

### Known Issues

- IPERF demo:
    - Example overwrite MH3 generated code to get maximum performances with the product:
        - Application code is relocated at startup to be executed in RAM.
        - Cache maintenance operation is modified to execute less instructions (only one global cache maintenance for all received packets).

### Development Tools

- [MPLAB® X IDE v5.50](https://www.microchip.com/mplab/mplab-x-ide)
- MPLAB® X IDE plug-ins:
  - MPLAB® Harmony Configurator (MHC) v3.8.0
- [MPLAB® XC32 C/C++ Compiler v3.01](https://www.microchip.com/mplab/compilers)

### Dependent Components

* [CSP v3.10.0](https://github.com/Microchip-MPLAB-Harmony/csp/releases/tag/v3.10.0)
* [dev_packs v3.10.0](https://github.com/Microchip-MPLAB-Harmony/dev_packs/releases/tag/v3.10.0)
* [Core v3.10.0](https://github.com/Microchip-MPLAB-Harmony/core/releases/tag/v3.10.0)
* [BSP v3.10.0](https://github.com/Microchip-MPLAB-Harmony/bsp/releases/tag/v3.10.0)
* [Crypto v3.7.3](https://github.com/Microchip-MPLAB-Harmony/crypto/releases/tag/v3.7.3)
* [Net v3.7.4](https://github.com/Microchip-MPLAB-Harmony/net/releases/tag/v3.7.4)
* [Wolfssl v4.7.0](https://github.com/Microchip-MPLAB-Harmony/wolfssl/releases/tag/v4.7.0)
* [CMSIS-FreeRTOS v10.3.1](https://github.com/Microchip-MPLAB-Harmony/CMSIS-FreeRTOS/releases/tag/v10.3.1)

## Harmony 3 Network application examples for SAMRH71 family  v3.7.0

### Demonstration Applications
There are no applications for SAMRH71 added to this release.



### Development Tools

- [Harmony net repository, 3.7.0](https://github.com/Microchip-MPLAB-Harmony/net/tree/v3.7.0)
