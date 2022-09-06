# Nmap Switches 
1. -sS (Syn Scan) # A partial completeion of a SYN/ACK/SYNACK handshake. AKA a half-open scan, just enough to see if a port is open. 
### Sends a UDP packet that is empty (no payload) unless protocol specific. States include open, open | filtered, closed, filtered.
2. -sU (UDP Scan) 
3. -O (OS Scan) 
4. -sV (Version of services running on the target) 
5. -v (Verbosity I) 
6. -vv (Verbosity II)
7. -oA (Saves scan to three MAJOR formats)
8. -oN (Saves results to a normal format) 
9. -oG (Grepable format) 
10. -A (Aggressive Mode) 
11. -T5 (Timing Template, used to increase or decrease speed. Higher means noisier) 
12. -p <port> (Single Port Scan) 
13. -p <1000>-<1500> (Port Scan Range) 
14. --script (runs default script) 
15. --script=vuln
  
  
