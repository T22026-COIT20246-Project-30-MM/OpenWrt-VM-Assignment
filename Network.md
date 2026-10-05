**##COIT20246 Cyber Security and Networking##**

**Project Specification 1**

Small Business Network Security, OpenWrt Firewall Configuration and
Cyber Security Risk Assessment

Student 1: Pavan Reddy Chinthalapally Student ID: 12327397

Student 2: Patel Ronak Ghanshyambhai Student ID: 12328755

Business Scenario: Small IT and Business Consultancy, Brisbane,
Queensland, Australia

**4.1 Network Setup**

**4.1.1 List the Assumptions**

Location: The business is assumed to operate in Brisbane, Queensland,
Australia.

Professional services: It provides IT support, cybersecurity consulting,
network configuration and business technology services.

Staff: 8 staff -- 1 Business Manager, 2 IT Support Specialists, 3
Business Consultants and 2 Administrative Staff.

Business/public information: The Website contains business and service
information, contact information, project information, and
Identification information of staff members/students needed for testing.

**4.1.2 Set Up the Network**

![Network Setup](images/Picture1.png)

Figure 1: OpenWrt 22.03.3 Virtual Machine Boot and System Information
![Network Setup](images/Picture2.png)

Figure 2: OpenWrt Network Interface Configuration and IP Address
Allocation
![Network Setup](images/Picture3.png)

Figure 3: OpenWrt System and Virtual Machine Information

![Network Setup](images/Picture4.png)

Figure 4: OpenWrt Network Configuration and Interface Mapping
![Network Setup](images/Picture32.png)

Figure 5: OpenWrt Network Interface and DHCP Configuration

![Network Setup](images/Picture30.png)

Figure 6: OpenWrt Routing Table and Network Interface Status

![Network Setup](images/Picture6.jpg)


Figure 7: Proposed OpenWrt VirtualBox Laboratory Network Topology and IP
Address Allocation
![Network Setup](images/Picture7.png)

Figure 8: Successful ICMP Connectivity Test from Windows Host to OpenWrt

![Network Setup](images/Picture8.png)

Figure 9: Successful Internet Connectivity Test from OpenWrt to External
Networks

![Network Setup](images/Picture9.png)

Figure 10: OpenWrt Web Interface HTML in /www/index.html

**4.1.3 Configure Firewall Rules**
 
![Network Setup](images/Picture11.png)

Figure 11: Failed SSH Authentication Attempt on OpenWrt Through TCP Port
22

![Network Setup](images/Picture12.png)

Figure 12: OpenWrt Firewall Configuration Allowing SSH Traffic on TCP
Port 2222
![Network Setup](images/Picture33.png)
![Network Setup](images/Picture13.png)

Figure 13: SSH Port Modification to TCP 2222 and Connection Refusal
During Port Verification

![Network Setup](images/Picture34.png)

Figure 14: Successful Access to the OpenWrt Web Server Through HTTP

![Network Setup](images/Picture35.png)

Figure 15: OpenWrt Root Password Hardening and Firewall Zone
Configuration

![Network Setup](images/Picture36.png)

Figure 16: OpenWrt HTTP Service Configuration and TCP Port 80 Firewall
Rule

![Network Setup](images/Picture37.png)

Figure 17: Successful ICMP Connectivity Test from Windows Host to
OpenWrt

![Network Setup](images/Picture16.png)

Figure 18: OpenWrt Firewall and Network Security Configuration Verification

Firewall Filtering provides some extra security on the network, as it
restricts access to key services. The block of port 80 prevents any
unauthorised access of web services and then it is opened back to test
the service availability in a controlled way. Administrative access
through SSH port 22 is initially allowed and it is later switched to
port 2222 thus lessening the chances of making SSH automatic attacks
(Kuruppathukattil, 2025). Blocking ICMP helps prevent network
reconnaissance, re-enabling it when it is needed for connectivity
testing. The management interface port 81 is limited and access to it
may not be provided to any unauthorised administrative access. Together,
these rules mandate controlled connectivity, eases the attack surface,
protects administrative services and enhances network security.

**4.1.4 Network Diagram and Address Allocation Production**

![Network Setup](images/Picture17.jpg)

Figure 19: Proposed Small Business Production Network Topology and IP
Address Allocation

The suggested production network includes a OpenWrt router/firewall for
Internet connection and several routing and NAT services, thus offering
traffic protection and routing to the Internet. The protected
97.0.0.0/24 LAN is used to physically connect the business Ethernet
switch and the dedicated web server to 8 staff workstations. The web
server uses 97.0.0.10, while staff devices use 97.0.0.20--97.0.0.27
(Gentile et al. 2024). The default gateway for the router is 97.0.0.1.
The structured design facilitates safe connectivity, managed network
access, business website functionality and resource management.

**4.1.5 IP Addressing Requirements**


| **Device / Role** | **IP Address** | **Subnet Mask** | **Default Gateway** | **Purpose** |
|---|---|---|---|---|
| **OpenWrt Router/Firewall** | `97.0.0.1` | `255.255.255.0` (`/24`) | `---` | Network gateway, routing and firewall |
| **Business Web Server** | `97.0.0.10` | `255.255.255.0` (`/24`) | `97.0.0.1` | Business website |
| **Business Manager** | `97.0.0.20` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **IT Support 1** | `97.0.0.21` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **IT Support 2** | `97.0.0.22` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **Business Consultant 1** | `97.0.0.23` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **Business Consultant 2** | `97.0.0.24` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **Business Consultant 3** | `97.0.0.25` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **Administration 1** | `97.0.0.26` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |
| **Administration 2** | `97.0.0.27` | `255.255.255.0` (`/24`) | `97.0.0.1` | Staff workstation |


**References**

Gentile, A.F., Macrì, D., Greco, E. and Fazio, P., 2024. IoT IP overlay
network security performance analysis with open source infrastructure
deployment. Journal of Cybersecurity and Privacy, 4(3), pp.629-649.

Kuruppathukattil, V., 2025, August. Optimized WiFi Network Deployment
with OpenWRT and FreeRadius for Secure and Scalable Connectivity. In
2025 IEEE 2nd International Conference on Information Technology,
Electronics and Intelligent Communication Systems (ICITEICS) (pp. 1-6).
IEEE.