# CSE Interview: Networking & Security Questions
##  what is the difference between ssl and tls?
### answer:
TLS (Transport Layer Security) and SSL (Secure Sockets Layer) are cryptographic protocols for securing network communications. TLS is the modern, secure replacement for the deprecated SSL.

## Comparison Table

| Feature       | SSL (Deprecated)           | TLS (Current Standard)              |
|--------------|---------------------------|------------------------------------|
| **Versions** | SSL 2.0, 3.0              | TLS 1.0, 1.1, 1.2, 1.3             |
| **Security** | Vulnerable (POODLE, etc.) | More secure (AES, ECC, etc.)        |
| **Handshake**| Slower                    | Faster (especially TLS 1.3)         |
| **Usage**    | No longer supported       | Required for modern security        |

## Notes:
- **SSL is obsolete** and insecure (all versions should be disabled).
- **TLS 1.2 or 1.3** is the current security standard.
- TLS offers stronger encryption, faster handshakes, and better vulnerability protection.
## OSPF & Routing Protocols

### 1. In your own terms, describe what is the Border Gateway (BGP)?
- **Answer:** A Border Gateway (often referring to a BGP router) connects different autonomous systems (AS) on the internet, exchanging routing information between networks.

### 3. Which routing protocols depend only on Hop Count?
- **Answer:** RIP (Routing Information Protocol).

### 4. ARP request operates at which layer of OSI?
- **Answer:** **Layer 2 (Data Link Layer)**.

### 6. Why must all areas connect to Area 0 backbone in OSPF?
- **Answer:** Area 0 is the OSPF backbone that ensures loop-free routing by centralizing route distribution between non-backbone areas.

### 5. What is OSPF used for?
- **Answer:** OSPF (Open Shortest Path First) is a **link-state routing protocol** used to dynamically find the best path in an IP network.

### 7. Which protocol transmits username/password in clear text?
- **Answer:** **Telnet** (SSH/SFTP encrypt credentials).

### 8. What is MPLS?
- **Answer:** **Multiprotocol Label Switching (MPLS)** directs data using labels (not IP addresses) for faster routing in networks.

### 9. What is OSPF?
- **Answer:** A **link-state routing protocol** using Dijkstra’s algorithm to calculate the shortest path in an autonomous system (AS).

### 10. What is BGP?
- **Answer:** **Border Gateway Protocol (BGP)** is a path-vector protocol that manages routing between autonomous systems (AS) on the internet.

---

## Network Fundamentals
### Q1. What is the OSI model, and why is it important?
The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a communication system into seven layers: Physical, Data Link, Network, Transport, Session, Presentation, and Application. It is important because it helps network engineers understand how different protocols and technologies interact, troubleshoot issues, and design networks effectively.

### Q2. What is the difference between a router and a switch?
- **Router**: Operates at Layer 3 (Network Layer), connects different networks, routes traffic between them, and makes decisions based on IP addresses.  
- **Switch**: Operates at Layer 2 (Data Link Layer), connects devices within the same network, and forwards data based on MAC addresses.

### Q3. What is a subnet mask, and how does it work?
A subnet mask is a 32-bit number used to divide an IP address into network and host portions. It determines which part of the IP address identifies the network and which identifies the device. For example, in 192.168.1.0/24, the /24 indicates that the first 24 bits are the network portion.

## 2. Protocols and Technologies

### Q4. Explain the difference between TCP and UDP.
- **TCP (Transmission Control Protocol)**: Connection-oriented, reliable, ensures data delivery with error checking and retransmission. Used for applications like web browsing and email.  
- **UDP (User Datagram Protocol)**: Connectionless, faster, does not guarantee delivery. Used for real-time applications like video streaming and VoIP.

### Q5. What is DHCP, and how does it work?
DHCP (Dynamic Host Configuration Protocol) automatically assigns IP addresses and network configuration parameters (e.g., subnet mask, gateway, DNS) to devices on a network. It works via a four-step process: Discover, Offer, Request, and Acknowledgment (DORA).

### Q6. What is NAT, and why is it used?
NAT (Network Address Translation) maps private IP addresses to a public IP address, allowing multiple devices to share a single public IP. It conserves IPv4 addresses and enhances security by hiding internal IP addresses from external networks.

## 3. Troubleshooting

### Q7. How would you troubleshoot a network connectivity issue?
1. Check physical connections (cables, ports, LEDs).  
2. Verify IP configuration using `ipconfig` (Windows) or `ifconfig` (Linux).  
3. Ping the default gateway to check local connectivity.  
4. Ping an external IP (e.g., 8.8.8.8) to check internet access.  
5. Use `tracert` or `traceroute` to identify where the connection fails.  
6. Check firewall or ACL settings for restrictions.

### Q8. What is a MAC address, and how is it different from an IP address?
A MAC (Media Access Control) address is a unique identifier assigned to a network interface card (NIC) at the hardware level, operating at Layer 2 for communication within the same network. An IP address operates at Layer 3 and is used for communication across different networks.

## 4. Routing and Switching

### Q9. What is the difference between static and dynamic routing?
- **Static routing**: Manually configured routes on a router; simple and secure but not scalable for large networks.  
- **Dynamic routing**: Uses protocols like OSPF, EIGRP, or BGP to automatically update routing tables based on network changes; scalable but requires more configuration and resources.

### Q10. What is VLAN, and why is it used?
A VLAN (Virtual Local Area Network) is a logical segmentation of a network into smaller broadcast domains. It improves network performance, enhances security, and simplifies management by grouping devices based on function rather than physical location.

## 5. Security

### Q11. What is a firewall, and how does it work?
A firewall is a network security device that monitors and controls incoming and outgoing traffic based on predefined security rules. It can be hardware- or software-based and operates at Layer 3 (Network) or Layer 7 (Application).

### Q12. What is the difference between IDS and IPS?
- **IDS (Intrusion Detection System)**: Monitors network traffic for suspicious activity and alerts administrators but does not act.  
- **IPS (Intrusion Prevention System)**: Actively blocks or mitigates threats in real-time.

## 6. Practical Scenarios

### Q13. How would you configure a new network from scratch?
1. Plan the network topology and IP addressing scheme.  
2. Configure routers, switches, and firewalls.  
3. Set up VLANs and inter-VLAN routing if needed.  
4. Implement DHCP and DNS services.  
5. Configure security policies (ACLs, firewalls).  
6. Test connectivity and troubleshoot as needed.

### Q14. What would you do if a user cannot connect to the internet?
1. Verify the user’s IP configuration.  
2. Check if the user can ping the default gateway.  
3. Test DNS resolution by pinging a domain name (e.g., google.com).  
4. Inspect firewall or proxy settings.  
5. Check for network outages or misconfigurations.

## 7. Advanced Topics

### Q15. What is BGP, and how does it work?
BGP (Border Gateway Protocol) is a path-vector routing protocol that exchanges routing information between autonomous systems (AS) on the internet. It uses attributes like AS_PATH and NEXT_HOP to determine the best path for data.

### Q16. What is MPLS, and why is it used?
MPLS (Multiprotocol Label Switching) speeds up and shapes traffic flows in a network using labels for forwarding decisions, reducing complex routing lookups. It’s used in WANs for efficient traffic engineering.

### Q17. What is SDN, and how does it differ from traditional networking?
SDN (Software-Defined Networking) separates the control plane (decision-making) from the data plane (forwarding), centralizing management for dynamic, programmable configurations. Traditional networking has each device operate independently.

## 8. Behavioral Questions

### Q18. Describe a time when you resolved a complex network issue.
*(Tailor your answer to your experience)*  
Example: "I once resolved an issue where users in a remote office couldn’t access the corporate network. After analyzing the VPN configuration, I discovered a misconfigured ACL blocking traffic. I corrected the ACL, tested the connection, and documented the solution for future reference."

### Q19. How do you stay updated with the latest networking technologies?

### 20. Do ARP requests leave the local network?
- **Answer:** **No**, ARP is confined to the local broadcast domain (Layer 2).

### 21. What is ICMP? At which OSI layer?
- **Answer:** **Internet Control Message Protocol (ICMP)** operates at **Layer 3 (Network Layer)** (e.g., used by `ping`).

### 22. What is MTU?
- **Answer:** **Maximum Transmission Unit (MTU)** is the largest packet size (in bytes) allowed on a network path.

### 23. Which wavelength is associated with multimode fiber telecom equipment?
- **Answer:** **b. 850 nm** (also 1300 nm; single-mode uses 1310/1550 nm).

### 24. Which protocol does **not** use UDP as transport?
- **Answer:**  
  - ✅ **DNS** (can use UDP/TCP)  
  - ✅ **DHCP** (UDP)  
  - ❌ **SNMP** (uses UDP; your answer was incorrect).  

### 25. Which command identifies TCP connections?
- **Answer:** **`netstat -t`** (or `ss -t` on Linux).

### 26. Which command displays IP address?
- **Answer:** **`ipconfig`** (Windows) / `ifconfig` (Linux).

### 27. What is a MAC address?
- **Answer:** A **hardware address** (48-bit) assigned to a network interface (e.g., `00:1A:2B:3C:4D:5E`).

### 28. What format is `00:01:02:03:04:05`?
- **Answer:** **Colon-Hexadecimal** (also accepts hyphenated or dot notation).

### 29. Ping operates at which OSI layer?
- **Answer:** **Layer 3 (Network Layer)** (uses ICMP).

---

## IP Addressing & Subnetting

### 30. How to list all open TCP ports on localhost?
- **Answer:**  
  - Linux: `netstat -tuln` or `ss -tuln`  
  - Windows: `netstat -ano | findstr LISTENING`  

### 31. What are listening ports?
- **Answer:** Ports actively accepting incoming connections (e.g., `0.0.0.0:22` for SSH).

### 32a. Command to list all open ports on localhost?
- **Answer:** `netstat -tuln` (Linux) or `netstat -ano` (Windows).

### 33. Class C IP address `192.168.0.0` – how many hosts?
- **Answer:** **254 hosts** (2^8 – 2 = 254; excludes network/broadcast).

### 34. Which IP cannot be routed?
- **Answer:** **10.255.200.200** (private IP; non-routable on the public internet).

### 35. Is `196.16.144.99/23` a valid host address?
- **Answer:**  
  - **Network:** `196.16.144.0`  
  - **Broadcast:** `196.16.145.255`  
  - **Usable Hosts:** 510 (2^9 – 2).  

### 36. Is `196.16.1.103/26` a broadcast address?
- **Answer:**  
  - **Network:** `196.16.1.64`  
  - **Broadcast:** `196.16.1.127` → **No**, `.103` is a host address.  

### 37. How to trace the path to a domain?
- **Answer:** **`tracert` (Windows) / `traceroute` (Linux)**.

### 38. Given `192.168.3.6/22`:  
   - **Network:** `192.168.0.0`  
   - **Broadcast:** `192.168.3.255`  
   - **1st Host:** `192.168.0.1`  
   - **Last Host:** `192.168.3.254`  

### 39. Non-routable IP example?
- **Answer:** **`172.16.0.1`** (private range; rejected by public routers).

### 40. Command to resolve routing table?
- **Answer:** **`route -n` (Linux) / `route print` (Windows)**.

---

## Security

### 41. Safest way to send data to the cloud?
- **Answer:** **a. VPN** (encrypts all traffic) and **b.
**--------------------------------------------------------------**

  # Cisco BGP Interview Questions (CCNA Focus)

## 1. What is BGP in CCNA?
**Answer:**  
Border Gateway Protocol (BGP) is the routing protocol of the Internet. Key features:
- Largest routing protocol globally.
- Manages trusted/untrusted routes.
- Routes through **Autonomous Systems (AS)** rather than individual routers.
- Slowest convergence among routing protocols.
- Primarily used by ISPs and enterprises.

---

## 2. How does BGP work?
**Answer:**  
**Peering Session:**  
1. Routers establish a BGP peering session (TCP port 179).  
2. Exchange routing tables.  

**Process Steps:**  
- Searches routes in **External BGP (eBGP)** neighbors.  
- Checks **Internal BGP (iBGP)** within its AS.  
- Applies filters (policies, attributes).  
- Selects **best path** → Installs in RIB (Routing Information Base).  
- Advertises best path to eBGP neighbors.  

**Sub-processes:**  
- **BGP "In":** Receives paths, flags best path in BGP table.  
- **BGP "Out":** Shares best path with peers.  

---

## 3. What does BGP mean in networking?
**Answer:**  
- BGP is the **"glue" of the Internet** – connects Autonomous Systems (AS).  
- Filters/modifies routes using policies (e.g., traffic engineering).  
- Without BGP, the Internet would lack inter-AS routing.  

---

## 4. Why is BGP used?
**Answer:**  
- **GPS for packets**: Finds optimal routes based on:  
  - Network node status.  
  - AS policies (cost, reliability).  
- Functions:  
  - Exchanges routing/reachability info between ASes.  
  - Uses **network prefix announcements** via BGP peers.  

---

## 5. Why use BGP over OSPF?
| **Feature**       | BGP                          | OSPF                         |
|-------------------|------------------------------|------------------------------|
| **Type**          | Inter-domain (path vector)   | Intra-domain (link-state)    |
| **Use Case**      | WAN, Internet redundancy    | LAN, data centers           |
| **Convergence**   | Slower                      | Faster                      |
| **Best For**      | Large networks, ISPs        | Enterprise internal routing |

**Key Reason:** BGP scales better for **Internet-wide routing**.

---

## 6. Is BGP faster than OSPF?
**Answer:**  
- ❌ **No**. OSPF converges faster (uses Dijkstra’s algorithm).  
- BGP prioritizes **path stability** over speed.  

---

## 7. What is the AD value of BGP?
**Answer:**  
- **eBGP:** `20`  
- **iBGP:** `200`  
- **OSPF:** `110` (lower AD = more preferred).  

---

## 8. What is OSPF used for?
**Answer:**  
- **Link-state protocol** for fast convergence.  
- Ideal for:  
  - Large/complex networks.  
  - Multi-site auto-updating routing tables.  
  - Enterprises (not Internet-scale).  

---

## 9. Do home routers use BGP?
**Answer:**  
- ❌ **No**. Home routers use default routes (ISP handles BGP).  
- BGP is for **AS-level routing** (ISPs/enterprises).  

---

## 10. Why is BGP not a routing protocol?
**Answer:**  
- **Misconception**: BGP *is* a routing protocol (path-vector type).  
- Distinction: Focuses on **policy-based routing** between ASes.  

---

## 11. OSPF LSA Types
| **Type** | **Name**               | **Description**                          |
|---------|------------------------|------------------------------------------|
| 1       | Router LSA            | Lists router’s direct links (intra-area).|
| 2       | Network LSA           | Generated by DR for multi-access nets.   |
| 3       | Summary LSA (ABR)     | Advertises routes between areas.         |
| 4       | ASBR Summary LSA      | Locates ASBR in other areas.             |
| 5       | External LSA (ASBR)   | Advertises external (e.g., BGP) routes.  |
| 7       | NSSA LSA              | Allows external routes in stub areas.    |

---

## 12. RIP vs OSPF vs EIGRP vs BGP
| **Protocol** | **Type**            | **Use Case**               |
|-------------|---------------------|----------------------------|
| RIP         | Distance-vector     | Legacy small networks.     |
| OSPF        | Link-state          | Enterprise LANs.           |
| EIGRP       | Hybrid (Cisco-only) | Fast-converging networks.  |
| BGP         | Path-vector         | Internet/ISP routing.      |

---

## 13. When should BGP *not* be used?
**Answer:**  
- **Single-homed networks** (only 1 ISP connection).  
- Small networks (use static routes/default gateway).  
- Low-resource devices (BGP is CPU/memory intensive).  

--------------------------------------------------------------------------------------------------------
# Palo Alto Firewall Interview Questions & Answers

## 1. What are the various deployment modes in Palo Alto?
In Palo Alto, you can choose from four deployment models: Tap mode, Virtual (V-Wire), Layer 2, and Layer 3.  
- **Tap mode deployment option**: Allows monitoring of traffic flow using a tap or switch SPAN/mirror port without infrastructure upgrades. Traffic is observed, not managed, as no security rules apply. Configure SPAN source/destination ports and enable Tap mode, assigning the tap interface to a security zone.  
- **Virtual (V-Wire) Deployment option**: Installs the firewall passively on a network segment, enabling traffic control and monitoring. Supports App-ID, User-ID, Content-ID, NAT, and decryption via Virtual Wire interfaces.  
- **Layer 2 deployment option**: Configures multiple interfaces in VLAN or virtual-switch mode, switching between network segments. Enhances security and visibility by analyzing traffic based on policies.  
- **Layer 3 deployment option**: Routes traffic between interfaces, each with its own IP address and security zone. The most common mode, directing traffic across multiple interfaces.

## 2. Is Palo Alto a stateful firewall?
Yes, Palo Alto is a stateful firewall. It tracks all traffic passing through it, matching it against sessions and cybersecurity policies to maintain state awareness.

## 3. What is the function of Palo Alto Focus?
Palo Alto Focus is a cloud-based threat intelligence service that identifies critical attacks and enables action without additional resources, enhancing threat response efficiency.

## 4. What is the Application Command Center (ACC)?
The Application Command Center (ACC) provides visibility into traffic patterns and actionable threat insights from firewall network logs.

## 5. Which command is used to check the firewall policy matching in Palo Alto?
To check firewall policy matching, use: Open the Palo Alto web browser > go to Test Security > Policy > Match from trust to untrust destination.

## 6. What are the various states of the HA Firewall?
HA Firewalls operate in:  
- **Active-Active**: Both firewalls handle traffic simultaneously.  
- **Active-Passive**: One firewall is active, the other on standby.  
- **Standby**: A backup state for failover readiness.  
- **Failed**: Indicates a malfunction requiring intervention. These states ensure redundancy, failover, load balancing, and continuous security.

## 7. What are the various URL filtering options?
URL filtering options include:  
- **Allow**: Permits access.  
- **Block**: Denies access.  
- **Monitor**: Logs access without blocking.  
- **Warn**: Alerts users before proceeding.  
- **Category-based restrictions**: Limits access by URL categories. These enhance security and enforce compliance.

## 8. What is the zone protection profile?
The zone protection profile safeguards against:  
- **Flood attacks**: SYN, ICMP, UDP, etc.  
- **Reconnaissance**: Port and host sweeps.  
- **Packet-based attacks**: Large ICMP and ICMP fragments. It ensures comprehensive network protection.

## 9. What are the types of protection used in Palo Alto?
Major protection types include:  
- **Zone protection profile**: Covers floods, reconnaissance, and packet-based attacks.  
- **Network tab protection**: Includes network profiles and zone protections configured under the Network tab.

## 10. What is the difference between virtual routers and virtual systems?
- **Virtual routers**: Layer 3 routing mechanisms within a firewall, managing routes to subnets via static or dynamic protocols (e.g., OSPF). Multiple VRs can exist, each with unique routes, and can be shared across VSYS.  
- **Virtual systems**: Logical firewall instances within a single device, each with its own interfaces, security policies, and admins. Supports virtual wire, Layer 2, or Layer 3 modes, enabling logical network separation.

## 11. What is a U-turn NAT?
A U-turn NAT allows users to access internal DMZ servers using the servers’ external IP addresses, creating a logical path for internal-to-external communication.

## 12. What is WAF (Web Application Firewall)?
A Web Application Firewall (WAF) monitors and secures web applications by filtering traffic between the Internet and the app. Features include:  
- Compensating for insecure coding.  
- Customizable behavior monitoring to block deviations.

## 13. What is Palo Alto’s architecture like?
Palo Alto’s next-generation firewalls use Single-Pass Parallel Processing (SP3) architecture, combining:  
- **Single Pass software**: Processes traffic once for all functions.  
- **Parallel Processing hardware**: Enhances throughput and reduces latency. This delivers high-performance security with low latency.

## 14. What are the benefits of Panorama in Palo Alto?
Panorama offers:  
- Centralized configuration and deployment.  
- Distributed administration for delegated firewall management.  
- Aggregated logging, reporting, and analysis.  
- Graphical network visualization.  
- Centralized traffic and security oversight.

## 15. What is the meaning of endpoint security?
Endpoint security protects devices (e.g., PCs, laptops, smartphones, servers, IoT) connected to a network from cyber threats and unauthorized access.

## 16. What are the different types of linkages used to establish HA or the HA introduction?
HA linkages include:  
- **HA1 (Control link)**: Manages synchronization.  
- **HA2 (Datalink)**: Transfers session data.  
- **Backup links**: Provide redundancy.  
- **Packet forwarding links**: Enable traffic continuity.

## 17. Which virtualization platforms fully support Palo Alto network deployments?
The VM-Series supports:  
- OpenStack, VMware, Cisco ACI, AWS, Google Cloud Platform, public/private clouds.

## 18. What is the default IP address, login, and password for Palo Alto Firewall’s administration port?
- **IP Address**: 192.168.1.1  
- **Username**: admin  
- **Password**: admin

## 19. That’s it! There are some Important Palo Alto firewall Interview Questions
These basic, intermediate, and advanced questions are ideal for Palo Alto interview preparation.

## 20. What are the different types of media supported by Palo Alto firewall support?
Supported media include:  
- Ethernet (copper/fiber), SFP/SFP+ modules, wireless via VPNs, SD-WAN, USB for logs, cloud connections (AWS, Azure, GCP), and virtual instances for hybrid environments.

## 21. What is the advantage of Palo Alto SP3 architecture?
SP3 enhances efficiency by:  
- Processing traffic in a single pass, reducing latency.  
- Integrating security functions in parallel for high throughput.  
- Supporting scalable, real-time threat prevention with minimal performance impact.
------------------------------------------------------------------------------------------------------------------------------------
# Network Engineer Interview Questions and Answers

## OSI (Open System Interconnect)

### 1. Explain OSI Layer?
The Open System Interconnect (OSI) model was developed by the International Organization for Standardization (ISO) and introduced in 1984. It consists of seven layers:  
- **Application Layer**: Provides an interface for users to interact with application or network services (e.g., web browsers).  
- **Presentation Layer**: Handles data formatting, encoding, and encryption.  
- **Session Layer**: Manages session establishment, maintenance, and termination.  
- **Transport Layer**: Ensures reliable data delivery between applications.  
- **Network Layer**: Manages logical addressing and routing.  
- **Data Link Layer**: Facilitates communication between the network layer and physical layer using MAC addresses.  
- **Physical Layer**: Defines electrical and mechanical specifications for device communication.

### 2. Which Layer is Responsible for Reliable Connection?
The **Transport Layer** guarantees a reliable end-to-end connection through mechanisms like error correction and flow control.

### 3. What are Different Protocols That Work at Each Layer in the OSI Model?
- **Application Layer**: HTTP (web browsing), Telnet (remote login).  
- **Presentation Layer**: Encoding/Decoding (e.g., AVI for video, WAV for voice, JPEG for graphics, ASCII for text), Encryption/Decryption.  
- **Session Layer**: Remote Procedure Call (RPC), AppleTalk Session Protocol (ASP).  
- **Transport Layer**: TCP (reliable, connection-oriented), UDP (fast, connectionless).  
  - **TCP vs. UDP**:  
    - TCP: Transmission Control Protocol, connection-oriented, supports acknowledgments, reliable, protocol number 6 (e.g., HTTP, FTP, SMTP).  
    - UDP: User Datagram Protocol, connectionless, no acknowledgments, unreliable, protocol number 17 (e.g., DNS, DHCP, TFTP).  
- **Network Layer**:  
  - **Routed Protocols**: Carry user data (e.g., IP).  
  - **Routing Protocols**: Determine paths (e.g., OSPF, RIP).  
- **Data Link Layer**: Uses MAC (Media Access Control) for reliable data transit across physical links (e.g., Ethernet).  
- **Physical Layer**: Specifies hardware standards (e.g., cables, connectors).

## Ports and Protocols

### 5. What is a Port Number and Give Some Examples?
A port number is a 16-bit integer in TCP/UDP headers that identifies a specific process on a server. Examples:  
- FTP (File Transfer Protocol): TCP 20 (data), 21 (control).  
- SSH (Secure Shell): TCP 22.  
- Telnet: TCP 23.  
- SMTP (Simple Mail Transfer Protocol): TCP 25.  
- DNS (Domain Name System): TCP/UDP 53.  
- DHCP (Dynamic Host Configuration Protocol): UDP 67 (server), 68 (client).  
- HTTP (Hypertext Transfer Protocol): TCP 80.  
- POP3 (Post Office Protocol): TCP 110.  
- NTP (Network Time Protocol): UDP 123.  
- SNMP (Simple Network Management Protocol): UDP 161/162.  
- HTTPS (HTTP Secure): TCP 443.

### 6. What is the Range of Port Numbers?
- **Well-Known Ports**: 0 to 1023 (e.g., HTTP, FTP).  
- **Registered Ports**: 1024 to 49151 (assigned by IANA for specific services).  
- **Open Ports**: 49152 to 65535 (dynamic or private use).

### 7. What is a Protocol Number and Give Some Examples?
A protocol number is a single-byte value in the IP header identifying the upper-layer protocol. Examples:  
- ICMP: 1  
- IGMP: 2  
- IPv4: 4  
- TCP: 6  
- EGP: 8  
- IGP: 9  
- UDP: 17  
- IPv6: 41  
- GRE: 47  
- EIGRP: 88  
- OSPF: 89  
- BGP: 179

### 8. What is Unicast, Multicast, and Broadcast?
- **Unicast**: One-to-one transmission (e.g., a single device to another).  
- **Multicast**: Group communication (e.g., one-to-many within a specific group).  
- **Broadcast**: One-to-all transmission (e.g., sent to all devices in a network).

### 9. What is the Difference Between Half-Duplex and Full-Duplex?
- **Half-Duplex**: Data flows in both directions but not simultaneously (e.g., hubs).  
- **Full-Duplex**: Data flows in both directions simultaneously (e.g., switches).

## Data Link Layer Concepts

### 10. What is the MAC Format?
A MAC address is a 48-bit (6-byte) hardware address written in hexadecimal format (e.g., 00:1A:2B:3C:4D:5E). It consists of:  
- **First 24 bits**: Organizationally Unique Identifier (OUI), assigned by IEEE.  
- **Last 24 bits**: Manufacturer-assigned code.

### 11. What is a Frame?
A frame is a data unit at the Data Link Layer, formatted with a header containing source and destination MAC addresses, encapsulating the network layer packet.

### 12. What is the TCP/IP Model?
The TCP/IP model is a four-layer standard:  
- **Application Layer**: Combines OSI Application, Presentation, and Session layers.  
- **Transport Layer**: Handles data delivery (TCP/UDP).  
- **Internet Layer**: Manages logical addressing and routing (IP).  
- **Network Access Layer**: Combines OSI Data Link and Physical layers.

### 13. What Protocols Are Included in Each Layer of the TCP/IP Model?
- **Application Layer**: DNS, DHCP, FTP, TFTP, SMTP, HTTP, Telnet, SSH.  
- **Transport Layer**: TCP, UDP.  
- **Internet Layer**: IP, ICMP, IGMP.  
- **Network Access Layer**: Ethernet, Token Ring, FDDI, X.25, Frame Relay, ARP, RARP.

## ARP (Address Resolution Protocol)

### 14. What is ARP?
Address Resolution Protocol (ARP) maps a network layer IP address to a data link layer MAC address, enabling communication within a network.

### 15. At Which Layer Does ARP Work and Why?
ARP operates at the **Data Link Layer (Layer 2)** because it is implemented by the network protocol driver and its packets are encapsulated in Ethernet headers.

### 16. What is an ARP Table (Cache)?
An ARP cache is a table storing IP-to-MAC address mappings created when an IP address is resolved. It aids efficient communication and can be exploited by attackers to hide behind fake IPs.

### 17. What is the Size of an ARP Request and ARP Reply Packet?
Both ARP request and reply packets are **28 bytes** in size.

### 18. What is Proxy ARP?
Proxy ARP occurs when one device responds to an ARP request on behalf of another device (e.g., Host C responds for Host B when Host A queries Host B’s IP).

### 21. What is Reverse ARP?
Reverse ARP (RARP) obtains a device’s IP address when its MAC address is known, typically used by diskless workstations.

### 22. What is Inverse ARP?
Inverse ARP dynamically maps local Data Link Connection Identifiers (DLCIs) to remote IP addresses in Frame Relay networks.

## TCP (Transmission Control Protocol)

### 23. What is Transmission Control Protocol (TCP)?
TCP is a reliable, connection-oriented protocol ensuring end-to-end data delivery in digital networks. It organizes data for transmission between a server and client, guaranteeing data integrity.

### 24. Explain the TCP Three-Way Handshake Process?
The TCP three-way handshake establishes a connection:  
1. **SYN**: Client sends a synchronization packet to initiate the connection.  
2. **SYN-ACK**: Server responds with a synchronization-acknowledgment packet.  
3. **ACK**: Client acknowledges, completing the connection setup.

### 25. What is the Purpose of the RST Bit?
The **RST (Reset)** bit resets a connection when it’s not allowed by the destination or encounters an error.

### 26. What are the TCP Flags?
TCP flags control data flow:  
- **PSH (Push)**: Pushes buffered data to the receiver immediately.  
- **RST (Reset)**: Resets the connection.  
- **FIN (Finish)**: Indicates no more data from the sender, ending the session.  
- **URG (Urgent)**: Marks data as high-priority.  
- **ACK (Acknowledgment)**: Confirms receipt of data (e.g., ACK=10 means expecting byte 10 next).  
- **SYN (Synchronize)**: Initiates a connection and synchronizes sequence numbers.

### 28. What is the Importance of Sequence Number and Acknowledgment Number?
- **Sequence Number**: A 32-bit field indicating the amount of data sent in a TCP session (0–4,294,967,295). Ensures reliable delivery as the receiver uses it in the next ACK.  
- **Acknowledgment Number**: Confirms receipt, set to the next expected byte (e.g., ACK=10 after receiving bytes 0–9).

### 29. What is the Importance of the Identification Field in IP Packets?
The identification field uniquely identifies fragmented packets, enabling the destination device to reassemble them in order.

## IP Packet Concepts

### 30. What is the MTU (Maximum Transmission Unit)?
The MTU is the largest packet or frame size (in bytes) that can be sent over a network. TCP uses the MTU to determine packet size for transmission.

### 31. What is Fragmentation?
Fragmentation breaks large IP packets into smaller fragments when they exceed the MTU of a link. Each fragment is transmitted independently and reassembled at the destination.

### 32. How is a Packet Reassembled?
Fragments are reassembled by the receiving host using the identification field, fragment offset, and flags in the IP header to reconstruct the original packet.

### 33. What is the Importance of DF and MF Flags?
- **DF (Don’t Fragment)**: If set, fragmentation is disallowed; the router discards oversized packets.  
- **MF (More Fragments)**: Indicates additional fragments follow (unset on the last fragment).

### 34. What is the Purpose of a Fragment Offset?
The fragment offset defines the position of a fragment relative to the start of the original packet, aiding reassembly.

### 35. What is the Importance of the TTL Value?
The **TTL (Time to Live)** limits a packet’s lifespan in the network, decrementing by 1 per hop. When it reaches 0, the packet is discarded to prevent routing loops. Typical values are 32 or 64.

## Routing

### 37. What is Routing?
Routing directs packets between networks that are not locally attached, determining the best path to the destination.

### 38. What is a Router?
A router is a Layer 3 device enabling communication between different logical networks by forwarding packets based on IP addresses.

### 39. What are the Different Types of Memory in a Router?
- **RAM**: Stores the running configuration (running-config).  
- **NVRAM**: Stores the startup configuration (startup-config).  
- **Flash Memory**: Stores the IOS (Internetwork Operating System).  
- **ROM**: Stores POST, bootstrap, and mini-IOS instructions.

### 40. What are the Possible Locations of an IOS Image?
- **Flash Memory**: Primary storage for the IOS.  
- **TFTP Server**: Alternative source for IOS backup or updates.

### 41. What are the Different Modes in a Router?
- **User Mode**: Limited monitoring commands (e.g., `enable`, `ping`, `traceroute`). Prompt: `Router>`.  
- **Privilege Mode**: Full monitoring and troubleshooting (e.g., `show`, `configure terminal`, `write`). Prompt: `Router#`.  
- **Global Configuration Mode**: Changes affect the entire device (e.g., `hostname`). Prompt: `Router(config)#`.

### 42. What is the Command to Reboot a Router?
`#reload`

### 43. What is the Command to Backup IOS to a TFTP Server?
`#copy flash tftp`

### 44. What is the Command to Copy Running Config to Startup Config?
`#copy running-config startup-config`

### 45. Define Static Routing?
Static routing involves manually configured routes by an administrator.  
- **Advantages**: Secure, reliable, faster, no bandwidth waste.  
- **Disadvantages**: No automatic updates, requires destination network ID, high administrative effort, suited for small networks.

### 46. What is a Default Route?
A default route is a fallback path for unknown destinations, directing all unmatched traffic (e.g., `0.0.0.0/0`) to a specified gateway.

### 47. What is Dynamic Routing?
Dynamic routing uses protocols (e.g., OSPF, EIGRP, BGP) to learn routes automatically from neighboring routers, adapting to network changes.

### 48. What is a Routed Protocol?
A routed protocol carries user data between networks (e.g., IP, IPX, AppleTalk), such as file transfers or web traffic.

### 49. What is a Routing Protocol?
A routing protocol determines the best paths between networks (e.g., EIGRP, OSPF, RIP), maintaining routing tables dynamically.

### 50. What is IGP?
An **Interior Gateway Protocol (IGP)** handles routing within a single autonomous system (e.g., RIP, EIGRP, OSPF).

### 51. What is EGP?
An **Exterior Gateway Protocol (EGP)** manages routing between different autonomous systems (e.g., BGP).

### 52. What is an Autonomous System?
An **Autonomous System (AS)** is a group of networks under a single administrative control, identified by a unique AS number.

### 53. What is Administrative Distance?
Administrative Distance (AD) measures the trustworthiness of a routing protocol, used to select the best path when multiple protocols provide routes to the same destination. Lower AD is preferred.

### 54. What is the Range of AD Values?
AD ranges from **0 to 255**:  
- **0**: Direct connect (best).  
- **1**: Static route.  
- **5**: EIGRP summary route.  
- **20**: eBGP.  
- **90**: EIGRP.  
- **110**: OSPF.  
- **120**: RIP.  
- **170**: External EIGRP.  
- **200**: iBGP.  
- **255**: Worst (unusable).

### 55. What is a Distance-Vector Routing Protocol?
Distance-vector protocols use distance (e.g., hop count) as the metric to find paths (e.g., RIP, EIGRP).

### 56. What is a Link-State Routing Protocol?
Link-state protocols share neighborhood information with all routers, building a complete network topology (e.g., OSPF).

### 57. What is a Hybrid Routing Protocol?
Hybrid protocols combine distance-vector and link-state features (e.g., EIGRP).

### 58. What is a Routing Metric?
A routing metric determines the best path when multiple routes exist. Examples:  
- **RIP**: Hop count.  
- **OSPF**: Cost (bandwidth-based).  
- **EIGRP**: Bandwidth, delay, reliability, load, MTU.

### 59. What is Hop Count?
Hop count is the number of routers a packet traverses to reach its destination.

### 60. What is Bandwidth, Delay, Reliability, Load?
- **Bandwidth**: Data capacity of a link (Kbps).  
- **Delay**: Time to reach the destination.  
- **Reliability**: Path with the least errors/downtime.  
- **Load**: Utilization level of a path.  
- **MTU**: Maximum packet size for a medium.

### 61. Define Bandwidth and Latency?
- **Bandwidth**: Amount of data transferred.  
- **Latency**: Time taken to transfer data.  
- **Throughput**: Data transferred over a period (combines bandwidth and latency).

### 62. What is Cost?
Cost is inversely proportional to link bandwidth, used as a metric in protocols like OSPF.

### 63. What is CDP?
Cisco Discovery Protocol (CDP) is a Cisco proprietary protocol for collecting information about locally attached and remote devices.

## EIGRP (Enhanced Interior Gateway Routing Protocol)

### 64. Explain EIGRP Routing Protocol?
Enhanced Interior Gateway Routing Protocol (EIGRP) is an advanced distance-vector protocol using the Diffusing Update Algorithm (DUAL) for shortest-path calculation. It’s a hybrid protocol with features of both distance-vector and link-state routing. Supports classless routing, VLSM, route summarization, incremental updates, and load balancing.

### 65. What are the Requirements for Neighborship in EIGRP?
- Same **Autonomous System (AS) number**.  
- Matching **K-values** (metric weights).  
- Same **authentication** settings.  
- Use of **primary address**.  
- Static neighbors must be defined on both sides.

### 66. What Tables Do EIGRP Routers Maintain?
- **Neighbor Table**: Stores EIGRP neighbor information.  
- **Topology Table**: Holds all learned routes from neighbors.  
- **Routing Table**: Contains the best paths to destinations.

### 70. Why is the "No Auto-Summary" Command Used in EIGRP?
By default, EIGRP uses classful routing, omitting subnet masks. The `no auto-summary` command ensures subnet mask information is included with routing updates.

### 71. What Metrics Does EIGRP Use?
EIGRP calculates metrics using **bandwidth**, **load**, **delay**, **reliability**, and **MTU**.

### 72. What are EIGRP Hello & Hold Timers?
- **Hello Timer**: Sends hello packets every 5 seconds.  
- **Hold Timer**: Assumes a link is down if no hello is received for 15 seconds, dropping neighborship.

### 73. What is a Successor?
A **successor** is the best (lowest metric) path to a destination in the topology table.

### 74. What is a Feasible Successor?
A **feasible successor** is the second-best path, acting as a backup to the successor.

### 75. What is Feasible Distance?
**Feasible distance** is the total metric to a destination via the successor route, stored in the routing table.

### 76. What is Advertised Distance & Reported Distance?
**Advertised Distance (Reported Distance)** is the metric a neighbor reports to reach a destination.

### 77. What Authentication Does EIGRP Support?
EIGRP supports only **MD5 authentication**.

### 78. What is the Formula EIGRP Uses to Calculate Metric?
`((10^7 / least bandwidth) + cumulative delay) * 256`

### 79. What are the Different Administrative Distances EIGRP Uses?
- **Internal**: 90  
- **External**: 170  
- **Summary**: 5

### 80. What are the EIGRP Packet Types?
- **Hello**: Discovers and maintains neighbors.  
- **Request**: Queries specific information from neighbors.  
- **Update**: Sends routing and reachability updates.  
- **Query**: Searches for alternate paths during convergence.  
- **Reply**: Responds to query packets.

### 81. What is EIGRP Named Mode?
Named mode is a hierarchical configuration method for EIGRP, allowing multiple address families and AS numbers under a single router configuration.

### 82. What is an EIGRP Passive Interface?
A passive interface stops sending and receiving EIGRP updates on that interface.

### 83. What are EIGRP Variance Values?
Variance (1–128) enables unequal-cost load balancing by multiplying the best metric; default is 1 (equal-cost only).

### 84. What is EIGRP Convergence?
EIGRP maintains feasible successors for fast convergence, switching to backups if the successor fails.

### 85. How Do I Fix EIGRP Stuck in Active?
EIGRP’s active timer (default 3 minutes) tracks queries. If no reply is received within 90 seconds, an SIA (Stuck in Active) query is sent. Fix by checking neighbor connectivity or adjusting timers.

### 86. What is a Leak Map in EIGRP?
A leak map advertises specific prefixes within a summarized range alongside the summary itself.

### 87. What is an EIGRP Stub Router?
A stub router conserves resources in hub-and-spoke networks by limiting route advertisements.

### 88. What is Split Horizon in EIGRP?
Split horizon prevents routing loops by not advertising a route back to the interface it was learned from (enabled by default).

### 89. What Multicast Address Does EIGRP Use?
EIGRP uses **224.0.0.10** for multicast communication.

### 90. How Do I Configure EIGRP?
### 91. How to Configure EIGRP Named Mode?
R1(config)# router eigrp IBM_Hyd
R1(config-router)# address-family ipv4 autonomous-system 12
R1(config-router-af)# network 192.168.12.0
R1(config-router-af)# af-interface FastEthernet0/0

text

Collapse

Wrap

Copy

### 92. Tell Me Some Commands to Troubleshoot EIGRP?
- `#show ip route`: Displays the full routing table.  
- `#show ip eigrp routes`: Shows only EIGRP routes.  
- `#show ip eigrp neighbors`: Displays the neighbor table.  
- `#show ip eigrp topology`: Shows the topology table.

## OSPF (Open Shortest Path First)

### 93. What is the OSPF Routing Protocol?
Open Shortest Path First (OSPF) is a link-state IGP developed by the IETF. It uses the Shortest Path First (SPF) algorithm to find the best path, operates on protocol number 89, and has an AD of 110. Uses multicast addresses **224.0.0.5** (all routers) and **224.0.0.6** (DR/BDR).

### 94. What is an Area in OSPF?
An **area** is a logical group of OSPF networks, routers, and links sharing the same area ID. Each router maintains a topological database for its area.

### 95. What is an Intra-Area Route?
Intra-area routes are updates passed within the same OSPF area.

### 96. What is an Area Border Router (ABR)?
An **ABR** connects two OSPF areas, maintaining topological databases for both and ensuring links belong to the same area.

### 97. What is the Backbone Area?
The **backbone area (Area 0)** is the core of an OSPF network, connecting all other areas and distributing inter-area traffic.

### 98. What is an Autonomous System Boundary Router (ASBR)?
An **ASBR** runs multiple protocols, acting as a gateway to external networks by redistributing routes into OSPF.

### 99. Why Are Areas Used in OSPF?
Areas simplify administration, optimize traffic, and reduce resource usage by limiting the scope of topological databases.

### 100. What is the Router ID (RID)?
The **RID** is a unique 32-bit identifier (e.g., an IP address) for each OSPF router within an AS.

### 101. What is the OSPF Hello Interval?
The **hello interval** is the time between hello packets (default: 10 seconds) to detect neighbors.

### 102. What is the OSPF Dead Interval?
The **dead interval** is the time a router waits for a hello before declaring a neighbor dead (default: 40 seconds).

### 103. What is the OSPF Interface Priority?
The interface priority (default: 1, range: 0–255) determines DR/BDR election; 0 excludes the interface from election.

### 104. What is a Passive Interface?
A **passive interface** stops sending OSPF updates but still advertises the network without forming adjacencies.

### 105. What are the Requirements for Neighbor Adjacency?
- Same **area**.  
- Matching **authentication**.  
- Same **subnet**.  
- Matching **MTU**.  
- Identical **hello and dead intervals**.  
- Matching **stub flags**.

### 106. How Do I Reset My OSPF Neighbor?
Use `#clear ip ospf neighbor`.

### 107. What is a Designated Router (DR)?
The **DR** minimizes adjacencies in broadcast networks by distributing LSAs to all routers.

### 108. What is a Backup Designated Router (BDR)?
The **BDR** is a backup to the DR, taking over if the DR fails.

### 109. How Are OSPF DR and BDR Elected?
- Highest **router priority** wins.  
- If tied, the highest **RID** (loopback or active IP) is chosen.

### 110. What are the OSPF Packet Types?
- **Hello**: Discovers and maintains neighbors.  
- **DBD (Database Description)**: Summarizes the Link-State Database (LSDB).  
- **LSR (Link-State Request)**: Requests specific LSDB records.  
- **LSU (Link-State Update)**: Sends requested LSDB records.  
- **LSAck (Link-State Acknowledgment)**: Ensures reliable delivery.

### 111. What are the OSPF Neighbor States?
- **Down**: No hello received.  
- **Init**: Hello received.  
- **2-Way**: Bidirectional communication established (DR/BDR election occurs here).  
- **Exstart**: Master/slave election and NULL DBD exchange.  
- **Exchange**: Actual DBD exchange.  
- **Loading**: LSR, LSU, and LSAck exchange for updates.  
- **Full**: Databases synchronized, routing begins.

### 113. What are the OSPF Network Types?
Default types depend on media (e.g., broadcast, point-to-point), configurable independently (e.g., Cisco’s five types: broadcast, non-broadcast, etc.).

### 114. What is OSPF Authentication?
OSPF supports **null**, **simple password**, and **MD5** authentication for security, configurable globally or per interface.

### 115. What is a Router LSA (Link-State Advertisement)?
**LSA Type 1 (Router LSA)** describes a router’s interfaces and neighbors within the same area.

### 116. What is a Network LSA?
**LSA Type 2 (Network LSA)** is generated by the DR to describe all routers in its segment, staying within the area.

### 117. What is a Summary LSA?
**LSA Type 3 (Summary LSA)** is generated by ABRs to advertise summarized inter-area routes (e.g., 192.168.0.0/22) across areas.

### 118. What is an ASBR Summary LSA?
**LSA Type 4 (ASBR Summary LSA)** advertises an ASBR’s presence to other areas, generated by ABRs.

### 119. What is an ASBR External LSA?
**LSA Type 5 (ASBR External LSA)** advertises external routes (e.g., 192.168.10.0/24) redistributed by an ASBR into OSPF.

### 120. What is an NSSA External LSA?
**LSA Type 7 (NSSA External LSA)** allows external routes in Not-So-Stubby Areas (NSSAs), masking Type 5 LSAs until converted back by the ABR.

### 121. What Tables Does OSPF Maintain?
- **Neighbor Table**: OSPF neighbor details.  
- **Topology Table**: Network topology structure.  
- **Routing Table**: Best routes.

### 122. Explain OSPF Virtual Link?
A **virtual link** is a logical connection over a non-backbone area to connect a disconnected area to Area 0, using the least-cost path between ABRs.

### 123. Explain Stub Area and Different Types of Stub Areas?
- **Stub Area**: Blocks Type 4 and 5 LSAs, injecting a default route instead. Restrictions: no virtual links, not Area 0, no ASBRs.  
- **Totally Stubby Area**: Blocks Type 3, 4, and 5 LSAs, allowing only intra-area routes and a default route.  
- **Not-So-Stubby Area (NSSA)**: Allows external routes as Type 7 LSAs, converted to Type 5 by the ABR.  
- **Totally NSSA**: Blocks Type 3, 4, and 5 LSAs, allowing Type 7 for external routes.

### 124. Can We Have OSPF Run Over a GRE Tunnel?
Yes, OSPF can run over a GRE tunnel.

### 125. How Do We Configure the OSPF Routing Protocol?
Router(config)# router ospf 100
Router(config-router)# network 172.16.1.0 0.0.0.255 area 0
Router(config-router)# network 10.16.1.0 0.0.0.255 area 1
Router(config-router)# exit

text

Collapse

Wrap

Copy

## BGP (Border Gateway Protocol)

### 126. Explain the Border Gateway Protocol (BGP)?
BGP is an exterior gateway protocol for exchanging routing information between autonomous systems (AS) on the internet. It’s a path-vector protocol making decisions based on paths and policies.  
- **iBGP**: Internal BGP within an AS.  
- **eBGP**: External BGP between ASes.

### 127. What are the BGP Features?
- Path-vector protocol.  
- Open standard.  
- Classless routing.  
- AD: eBGP (20), iBGP (200).  
- Uses TCP port 179.  
- Hello timer: 60 sec; hold timer: 180 sec.

### 128. Can Routers on Different Subnets Become BGP Neighbors?
Yes, BGP uses TCP connections, allowing neighbors on different subnets.

### 129. Difference Between eBGP & iBGP Neighbors?
- **eBGP**: Between different ASes.  
- **iBGP**: Within the same AS.

### 130. Explain Loop Prevention Mechanism in BGP?
- **iBGP**: Routes learned from an iBGP peer aren’t advertised to other iBGP peers.  
- **eBGP**: AS_PATH attribute adds the local AS number; routes with the local AS in AS_PATH are ignored.

### 131. What is the Difference Between Hard Reset and Soft Reset in BGP?
- **Hard Reset**: Drops neighborship, TCP connection, and clears all BGP tables (`#clear ip bgp *`).  
- **Soft Reset**: Retains neighborship and TCP connection, resending/reprocessing updates (`#clear ip bgp * soft`).

### 132. What are Different BGP Message Types?
- **Open**: Establishes neighborship and exchanges parameters (AS number, authentication).  
- **Keepalive**: Sent every 60 seconds to confirm peer availability (hold time: 180 seconds).  
- **Update**: Shares path attributes and NLRI (prefix/length).  
- **Notification**: Reports errors, resetting the neighborship.

### 133. Explain Various States of BGP?
- **Idle**: Initial state, no activity.  
- **Connect**: Awaiting TCP connection completion.  
- **Active**: Retrying TCP handshake if Connect fails.  
- **Open Sent**: TCP established, OPEN message sent, awaiting reply.  
- **Open Confirm**: Awaiting KEEPALIVE after OPEN reply.  
- **Established**: Neighborship formed, updates exchanged.

### 134. Explain BGP Path Attributes?
- **Next Hop**: Next-hop IP address.  
- **Weight**: Cisco proprietary, local significance (0–65535, default 0, 32768 for local routes).  
- **Local Preference**: Best outbound path (0–4294967295, default 100, higher preferred).  
- **AS Path**: Shortest path preferred.  
- **Origin**: i (IGP, preferred), e (EGP), ? (incomplete, least preferred).  
- **MED**: Best inbound path (lower preferred, default 0).  
- **Neighbor Type**: eBGP > iBGP.  
- **IGP Metric**: Lowest preferred.  
- **eBGP Route**: Oldest preferred.  
- **Neighbor RID/IP**: Lowest preferred.

### 135. Explain BGP Local Preference?
Local Preference selects the best exit path from an AS (default: 100, higher preferred), shared among iBGP peers.

### 136. Explain BGP MED?
Multi-Exit Discriminator (MED) hints to external neighbors about preferred entry into an AS (lower preferred, default 0).

### 137. Explain BGP Local Preference? (Repeated)
(See Q135)

### 138. What is Recursive Lookup?
Recursive lookup occurs when a router must resolve a next-hop gateway’s route to forward a packet.

### 139. What is a Route Reflector and Why is it Required?
A **route reflector** allows iBGP peers to share routes (normally restricted), reducing full-mesh requirements in large networks.

### 140. What is the Command to Administratively Disable BGP Neighborship?
#neighbor <neighbor-ip> shutdown
#no neighbor <neighbor-ip> shutdown (to re-enable)

text

Collapse

Wrap

Copy

## Switching

### 141. What is Switching?
Switching forwards data packets between devices on the same network.

### 142. What is a Switch?
A switch is a Layer 2 device connecting multiple devices in a LAN, processing packets based on MAC addresses rather than broadcasting like hubs.

### 143. What is the Difference Between a Hub, Switch, and Router?
- **Hub**: Layer 1, broadcasts all traffic.  
- **Switch**: Layer 2, forwards based on MAC addresses.  
- **Router**: Layer 3, routes between networks using IP addresses.

### 144. What are the Functions of a Switch?
- **Address Learning**: Builds MAC address table.  
- **Packet Forwarding**: Sends frames to specific ports.  
- **Loop Avoidance**: Uses Spanning Tree Protocol (STP).

### 145. What is a Sub-Interface?
A sub-interface is a logical division of a physical interface (e.g., Fast Ethernet) to support VLAN routing (ISL or 802.1Q).

### 146. What is a Broadcast Domain & Collision Domain?
- **Broadcast Domain**: All devices receiving a broadcast frame (VLAN reduces this).  
- **Collision Domain**: Devices competing for medium access (switches eliminate this per port).

### 147. What is a MAC Address Table and How Does a Switch Build It?
The MAC address table maps MAC addresses to ports. The switch learns by associating the source MAC of incoming frames with the receiving port.

### 148. How Does a Switch Learn MAC Addresses?
- **Static**: Manually configured in the CAM table.  
- **Dynamic**: Automatically learned and stored in RAM from incoming frames.

### 149. Explain Flooding?
Flooding occurs when a switch forwards a frame out all ports (except the source port) if the destination MAC is unknown.

## VLAN (Virtual LAN)

### 150. What is a VLAN and How Does It Reduce Broadcast Traffic?
A VLAN logically groups devices on a switch, reducing broadcast domains by limiting broadcast traffic to the VLAN’s ports.

### 151. What is the Difference Between an Access Port and a Trunk Port?
- **Access Port**: Carries traffic for one VLAN, untagged (devices unaware of VLAN).  
- **Trunk Port**: Carries multiple VLANs (1–4094), tagged unless native VLAN.

### 152. What is Frame Tagging and Different Types of Tagging?
Frame tagging assigns a VLAN ID to frames:  
- **ISL (Inter-Switch Link)**: Cisco proprietary.  
- **802.1Q**: Open standard by IEEE.

### 153. Explain the Difference Between 802.1Q and ISL?
- **802.1Q**: Adds a 4-byte tag, lightweight, open standard.  
- **ISL**: Adds a 26-byte header and 4-byte trailer, Cisco proprietary.

### 154. What is a Native VLAN and What Type of Traffic Goes Through It?
The **native VLAN** (default: VLAN 1) carries untagged traffic on a trunk port.

### 155. What is Inter-VLAN Routing?
Inter-VLAN routing enables communication between VLANs via a router or Layer 3 switch (e.g., Router-on-a-Stick or Switch Virtual Interface).

### 156. Tell Me the Commands to Create a VLAN?
Switch(config)# vlan 10
Switch(config-vlan)# name sale
Switch(config-vlan)# exit

text

Collapse

Wrap

Copy

### 157. How Can We Add an Interface to a VLAN?
Switch(config)# interface fastEthernet 0/0
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10

text

Collapse

Wrap

Copy

### 158. How to Configure a Trunk Link?
Switch(config)# interface fastEthernet 0/24
Switch(config-if)# switchport trunk encapsulation <dot1q/isl>
Switch(config-if)# switchport mode trunk

text

Collapse

Wrap

Copy

### 159. How Can We Change the Native VLAN?
Switch(config)# interface fastEthernet 0/0
Switch(config-if)# switchport trunk native vlan 100

text

Collapse

Wrap

Copy

### 160. Which Command is Used to See Trunk Interfaces?
`#show interface trunk`

### 161. Which Command is Used to See All VLANs?
`#show vlan`

## VTP (VLAN Trunking Protocol)

### 162. What is VTP?
VTP (VLAN Trunking Protocol) is a Cisco proprietary protocol synchronizing VLAN information (ID, name) across switches in the same VTP domain.

### 163. What are the Different VTP Modes?
- **Server**: Creates/deletes VLANs, propagates changes (default mode).  
- **Client**: Cannot create/delete VLANs, syncs with server updates.  
- **Transparent**: Forwards VTP ads but doesn’t sync; allows local VLAN changes.

### 164. What are the Requirements to Exchange VTP Messages Between Two Switches?
- Configured as server or client.  
- Same **VTP domain name**.  
- Matching **VTP version**.  
- Trunk link between switches.

### 165. Explain Dynamic Trunking Protocol (DTP)?
DTP, a Cisco proprietary protocol, negotiates trunking and encapsulation (802.1Q or ISL) between switches.

### 166. Explain Dynamic Desirable & Dynamic Auto?
- **Dynamic Desirable**: Actively negotiates to form a trunk if possible.  
- **Dynamic Auto**: Passively responds to trunk negotiation.

## STP (Spanning Tree Protocol)

### 167. What is STP and Redundant Links?
Spanning Tree Protocol (STP) prevents Layer 2 loops by negotiating a loop-free path. Redundant links provide failover but can cause loops without STP.

### 168. How Does STP Work?
STP elects a **Root Bridge**, calculates paths to it, selects one path to forward frames, and blocks others to prevent loops.

### 169. What are the Different Port States?
- **Disabled**: Not participating in STP.  
- **Blocking**: Listens to BPDUs, prevents loops.  
- **Listening**: Processes BPDUs, no frame forwarding.  
- **Learning**: Populates MAC table, no forwarding.  
- **Forwarding**: Fully functional, sends/receives frames.

### 170. What is an STP Timer and Explain Different Types?
STP uses timers for convergence:  
- **Hello Timer**: Interval between BPDUs (default: 2 seconds).  
- **Forward Delay Timer**: Time in Listening + Learning states (default: 15 seconds).  
- **Max Age Timer**: Time BPDUs are stored without updates (default: 20 seconds).

### 171. Explain Types of STP Port Roles?
- **Root Port**: Shortest path to the Root Bridge (on non-root bridges).  
- **Designated Port**: Best path for forwarding (on root and non-root bridges).  
- **Forwarding Port**: Actively forwards frames.  
- **Blocked Port**: Prevents loops, only listens to BPDUs.

### 172. What is a BPDU?
Bridge Protocol Data Units (BPDUs) are messages exchanged by switches to elect the Root Bridge and configure the network topology.

### 173. What is the Destination MAC Address Used by BPDUs?
BPDUs use the multicast address **01:80:C2:00:00:00**.

### 174. How is the Root Bridge Elected?
The Root Bridge has the lowest **Bridge ID** (8 bytes: priority + MAC address). Lower priority wins; if tied, the lowest MAC address is chosen.

### 175. What is the Root Port?
The **Root Port** is the port on a non-root switch with the lowest cost to the Root Bridge, placed in the forwarding state.

## DHCP (Dynamic Host Configuration Protocol)

### 176. What is DHCP?
DHCP dynamically assigns IP addresses and configuration (e.g., subnet mask, gateway) to hosts, using ports 67 (server) and 68 (client).

### 177. What Information Can a DHCP Provide to a Host?
- IP address.  
- Subnet mask.  
- Default gateway.  
- DNS server.  
- WINS information.

### 178. How Does DHCP Work?
DHCP uses the DORA process:  
- **Discover**: Client requests an IP.  
- **Offer**: Server offers an IP.  
- **Request**: Client requests the offered IP.  
- **Acknowledgment**: Server assigns the IP.

### 179. What is the Range of APIPA Addresses?
APIPA (Automatic Private IP Addressing): **169.254.0.1 to 169.254.255.254**, with a subnet mask of **255.255.0.0**.

### 180. What is the Purpose of a Relay Agent?
A DHCP relay agent forwards DHCP packets between clients and servers on different subnets.

### 181. What is a DHCP Decline Message?
A client sends a decline message to indicate an offered IP is already in use.

### 182. What is SNMP?
Simple Network Management Protocol (SNMP) enables devices to share status and activity data using UDP.

### 183. Which Ports Are Used in SNMP?
- **UDP 161**: Sending/receiving requests.  
- **UDP 162**: Receiving traps from devices.

## VPN (Virtual Private Network)

### 184. What is a VPN?
A Virtual Private Network (VPN) creates a secure connection over a public network using encryption, authentication, and tunneling.

### 185. What is an IPsec VPN?
IPsec VPN secures communication with authentication and encryption of IP packets, ensuring confidentiality, integrity, and authenticity.

### 186. At Which Layer Does IPsec Work?
IPsec operates at **Layer 3 (Network Layer)**.

### 187. Name a Major Drawback of IPsec?
IPsec supports only **unicast IP traffic**.

### 188. What is the Difference Between Transport & Tunnel Mode?
- **Transport Mode**: Encrypts the payload only (host-to-host).  
- **Tunnel Mode**: Encrypts the entire packet, adding a new header (network-to-network).

### 189. What are the Three Main Security Services That IPsec VPN Provides?
- **Peer Authentication**.  
- **Data Confidentiality**.  
- **Data Integrity**.

### 190. Define Digital Signature?
A digital signature is an electronic attachment verifying the sender’s authenticity.

### 191. What is Site-to-Site and Remote Access VPN?
- **Site-to-Site VPN**: Connects multiple office networks over the internet.  
- **Remote Access VPN**: Allows remote users to connect to a headquarters network via IPsec or SSL.

### 192. What are the 3 Protocols Used in IPsec?
- **AH (Authentication Header)**: Provides integrity and authentication.  
- **ESP (Encapsulating Security Payload)**: Adds encryption, integrity, and authentication.  
- **IKE (Internet Key Exchange)**: Manages key exchange and SA creation.

### 193. How Do ESP & AH Provide Anti-Replay Protection?
Both use sequence numbers incremented per packet; receivers reject out-of-sequence packets.

### 194. What is IKE?
IKE is a hybrid protocol (Oakley, SKEME, ISAKMP) that negotiates keys and Security Associations (SAs) for IPsec.

### 195. Which Protocol Does IKE Use?
IKE uses **UDP port 500**.

### 196. Explain How IKE/ISAKMP Works?
- **Phase 1**: Establishes a secure channel (bidirectional IKE SA).  
  - **Main Mode**: 6 messages (secure but slower).  
  - **Aggressive Mode**: 3 messages (faster but less secure).  
- **Phase 2**: Establishes IPsec SAs for data (Quick Mode, 3 messages), creating two unidirectional SAs.

### 197. Explain the Message Exchange Between Peers in IKE/ISAKMP?
- **Phase 1 Main Mode**:  
  1. Initiator: Policy proposal (encryption, authentication).  
  2. Responder: Policy acceptance.  
  3. Initiator: Diffie-Hellman key, nonce.  
  4. Responder: Diffie-Hellman key, nonce.  
  5. Initiator: ID, authentication (encrypted).  
  6. Responder: ID, authentication (encrypted).  
- **Phase 2 Quick Mode**:  
  7. Initiator: Hash, IPsec proposal, ID, nonce.  
  8. Responder: Hash, IPsec proposal, ID, nonce.  
  9. Initiator: Signature, hash, ID (all encrypted).

### 198. What is Diffie-Hellman?
Diffie-Hellman (DH) is a public-key protocol for establishing a shared secret over an insecure channel, used in IKE.

### 199. What are Security Associations?
SAs define protocols, algorithms, and keys for IPsec, unidirectional per protocol (AH/ESP).

### 200. What is a Transform Set?
A transform set is a combination of security protocols and algorithms agreed upon during IPsec SA negotiation.

### 201. What are Crypto Access Lists?
Crypto ACLs define which traffic is protected (`permit`) or unprotected (`deny`) by IPsec.

### 202. How to Check the Status of the Tunnel’s Phase 1 & 2?
- **Phase 1**: `#show crypto isakmp sa`  
- **Phase 2**: `#show crypto ipsec sa`

### 203. What is an IPsec Virtual Tunnel Interface?
IPsec VTI provides a routable interface for scalable VPNs, supporting multicast encryption.

### 204. What is DMVPN?
Dynamic Multipoint VPN (DMVPN) scales hub-to-spoke and spoke-to-spoke IPsec VPNs, optimizing performance and supporting dynamic routing and multicast.

### 205. What is GRE?
Generic Routing Encapsulation (GRE) encapsulates IP unicast, multicast, and broadcast packets (protocol 47), developed by Cisco.

### 206. Name a Major Drawback of Both GRE & L2TP?
No encryption.

### 207. What is an SSL VPN? How is it Different from an IPsec VPN?
SSL VPN uses a web browser’s native SSL encryption for remote access, requiring no client software. IPsec VPN uses pre-installed client software.

## Firewall

### 208. What is a Firewall?
A firewall controls traffic between trusted and untrusted networks based on policies, protecting against unauthorized access.

### 209. What is the Difference Between a Gateway and a Firewall?
- **Gateway**: Connects two networks.  
- **Firewall**: Secures a network from unauthorized access.

### 210. At Which Layers Does a Firewall Work?
Firewalls operate at **Layer 3 (Network)**, **Layer 4 (Transport)**, and **Layer 7 (Application)**.

### 211. What is the Difference Between Stateful & Stateless Firewall?
- **Stateful**: Tracks connection states in a table (e.g., PIX, ASA, Checkpoint).  
- **Stateless**: Filters packets individually without state (e.g., Cisco router ACLs).

### 212. What Information Does a Stateful Firewall Maintain?
- Source IP, Destination IP.  
- Protocol (TCP/UDP).  
- TCP/UDP port numbers, TCP sequence numbers, flags.

### 213. How Can We Allow Packets from a Lower Security Level to a Higher Security Level?
Use **Access Control Lists (ACLs)** to override default security levels.

### 214. What is the Security Level of Inside and Outside Interfaces by Default?
- **Inside**: 100 (highest).  
- **Outside**: 0 (lowest).

### 215. What Protocols Are Inspected by ASA?
TCP and UDP by default.

### 216. Does ASA Inspect ICMP?
No, ICMP inspection is not enabled by default on ASA.

### 217. Explain DMZ (Demilitarized Zone) Server?
A DMZ is a separate network behind a firewall hosting public servers (e.g., web, FTP), limiting attack impact to those servers.

### 218. What are the Values for Timeout of TCP Session, UDP Session, ICMP Session?
- **TCP**: 60 minutes.  
- **UDP**: 2 minutes.  
- **ICMP**: 2 seconds.

### 219. What is the Difference in ACL on ASA vs. Router?
- **Router**: Deleting one ACE removes the entire ACL.  
- **ASA**: Deleting one ACE leaves the ACL intact.

### 220. What are the Different Types of ACL in a Firewall?
- Standard ACL.  
- Extended ACL.  
- EtherType ACL (Transparent Firewall).  
- WebType ACL (SSL VPN).

### 221. What is a Transparent Firewall?
In transparent mode, ASA acts as a Layer 2 device (bridge/switch), forwarding frames by MAC address.

### 222. What is the Need for a Transparent Firewall?
It simplifies deployment in existing networks without requiring IP reconfiguration or topology changes.

### 223. What are the Differences Between a Switch and ASA (in Transparent Mode)?
- ASA doesn’t flood unknown unicast frames or participate in STP.  
- Switch: Layers 1–2; ASA: Layers 1–7.

### 224. What Information is Exchanged Between ASAs Over a Failover Link?
- State (Active/Standby).  
- Hello messages.  
- Network link status.  
- MAC addresses.  
- Configuration replication.

### 225. Explain Active/Standby Failover?
In Active/Standby, one ASA passes traffic (active), while the other (standby) takes over if the active unit fails. Supported in single/multiple context modes.

### 226. What is Policy NAT?
Policy NAT uses an extended ACL to NAT based on both source and destination addresses (and optionally ports), unlike regular NAT (source only).  
- **Static Policy NAT**: For static mappings.  
- **Dynamic Policy NAT**: For dynamic mappings.
- -----------------------------------------------------------------------------------------------------------------------

