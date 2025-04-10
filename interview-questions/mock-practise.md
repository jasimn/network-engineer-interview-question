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


