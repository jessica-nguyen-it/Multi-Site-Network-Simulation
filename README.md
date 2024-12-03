## Multi-Site-Network-Simulation (In Progress)
This project involves designing and configuring a multi-site network using Cisco Packet Tracer. It includes the setup of routers, switches, servers, and PCs across three sites, with a focus on efficient network management. I implemented IP addressing, subnetting, DHCP, and RIP routing to ensure seamless communication between sites. Additionally, I optimized network performance using Spanning Tree Protocol (STP) and validated the setup with diagnostic tools like ping and tracert for troubleshooting and performance verification.

## Status
This project is nearly complete, with only bug fixes and additional features like VLANs left to implement. It should be finished very soon!

### Key Features
- **Three interconnected sites**:
  - **Site 1**: One core switch, four access switches, a dedicated DHCP server, and multiple PCs.
  - **Site 2**: One core switch, a DNS server, and an HTTP server.
  - **Site 3**: One core switch, two access switches, a DHCP server, and PCs.
- **Dynamic IP Addressing**: DHCP servers automatically allocate IPs within their site subnets.
- **Domain Name Resolution**: DNS server resolves domain names like `google.com` to corresponding IP addresses.
- **Routing Protocol**: Configured **RIP** (Routing Information Protocol) for inter-site communication.
- **Redundancy**: **Spanning Tree Protocol (STP)** ensures network reliability with designated primary and secondary root bridges.

---

## Network Topology
![Network Topology](https://github.com/jessica-nguyen-it/Multi-Site-Network-Simulation/blob/main/Screenshots/Screenshot%202024-12-02%20200223.png)
This topology connects three sites with routers, switches, servers, and PCs, each assigned a subnet and services for a segmented and scalable network.

---

## Configuration Details

### 1. IP Addressing
Each site is assigned a unique subnet to ensure proper segmentation:
- **Site 1**: `192.168.40.0/24`
- **Site 2**: `192.168.50.0/24`
- **Site 3**: `192.168.30.0/24`
- **Router-to-Router Links**: Reserved IP ranges `192.168.1.0` and `192.168.2.0`.

### 2. Servers
- **DNS Server**:
  - Maps domain names to IP addresses (e.g., `google.com` -> `192.168.50.3`).
  - Subnet: `192.168.50.0/24`
- **HTTP Server**:
  - Hosts a sample website accessible via `google.com`.
  - Subnet: `192.168.50.0/24`
- **DHCP Servers**:
  - **Site 1**: Allocates IPs within `192.168.40.0/24`.
  - **Site 3**: Allocates IPs within `192.168.30.0/24`.

### 3. Routing Protocol
- Implemented **RIP** for simplicity:
  - Enables routers to share routing information dynamically.
  - Configured to manage traffic within each subnet and between sites.

### 4. Redundancy
- **Spanning Tree Protocol (STP)**:
  - Configured to ensure fault tolerance by designating a primary and secondary root bridge for VLANs.

---

## How to Use

### 1. Open the Project
- Launch **Cisco Packet Tracer** and load the `.pkt` file.

### 2. Explore the Network
- Inspect the configurations of routers, switches, and servers.
- Simulate real-world scenarios like DNS lookups and web browsing.

### 3. Run Tests
- Use tools such as `ping` and `traceroute` to verify connectivity and network functionality.


