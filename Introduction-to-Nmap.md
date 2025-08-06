# Introduction to Nmap

**Network Mapper (Nmap)** is an open-source network analysis and security auditing tool written in C, C++, Python, and Lua. It is designed to scan networks and identify which hosts are available on the network using raw packets, and services and applications, including the name and version, where possible. It can also identify the operating systems and versions of these hosts. Besides other features, Nmap also offers scanning capabilities that can determine if packet filters, firewalls, or intrusion detection systems (IDS) are configured as needed.

## Use Cases

The tool is one of the most used tools by network administrators and IT security specialists. It is used to:

- Audit the security aspects of networks  
- Simulate penetration tests  
- Check firewall and IDS settings and configurations  
- Types of possible connections  
- Network mapping  
- Response analysis  
- Identify open ports  
- Vulnerability assessment as well  

## Nmap Architecture

Nmap offers many different types of scans that can be used to obtain various results about our targets. Basically, Nmap can be divided into the following scanning techniques:

- Host discovery  
- Port scanning  
- Service enumeration and detection  
- OS detection  
- Scriptable interaction with the target service (Nmap Scripting Engine)  

## Syntax

Offensive404@htb[/htb]$ nmap <scan types> <options> <target>


## Scan Techniques

Nmap offers many different scanning techniques, making different types of connections and using differently structured packets to send. Here we can see all the scanning techniques Nmap offers:

Offensive404@htb[/htb]$ nmap --help

## Output

<img width="651" height="284" alt="image" src="https://github.com/user-attachments/assets/c2968eba-da2f-4357-8446-f281ac90c38a" />


##

For example, the TCP-SYN scan (-sS) is one of the default settings unless we have defined otherwise and is also one of the most popular scan methods. This scan method makes it possible to scan several thousand ports per second.
The TCP-SYN scan sends one packet with the SYN flag and, therefore, never completes the three-way handshake, which results in not establishing a full TCP connection to the scanned port.
If our target sends a SYN-ACK flagged packet back to us, Nmap detects that the port is open.
If the target responds with an RST flagged packet, it is an indicator that the port is closed.
If Nmap does not receive a packet back, it will display it as filtered. Depending on the firewall configuration, certain packets may be dropped or ignored by the firewall.
