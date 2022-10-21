# TCP/IP UDP Client Server

The UDP Client Server configuration demonstrates creating a network client and a network server that uses the MPLAB Harmony UDP API. This demonstration shows how the UDP/IP loopback works and it is a combination of the TCP/IP UDP Client and TCP/IP UDP Server application.

**TCP/IP UDP Client Server MHC Configuration**

The following Project Graph diagram shows the Harmony components included in this application demonstration.

-   MHC is launched by selecting **Tools \> Embedded \> MPLAB® Harmony 3 Configurator** from the MPLAB X IDE, demo project is ready to be configured and regenerated.

-   **TCP/IP Root Layer Project Graph**

    The root layer project shows that FLEXCOM1 peripheral is selected to do read and write operation for TCP/IP commands.

    This is the basic configuration with SYS\_CONSOLE, SYS\_DEBUG and SYS\_COMMAND modules. These modules are required for TCP/IP command execution.

    ![tcpip_samrh71_project](../../docs/GUID-207FD930-4C65-4FCF-8DCD-D9878F681DE0-low.png)

-   **TCP/IP Required Application**

    TCP/IP demo use these application module components for this demo.

    **Announce** module to discover the Microchip devices within a local network.

    **DHCP Client** module to discover the IPv4 address from the nearest DHCP Server.

    **DNS Client** provides DNS resolution capabilities to the stack. During these components selection, the required transport and network modules are also selected.

    ![tcpip_samrh71_project](../../docs/GUID-FE61D479-C73B-4428-8E3B-A1329D5C608E-low.png)

-   **TCPIP Driver Layer**

    **Internal ethernet driver\(GMAC\)** is enabled with the external **KSZ8061 PHY driver** library.

    ![tcpip_samrh71_project_driver](../../docs/GUID-53EC3088-7D72-48E5-9C2A-AECE32A67AB0-low.png)

    The MIIM Driver supports asynchronous read/write and scan operations for accessing the external PHY registers and notification when MIIM operations have completed.


**TCP/IP UDP Client Server Hardware Configuration**

This section describes the required default hardware configuration for SAM RH71 Evaluation Kit that can be used for the respective application demonstration.

-   For initial setup, you can refer to the [Getting Started with SAMRH71F20 Evaluation Kit](https://ww1.microchip.com/downloads/en/AppNotes/Getting_Started_with_the_SAMRH71_Microcontroller_DS00003213C.pdf) application note.

-   Set all SW5 DIP Switch to 0.

-   Connect the micro USB cable from the computer to the J15 USB connector on the SAM RH71 Evaluation Kit

-   Establish a connection between the router/switch with the SAM RH71 Evaluation Kit through the RJ45 connector

    ![required_hardware](../../docs/GUID-8B619CD8-65FE-464A-97AC-74560E0CDE8F-low.png)


**TCP/IP UDP Client Server Running Application**

**MPLAB X IDE Project**

This table list the name and location of the MPLAB X IDE project folder for the demonstration.

|Project Name|Target Device|Target Development Board|Description|
|------------|-------------|------------------------|-----------|
|sam\_rh71\_ek.X|ATSAMRH71F20C|SAMRH71F20-EK|Demonstrates the Berkeley UDP Client Server on development board with ATSAMRH71F20C device. This implementation is based on Bare Metal \( non-RTOS\).|

**Demonstration Commands**

There are three sequential commands implemented in this demonstration.

1.  **setopt** < hostname \> < port \> < message \> - This command specifies the following parameters for the UDP packet: Destination IP Address or Host name, Destination Port and Message to transfer

2.  **getopt** - This command displays the current options

3.  **sendudp** - This command sends a UDP packet


**Running The Demonstration**

1.  Build and download the demonstration project on the target board.

2.  Connect the board UART connection:

    1.  A virtual COM port will be detected on the computer, when the USB cable is connected to USB-UART connector.

    2.  Open a standard terminal application on the computer \(like Hyper-terminal or Tera Term\) and configure the virtual COM port.

    3.  Set the serial baud rate to 115200 baud in the terminal application.

    4.  See that the initialization prints on the serial port terminal.

    5.  When the DHCP client is enabled in the demonstration, wait for the DHCP server to assign an IP address for the development board. This will be printed on the serial port terminal.

        -   Alternatively: Use the Announce service or ping to get the IP address of the board.

            -   Run **tcpip\_discoverer.jar** to discover the IPv4 and IPv6 address for the board.

3.  Execution:

    1.  Set the UDP packet options by typing **setopt** at the terminal console.

    2.  Verify the UDP packet settings by typing **getopt** at the terminal console.

    3.  Send the UDP packet to the destination using the **sendudp** command.

    4.  After the **sendudp** command is input, the demonstration will make a DNS query to look up the host name and send a UDP packet to that host.

    5.  The output message will be received by the UDP server on the port that is configured by the command **setopt**.

4.  Testing the UDP Server part of demonstration:

    1.  As soon as a valid IP address is assigned through the DHCP to the demonstration, it is ready to accept a UDP/IP connection on port 9760.

    2.  Send a UDP packet to the IP address of the hardware board and port 9760 from any UDP Client application running on the computer \(SocketTest, Packet Sender etc\).

    3.  The UDP Server demonstration running on the evaluation kit will echo back everything it receives along the connection.


**Parent topic:**[Harmony 3 TCP/IP Application for SAM RH71 Family](GUID-9F654EF7-6F64-4E62-98D9-7F1BDF366DE8.md)

