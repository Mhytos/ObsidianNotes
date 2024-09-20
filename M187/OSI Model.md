![[Pasted image 20240919132910.png]]
*here a little overview of protocols in general*
![[Pasted image 20240919135615.png]]
*here we see the OSI Model in action (I think)*
*going to get the higher quality version of this pic*
*red is pc to pc*
*blue is a lvl 2 switch*
*green is a lvl 3 switch/ router*
___
# OSI 

The OSI (Open Systems Interconnection) Model is a conceptual framework used to understand and implement network protocols in seven distinct layers. Each layer serves specific functions and communicates with the layers directly above and below it.

1. **Layer 1: Physical Layer**
    
    - **Function**: Transmits raw bitstreams over a physical medium (e.g., cables, radio waves).
    - **Devices**: Hubs, Repeaters, Network Cables.
    - **Example**: Ethernet cables, Wi-Fi signals.
2. **Layer 2: Data Link Layer**
    
    - **Function**: Ensures error-free data transfer between adjacent network nodes. It is responsible for MAC addresses and frames.
    - **Devices**: Switches, Bridges.
    - **Example**: MAC addressing, Ethernet frame transmission.
3. **Layer 3: Network Layer**
    
    - **Function**: Handles logical addressing and routing, determining the best path for data packets to travel across networks.
    - **Devices**: Routers, Layer 3 Switches.
    - **Example**: IP addressing, Routing protocols like OSPF, BGP.
4. **Layer 4: Transport Layer**
    
    - **Function**: Provides reliable data transfer services to the upper layers, including error checking and flow control. It uses protocols like TCP and UDP.
    - **Devices**: Gateways, Firewalls.
    - **Example**: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).
5. **Layer 5: Session Layer**
    
    - **Function**: Manages sessions or connections between applications, maintaining them and ensuring data exchange is synchronized.
    - **Example**: RPC (Remote Procedure Call), SQL sessions.
6. **Layer 6: Presentation Layer**
    
    - **Function**: Translates data between the application layer and the network, handling data encryption, compression, and formatting.
    - **Example**: Data encryption (SSL/TLS), Character encoding (ASCII, EBCDIC).
7. **Layer 7: Application Layer**
    
    - **Function**: Provides network services directly to end-users or applications, such as web browsers and email clients.
    - **Example**: HTTP (HyperText Transfer Protocol), FTP (File Transfer Protocol), SMTP (Simple Mail Transfer Protocol).

### Sources

1. **Cisco OSI Model Explanation**: Comprehensive breakdown of each OSI layer and its functionalities.
    
    - Cisco OSI Model
2. **CompTIA Network+ Guide**: Detailed explanations and practical applications of the OSI model.
    
    - [CompTIA Network+ OSI Model](https://www.comptia.org/)
3. **Wikipedia - OSI Model**: General information on the OSI model structure and layers.
    
    - [Wikipedia OSI Model](https://en.wikipedia.org/wiki/OSI_model)

---
