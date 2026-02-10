Network Reconnaissance Lab
SOC Reconnaissance Lab - VirtualBox, Nmap, Wireshark, nslookup, and ipconfig
	Host OS: Windows 11
	Hypervisor: Oracle VirtualBox
	Guest OS:
	Kali Linux 2025.2
	Windows 11
	Network Mode: Host-only Adapter

Step 1:
What I Did:
•	Configured a host-only network in VirtualBox.
•	Connected both the Kali Linux VM and the Windows VM to the same host-only adapter.
•	Verified that both systems were on the same subnet.


What I learned:
•	How to create an isolated virtual network for safe testing.
•	How host-only networks prevent lab traffic from reaching the real internet.
•	The importance of proper network configuration before running scans.

Purpose:
The purpose of this step was to create a controlled and isolated lab environment where network scans and traffic analysis could be performed safely without affecting real systems.
Step 2:
What I Did:
•	Used ipconfig /all on the Windows VM to check IP configuration.
•	Used Ip a on the Kali VM to identify its IP address.
•	Performed ping tests between the two machines to confirm connectivity.

What I learned:
•	How to identify IP addresses and subnet information.
•	How to verify network communication between systems.
•	How to troubleshoot connectivity using basic commands.

Purpose:
The purpose of this step was to ensure both machines were reachable on the network before performing reconnaissance and traffic analysis

Step 3:
What I Did:
•	Used netstat on the Windows VM to view listening ports and active services.

What I learned:
•	How to identify which services are running locally.
•	How to view open ports from the system itself.
•	That Windows systems commonly expose networking services by default.

Purpose:
The purpose of this step was to observe which services were running on the target system before performing an external scan
Step 4:
What I Did:
•	Used Nmap from the Kali VM to perform host discovery on the subnet.
•	Confirmed the Windows system was active on the network.

What I learned:
•	How Nmap identifies live hosts.
•	How subnet scanning works.
•	The importance of identifying active systems before deeper scans.

Purpose:
The purpose of this step was to discover active devices on the network and confirm that the target system was reachable for further analysis
Step 5:
What I Did:
•	Ran multiple Nmap scans against the Windows host.
•	Identified open ports: 135, 139, and 445.
•	Performed service detection scans.
•	Saved the results to a file (nmap_full.txt).
What I learned:
•	How to identify exposed services using Nmap.
•	That open ports represent potential attack surfaces.
•	How common Windows networking ports can be security risks.
Purpose:
The purpose of this step was to identify open ports and running services on the target system and assess their potential security risk
Step 6:
What I Did:
•	Launched Wireshark on the Kali VM.
•	Started a live packet capture.
•	Generated ICMP traffic by pinging the Windows host.
•	Ran an Nmap scan while capturing traffic.
•	Observed SYN packets from the scan.
•	Saved the capture file.


What I learned:
•	How to capture live network traffic.
•	How to filter and identify ICMP packets.
•	How reconnaissance scans appear on the network.
•	How SOC analysts detect scanning activity.


Purpose:
The purpose of this step was to gain visibility into network traffic and understand how scanning activity appears at the packet level
Step 7:
What I Did:
•	Used ipconfig /all to view network configuration.
•	Used nslookup to test DNS functionality.

What I learned:
•	How to verify IP configuration quickly.
•	How to test DNS resolution from the command line.
•	How basic tools assist in troubleshooting network issues.

Purpose:
The purpose of this step was to practice essential command-line tools used for network diagnostics and troubleshooting
