
# Configuring IP Addresses

This repository contains a Cisco Packet Tracer exercise focused on configuring router interfaces, assigning IP addresses, and testing connectivity between PCs. The exercise covers basic network configuration tasks using Cisco's Packet Tracer.

## Objective

The objective of this exercise is to practice the following tasks:
1. Configuring the hostname of a router.
2. Viewing router interface details using Cisco IOS commands.
3. Assigning IP addresses to router interfaces and enabling them.
4. Verifying the configuration and status of router interfaces.
5. Saving the router's running configuration.
6. Configuring IP addresses on PCs.
7. Testing network connectivity by pinging between PCs.

## Instructions

### 1. Configure R1's Hostname
1. Access the CLI of R1 in Packet Tracer.
2. Enter the following commands to set the hostname:
   ```bash
   enable
   configure terminal
   hostname R1
### 2. View R1's Interfaces
- Use the following command to view a list of R1's interfaces, their IP addresses, status, and other details:
    ```bash
    show ip interface brief
### 3. Configure IP Addresses on R1's Interfaces
- Enter the interface configuration mode for each interface and assign the appropriate IP addresses. 
    ```bash
    configure terminal
    interface GigabitEthernet0/0
    ip address 15.255.255.254 255.0.0.0
    no shutdown
    description ## to SW1 ##
    exit

    interface GigabitEthernet0/1
    ip address 182.98.255.254 255.255.0.0
    no shutdown
    description ## to SW2 ##
    exit

    interface GigabitEthernet0/2
    ip address 201.191.20.254 255.255.255.0
    no shutdown
    description ## to SW3 ##
    exit

### 4. Verify R1's Interfaces
- Use the following command to verify the interfaces have been configured correctly:

    ```bash
    show ip interface brief

### 5. View and Save the Running Configuration
- Use the following command to view the running configuration and confirm your changes:
    ```bash
    show running-config
- Save the configuration to NVRAM with the following command:
    ```bash
    copy running-config startup-config
### 6. Configure IP Addresses on PC1, PC2, and PC3
- In Packet Tracer, click on each PC and go to the Desktop tab.
- Click on IP Configuration.
- Set the IP address, subnet mask, and default gateway as appropriate for each PC.
### 7. Test Connectivity
- On PC1, open the Command Prompt and ping PC2:
    ```bash
    ping 182.98.0.1
- Ping PC3 from PC1 to ensure connectivity:
    ```bash
    ping 201.191.20.1
### Files Included
- The Packet Tracer file for this exercise.
## Acknowledgements


Special thanks to **Jeremy's IT Lab** for providing valuable resources and tutorials that greatly contributed to the completion of this exercise. His in-depth explanations and practical demonstrations have been instrumental in enhancing my understanding of Cisco networking concepts and the effective use of Packet Tracer.

For more information and additional resources, visit [Jeremy's IT Lab](https://jeremysitlab.com/) and check out his YouTube for the full course, [Jeremy's IT Lab Free CCNA 200-301 | Complete Course](https://www.youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ)
