---
grand_parent:  Harmony 3 TCP/IP Application for SAM RH71 Family
parent: TCP/IP TCP Client Server
title: MHC Configuration
nav_order: 1
has_children: false
has_toc: false
---
[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# TCP/IP TCP Client Server MHC Configuration

The following Project Graph diagram shows the Harmony components included in the TCP Client Server demonstration application.

* MHC is launched by selecting **Tools > Embedded > MPLAB® Harmony 3 Configurator** from the MPLAB X IDE, demo project is ready to be configured and regenerated.

* **TCP/IP Root Layer Project Graph**

  The root layer project shows that FLEXCOM1 peripheral is selected to do read and write operation for TCP/IP commands.

  This is the basic configuration with SYS_CONSOLE, SYS_DEBUG and SYS_COMMAND modules. These modules are required for TCP/IP command execution.

  ![tcpip_samrh71_project](images/tcpip_default_required_root_rh71.png)
  
  TCP sockets calculate the ISN using the wolfSSL crypto library. 


* **TCP/IP Required Application**

  TCP/IP demo use these application module components for this demo. 
  
  **Announce** module to discover the Microchip devices within a local network.
  
  **DHCP Client** module to discover the IPv4 address from the nearest DHCP Server.
  
  **DNS Client** provides DNS resolution capabilities to the stack. 
  

    ![tcpip_samrh71_project](images/tcpip_app_layer.png)

* **TCPIP Driver Layer**

  **Internal ethernet driver(GMAC)** is enabled with the external **KSZ8061 PHY driver** library. 

    ![tcpip_samrh71_project_driver](images/tcpip_driver_component_rh71.png)

  The MIIM Driver supports asynchronous read/write and scan operations for accessing the external PHY registers and notification when MIIM operations have completed.

