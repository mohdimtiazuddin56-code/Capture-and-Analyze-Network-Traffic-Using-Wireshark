# Capture-and-Analyze-Network-Traffic-Using-Wireshark

# Wireshark Capture Report

## Steps Performed
1. Installed Wireshark and opened it on Windows.
2. Selected the active network interface (Loopback Adapter).
3. Started packet capture and generated traffic:
   - Browsed the internet.
   - Ran `ping 8.8.8.8 -n 5` from PowerShell.
4. Stopped the capture after ~1 minute.
5. Applied filters (`icmp`, `tcp`, `udp`) to analyze traffic.
6. Exported capture as `traffic_capture.pcap`.

## Findings
- ICMP (Ping)
  Observed echo requests and replies to 8.8.8.8.  
  Example: `Echo (ping) request, id=1, seq=1` and `Echo reply`.

- TCP
  Captured TCP packets on local loopback.  
  Example: SYN → SYN/ACK → ACK handshake packets.

- UDP
  UDP packets between `::1` (IPv6 loopback).  
  Example: Source Port 53899 → Destination 53899.

## Summary
Wireshark successfully captured live traffic. The capture file contains at least three different protocols: ICMP, TCP, and UDP. This demonstrates how Wireshark can analyze packet-level communication between systems.


<img width="963" height="975" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/4e0f56d4-cb3e-40dc-8eb4-f50b734328b4" />

<img width="1920" height="1023" alt="{068F39E2-E4A8-4ADD-8C94-32A3171A29BC}" src="https://github.com/user-attachments/assets/ac82f2d5-02d5-49c8-90a8-b853db1e6b07" />
