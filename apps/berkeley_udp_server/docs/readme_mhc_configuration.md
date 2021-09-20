---
grand_parent:  Harmony 3 TCP/IP Application for SAM RH71 Family
parent: TCP/IP Berkeley UDP Server
title: MHC Configuration
nav_order: 1
has_children: false
has_toc: false
---
[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# TCP/IP Berkeley UDP Server MHC Configuration

The following Project Graph diagram shows the Harmony components included in the UDP Server demonstration application.

* MHC is launched by selecting **Tools > Embedded > MPLAB® Harmony 3 Configurator** from the MPLAB X IDE, demo project is ready to be configured and regenerated.

* **TCP/IP Root Layer Project Graph**

  The root layer project shows that FLEXCOM1 peripheral is selected to do read and write operation for TCP/IP commands. 

  This is the basic configuration with SYS_CONSOLE, SYS_DEBUG and SYS_COMMAND modules. These modules are required for TCP/IP command execution.

  ![tcpip_samrh71_project](images/tcpip_default_required_root_rh71.png)

* **TCP/IP Required Application**

  TCP/IP demo use these application module components for this demo. **Announce** module to discover the Microchip devices within a local network.
  
  **DHCP Client** module to discover the IPv4 address from the nearest DHCP Server.
  
  **DNS Client** provides DNS resolution capabilities to the stack. 
  
  **Berkeley API**  module provides the Berkeley_Socket_Distribution (BSD) wrapper to the native Microchip TCP/IP Stack APIs. During this component selection, the required transport and network modules are also selected.

    ![tcpip_samrh71_project](images/tcpip_berkeley_tcp_demo_app.png)

* **TCPIP Driver Layer** 

  **Internal ethernet driver(GMAC)** is enabled with the external **KSZ8061 PHY driver** library. 

    ![tcpip_samrh71_project_driver](images/tcpip_driver_component_rh71.png)

  The MIIM Driver supports asynchronous read/write and scan operations for accessing the external PHY registers and notification when MIIM operations have completed.

