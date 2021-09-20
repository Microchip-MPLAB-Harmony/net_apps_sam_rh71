---
parent: Harmony 3 TCP/IP Application for SAM RH71 Family
title: TCP/IP Berkeley UDP Relay
has_children: true
has_toc: false
---
[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# TCP/IP Berkeley UDP Relay

The Berkeley UDP Relay configuration demonstrates the use of multiple sockets for both sending and receiving. There are three different sub-functions of this application: 

* UDP Relay, which accepts UDP packets on one socket, and sends the packets out on a different socket 
* UDP Relay Client, which generates UDP traffic that is compatible with the UDP Relay Server 
* UDP Relay Server, which receives and checks traffic for a packet count and reports is any packets are dropped 



## Development kits
The following table provides links to the documentation to the TCP/IP Berkeley UDP Relay Application on SAM RH71 family.


| Development Kit |
|:---------|
|[SAM RH71 Evaluation Kit MHC Configuration](docs/readme_mhc_configuration.md) |
|[SAM RH71 Evaluation Kit Hardware Configuration](docs/readme_hardware_configuration.md) |
|[SAM RH71 Evaluation Kit Run Application](docs/readme_run_application.md) |
