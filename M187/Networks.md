#drecksSiemens #dns 
[[Netzwerkkonzepte]]
[[Networkcomponents]]

# Peer-to-Peer
- In a P2P network, there is no central server. Each node (peer) in the network can act as a client and a server. This means that participants can request services from other participants and may also provide services to the other participants.
- All nodes share resources like files, bandwidth or processing power directly with one another. So there is no need for a central server to manage the resources.
- Examples for P2P are BitTorrent (whaaaat, never heard of that)
- P2P networks are more scalable, as the network's capacity increases with more users joining.
- P2P network are very reliable and resistant to failure. If one peer goes down, the network can often still function without it.
- Security is something that might be harder to implement in P2P networks. Each peer must be trusted to some extent. It's much more difficult to control each new user and filter out the malicious users
---
# Client-Server
- In a client-server-network there is a central server that manages resources and services. Clients (users) request resources from the server, which controls and provides access.
- The server stores and controls resources (data, files, services) and clients access these resources through the server. This allows vor more efficient management of shared resources, as the server can control who has access, enforce security and handle large-scale data storage.
- Example are Pretty much all websites and web-services
- They can be scaled vertically, which means increasing the capacity of the server, or horizontally by adding more servers. But the central server might also become a bottleneck
- If the server crashes, the entire network may go down since clients rely on the server to access resources
- Enforcing security policies are easier to enforce. It's also easier to manage user permission and secure sensitive data.
---

| Aspect | Peer-to-Peer Networks | Client-Server Networks |
| ------ | --------------------- | ---------------------- |

|   |   |   |
|---|---|---|
|**Control**|Decentralized (each peer is equal)|Centralized (server controls network)|

|   |   |   |
|---|---|---|
|**Role of Devices**|Devices act as both clients and servers|Clients request resources from servers|

|   |   |   |
|---|---|---|
|**Scalability**|Highly scalable as more peers join|Limited by server capacity|

|   |   |   |
|---|---|---|
|**Reliability**|More resilient to single points of failure|More dependent on server stability|

|              |                                          |                                      |
| ------------ | ---------------------------------------- | ------------------------------------ |
| **Security** | Harder to secure (every peer is trusted) | Easier to secure (central authority) |

---

# Severdienste

![[Pasted image 20240919095604.png]]


![[Pasted image 20240919095814.png]]

![[Pasted image 20240919095943.png]]
