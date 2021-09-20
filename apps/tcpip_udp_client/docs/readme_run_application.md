---
grand_parent:  Harmony 3 TCP/IP Application for SAM RH71 Family
parent: TCP/IP UDP Client
title: Running Application
nav_order: 3
has_children: false
has_toc: false
---
[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# TCP/IP UDP Client Running Application

## MPLAB X IDE Project
This table list the name and location of the MPLAB X IDE project folder for the demonstration.

|Project Name|  Target Device|  Target Development Board | Description  |
|:-------------:|:---------:|:---------:|:---------:|
|sam_rh71_ek.X | ATSAMRH71F20C | SAMRH71F20-EK | Demonstrates the Berkeley UDP Client on development board with ATSAMRH71F20C device. This implementation is based on Bare Metal ( non-RTOS).  |

## Running The Demonstration

1. Configure the Development Board as given  **[Configure Hardware](readme_hardware_configuration.md)**.

2. Make the demonstration setup as shown [Network Setup](../../readme.md).

3. Build and download the demonstration project on the target board.

4. Connect the board UART connection:

    1. A virtual COM port will be detected on the computer, when the USB cable is connected to USB-UART connector.

    2. Open a standard terminal application on the computer (like Hyper-terminal or Tera Term) and configure the virtual COM port.

    3. Set the serial baud rate to 115200 baud in the terminal application.

    4. See that the initialization prints on the serial port terminal.

    5. When the DHCP client is enabled in the demonstration, wait for the DHCP server to assign an IP address for the development board. This will be printed on the serial port terminal.

		* Alternatively: Use the Announce service or ping to get the IP address of the board.

        * Run **tcpip_discoverer.jar** to discover the IPv4 and IPv6 address for the board.

5. Execution:

    **setopt**, **getopt** and **sendudp** are the UDP client APP commands.

	* For UDP Client test, the UDP Server application is required to run on the computer (SocketTest, Packet Sender etc). This demonstration is tested with **SocketTest v3.0(http://sockettest.sourceforge.net/)**.

    * Set the UDP packet options by typing **setopt** at the terminal console.
    
    * Verify the UDP packet settings by typing **getopt** at the terminal console. 

    * Open UDP Server application (**SocketTest** software) and select UDP server for the configured port number as per the command **setopt**.
    
    * Send the UDP packet to the destination using the **sendudp** command.
    
    * After the **sendudp** command is input, the demonstration will make a DNS query to look up the host name and send a UDP packet to that host. 
    
    * The output message will be received by the UDP server on the port that is configured by the command **setopt**.

