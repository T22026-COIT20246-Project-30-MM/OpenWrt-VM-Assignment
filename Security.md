COIT20246 Cyber Security and Networking

Project Specification 1

Small Business Network Security, OpenWrt Firewall Configuration and
Cyber Security Risk Assessment

Student 1: Pavan Reddy Chinthalapally Student ID: 12327397

Student 2: Patel Ronak Ghanshyambhai Student ID: 12328755

Business Scenario: Small IT and Business Consultancy, Brisbane,
Queensland, Australia

4.2 Security Hardening and Traffic Analysis

4.2.1 Harden the OpenWRT System

Figure 1: Successful SSH Login to the OpenWrt Virtual Machine

Figure 2: Successful Root Password Change on OpenWrt

Figure 3: OpenWrt Password Hashes Stored in /etc/shadow

Figure 4: Ed25519 SSH Key Pair Generation on the Windows Host

Key-based authentication is more secure because it uses a cryptographic
key pair instead of relying solely on passwords. The private key remains
securely on the authorised device, while the public key is stored on
OpenWrt. This reduces exposure to password guessing, brute-force
attacks, credential theft, and password reuse.

Figure 5: OpenWrt Enabled Services and Startup Configuration

Disabling unnecessary services reduces the system's attack surface by
removing functions that are not required. Fewer active services mean
fewer open ports, processes, and potential vulnerabilities for attackers
to exploit. This limits possible entry points, reduces security risks,
and makes the OpenWrt system easier to monitor and maintain securely.

4.2.2 Capture and Analyse Network Traffic

Figure 6: HTTP Traffic Capture Using tcpdump on the OpenWrt br-mng
Interface

Figure 7: HTTP Traffic Capture Using tcpdump with Host and TCP Port
Filtering

Figure 8: Captured Network Traffic Displayed in Wireshark (HTTP)

The attacker who taps information from an HTTP stream is able to obtain
the server and client IP addresses, the request and response URL, HTTP
requests and responses, and the content of the target web pages.
Personal information, including names, student IDs or details that could
be seen from the webpage, might be given away due to lack of encryption
in the HTTP. Any traffic monitoring, and information disclosure, would
be possible.

Figure 9: SSH Traffic Capture Attempt Using tcpdump on OpenWrt

Figure 10: SSH Network Traffic Packets Displayed in Wireshark During
Traffic Analysis

In the HTTP capture it is possible to read webpage content and requests.
Encrypted protocols like SSH, on the other hand, keep contents of the
sessions secure from being viewed directly. Encryption ensures the
confidentiality of the data being sent, minimising the chances of
attackers being able to obtain commands, credentials or any other
sensitive information through network interception.

  -----------------------------------------------------------------------
  Hardening Step                      Security Risk Addressed
  ----------------------------------- -----------------------------------
  1\. Change Default Root Password    Reduces the risk of unauthorised
                                      administrative access through
                                      default or easily guessed
                                      credentials. A strong, unique
                                      password makes credential-based
                                      attacks more difficult.

  2\. Examine Password Storage in     Addresses the risk of password
  /etc/shadow                         disclosure. Storing passwords as
                                      hashes rather than plaintext
                                      prevents the original passwords
                                      from being directly exposed if the
                                      password database is accessed.

  3\. Set Up SSH Key-Based            Reduces the risk of password
  Authentication                      guessing and brute-force attacks.
                                      SSH keys provide stronger
                                      authentication than password-only
                                      access, particularly when a
                                      passphrase protects the private
                                      key.

  4\. Disable Unnecessary Services    Reduces the attack surface of
                                      OpenWrt. Unnecessary services can
                                      provide additional entry points
                                      that an attacker could exploit.
  -----------------------------------------------------------------------
