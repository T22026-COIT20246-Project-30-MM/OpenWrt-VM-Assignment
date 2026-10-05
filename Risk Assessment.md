COIT20246 Cyber Security and Networking

Project Specification 1

Small Business Network Security, OpenWrt Firewall Configuration and
Cyber Security Risk Assessment

Student 1: Pavan Reddy Chinthalapally Student ID: 12327397

Student 2: Patel Ronak Ghanshyambhai Student ID: 12328755

Business Scenario: Small IT and Business Consultancy, Brisbane,
Queensland, Australia

4.3 Risk Assessment and Security Controls

4.3.1 Conduct a Cyber Security Risk Assessment

Figure 1: Cybersecurity Risk Assessment Matrix and Recommended Controls

A mini business network developed in Sections 4.1 and 4.2 is subject to
a mini cyber security risk assessment, carried out with the TVAMatrix
template. The assessment included 12 types of information security
threats such as: unauthorised access, network interception, malware,
denial of service, unauthorised modification, information disclosure,
phishing, physical theft, unnecessary service exposure, ICMP
reconnaissance, SSH exposure, management-interface exposure. The assets
covered hardware, software/services, information/data, credentials and
the people. These were business/client records, business/Service
information, employee credentials and SSH private keys. The controls
that already existed were firewall rules, SSH key authentication,
hardening of the root password, encryption and turning off unnecessary
services.

4.3.2 Recommend Security Controls

Employee credentials (A05) is the highest-risk data asset, with an
inherent risk score of 20. There are three suggested security controls:

1.  Multi-Factor Authentication (MFA): This decreases the likelihood of
    a credential being compromised. Must be activated for administrators
    and employees. This could result in longer logon, and use of an
    additional authentication mechanism will be necessary for users.

2.  Strong Authentication and SSH Key Management: Use of SSH Key
    Management is highly encouraged and SSH keys are going to replace
    password access, where the private key is protected with a
    passphrase (Makris, 2024). Moving SSH from its own port 22 and
    hardening its access with port 2222 means less exposure from a
    brute-force approach. The key management may cause recovery and
    admin overhead.

3.  Access Control/Firewall Restrictions: Administrative services should
    be networked within a management network and unneeded ports should
    be closed. A foundation of exit and entry firewall rules for SSH,
    HTTP and ICMP and management.

References

Makris, N., 2024. Cyber range development: Configuration of the cyber
range environment network and monitoring tools (Master's thesis,
Πανεπιστήμιο Πειραιώς).
