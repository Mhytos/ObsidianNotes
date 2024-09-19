#drecksSiemens 
*Erkläre die Grundlagen der IP Adressierung*
**Understanding IP Addresses and How a PC Gets One**

An **IP address** (Internet Protocol address) is a unique numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves two main purposes:

1. **Identification**: Distinguishes one device from another on a network.
2. **Location Addressing**: Helps route traffic between devices by providing their location in the network.

### **Types of IP Addresses**

- **IPv4 Addresses**: Consist of four numbers separated by periods (e.g., `192.168.1.1`), with each number ranging from 0 to 255.
- **IPv6 Addresses**: A newer format using eight groups of hexadecimal numbers separated by colons (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`), designed to provide a larger address pool.

### **How a PC Gets an IP Address**

1. **Dynamic Assignment via DHCP**
    
    - **DHCP (Dynamic Host Configuration Protocol)** servers automatically assign IP addresses to devices on a network.
    - When your PC connects to a network, it sends a request to the DHCP server.
    - The DHCP server responds by assigning an available IP address for a specific lease duration.
    - This is the most common method for home and office networks.
2. **Static IP Assignment**
    
    - An IP address is manually set on the PC's network settings.
    - Used when a fixed IP address is necessary, such as for servers or network printers.
    - Ensures the device's IP address doesn't change over time.
3. **Automatic Private IP Addressing (APIPA)**
    
    - If a PC can't find a DHCP server, it assigns itself an IP address in the range `169.254.0.1` to `169.254.255.254`.
    - Allows communication with other devices on the same network segment that also use APIPA.
    - Does not provide internet access.

### **Summary**

- **IP Addresses** are essential for network communication, acting like mailing addresses for devices.
- **Dynamic IPs** are assigned automatically and can change over time.
- **Static IPs** are manually configured and remain constant.
- Most devices get their IP addresses dynamically from a **DHCP server**, which could be a router in home networks.

---
![[Pasted image 20240919094038.png]]
![[Pasted image 20240919094304.png]]
