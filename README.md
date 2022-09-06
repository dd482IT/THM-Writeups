# Nmap Switches 
### A partial completeion of a SYN/ACK/SYNACK handshake. AKA a half-open scan, just enough to see if a port is open.
1. -sS (Syn Scan)  
### Sends a UDP packet that is empty (no payload) unless protocol specific. States include open, open | filtered, closed, filtered.
### Open means there was a response (unusual), open | filtered means no response after retries, closed means ICMP port unreachable and filtered means 
### others ICMP unreacable errors. 
2. -sU (UDP Scan) 
###  
4. -O (OS Scan) 
5. -sV (Version of services running on the target) 
6. -v (Verbosity I) 
7. -vv (Verbosity II)
8. -oA (Saves scan to three MAJOR formats)
9. -oN (Saves results to a normal format) 
10. -oG (Grepable format) 
11. -A (Aggressive Mode) 
12. -T5 (Timing Template, used to increase or decrease speed. Higher means noisier) 
13. -p <port> (Single Port Scan) 
14. -p <1000>-<1500> (Port Scan Range) 
15. --script (runs default script) 
16. --script=vuln
  
  
