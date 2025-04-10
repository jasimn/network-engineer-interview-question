# Network Engineer Interview
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
# CSE Interview: Networking & Security Questions

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

### 11. Do ARP requests leave the local network?
- **Answer:** **No**, ARP is confined to the local broadcast domain (Layer 2).

### 12. What is ICMP? At which OSI layer?
- **Answer:** **Internet Control Message Protocol (ICMP)** operates at **Layer 3 (Network Layer)** (e.g., used by `ping`).

### 13. What is MTU?
- **Answer:** **Maximum Transmission Unit (MTU)** is the largest packet size (in bytes) allowed on a network path.

### 14. Which wavelength is associated with multimode fiber telecom equipment?
- **Answer:** **b. 850 nm** (also 1300 nm; single-mode uses 1310/1550 nm).

### 15. Which protocol does **not** use UDP as transport?
- **Answer:**  
  - ✅ **DNS** (can use UDP/TCP)  
  - ✅ **DHCP** (UDP)  
  - ❌ **SNMP** (uses UDP; your answer was incorrect).  

### 16. Which command identifies TCP connections?
- **Answer:** **`netstat -t`** (or `ss -t` on Linux).

### 17. Which command displays IP address?
- **Answer:** **`ipconfig`** (Windows) / `ifconfig` (Linux).

### 18. What is a MAC address?
- **Answer:** A **hardware address** (48-bit) assigned to a network interface (e.g., `00:1A:2B:3C:4D:5E`).

### 19. What format is `00:01:02:03:04:05`?
- **Answer:** **Colon-Hexadecimal** (also accepts hyphenated or dot notation).

### 20. Ping operates at which OSI layer?
- **Answer:** **Layer 3 (Network Layer)** (uses ICMP).

---

## IP Addressing & Subnetting

### 21. How to list all open TCP ports on localhost?
- **Answer:**  
  - Linux: `netstat -tuln` or `ss -tuln`  
  - Windows: `netstat -ano | findstr LISTENING`  

### 22. What are listening ports?
- **Answer:** Ports actively accepting incoming connections (e.g., `0.0.0.0:22` for SSH).

### 22a. Command to list all open ports on localhost?
- **Answer:** `netstat -tuln` (Linux) or `netstat -ano` (Windows).

### 23. Class C IP address `192.168.0.0` – how many hosts?
- **Answer:** **254 hosts** (2^8 – 2 = 254; excludes network/broadcast).

### 24. Which IP cannot be routed?
- **Answer:** **10.255.200.200** (private IP; non-routable on the public internet).

### 25. Is `196.16.144.99/23` a valid host address?
- **Answer:**  
  - **Network:** `196.16.144.0`  
  - **Broadcast:** `196.16.145.255`  
  - **Usable Hosts:** 510 (2^9 – 2).  

### 26. Is `196.16.1.103/26` a broadcast address?
- **Answer:**  
  - **Network:** `196.16.1.64`  
  - **Broadcast:** `196.16.1.127` → **No**, `.103` is a host address.  

### 27. How to trace the path to a domain?
- **Answer:** **`tracert` (Windows) / `traceroute` (Linux)**.

### 28. Given `192.168.3.6/22`:  
   - **Network:** `192.168.0.0`  
   - **Broadcast:** `192.168.3.255`  
   - **1st Host:** `192.168.0.1`  
   - **Last Host:** `192.168.3.254`  

### 29. Non-routable IP example?
- **Answer:** **`172.16.0.1`** (private range; rejected by public routers).

### 30. Command to resolve routing table?
- **Answer:** **`route -n` (Linux) / `route print` (Windows)**.

---

## Security

### 31. Safest way to send data to the cloud?
- **Answer:** **a. VPN** (encrypts all traffic) and **b.

