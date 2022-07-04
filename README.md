# Wireshark

## Description 

Wireshark is a network protocol anaylyzer. It can be used to anaylyze your network traffic at the packet level. 

## Major features
1. Live and Offline Analysis 
2. Multiplatform: Windows, Linux, MacOS, Solaris, FreeBSD, NetBSD and others.
3. VoIP anaylsis 
4. Decryption support for IPSec, ISAKMP, Kerberos, SNMPv3, SSL/TLS, WEP and WPA/WPA2.
5. Output export includes XML, PostScript, CSV or plain text 

## Installation 

Wireshark can be installed at https://www.wireshark.org for Windows or MacOS.
On linux, you can install using `apt install wireshark` or a similar package manager. 

### Filtering 

Wireshark only has a few that you will need to be familiar with:

and - operator: and / &&
or - operator: or / ||
equals - operator: eq / ==
not equal - operator: ne / !=
greater than - operator: gt /  >
less than - operator: lt / <

`ip.addr == <IP Address>`
`ip.src == <SRC IP Address> and ip.dst == <DST IP Address>`
`tcp.port eq <Port #> or <Protocol Name>`
`udp.port eq <Port #> or <Protocol Name>`

### Packet Dissection

Packet Disections follows the OSI Model, i.e 

Frame (Layer 1) 
Source [MAC] (Layer 2) 
Source [IP] (Layer 3)
Protocol (Layer 4) - UDP/TCP 
Application Protcol (Layer 5) - HTTP, FTP, SMB etc.

![image](https://user-images.githubusercontent.com/70596795/177217682-bfca062f-e508-45f7-8269-6a816d9ef442.png)



# General Notes 



1. You can open a file from the command line using the command line with 
`# wireshark example.pcap`

2. Wireshark Color Coding Cheat Sheet
![image](https://user-images.githubusercontent.com/70596795/177215459-e4010a19-868b-4f78-87e5-aad28d7b7da2.png)

3. Collection Methods 
- Network Taps
- Mac Floods
    Intended to overflood the swtiches CAM table which turns the switch into     a HUB because no more mac-address can be handed out.
- ARP Poisoning 
    Allows redirection of traffic from host(s) to attackers machine.
   



## Resources/Citations
