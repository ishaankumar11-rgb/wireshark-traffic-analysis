# Network Traffic Packet Inspection & Analysis with Wireshark

Arrowstack Cyber Security Internship, Task 2.

Captured and analysed traffic generated only by my own Kali VM in a lab (ping, nslookup, curl), then documented the findings.

## Contents
- `report/security_report.md` : findings and analysis
- `screenshots/` : Wireshark views (DNS, ICMP)
- `evidence/` : tshark text output (IPv6 address of the VM redacted)

## Method
1. Captured on `eth0` with Wireshark: `ping -c 4 8.8.8.8`, `nslookup example.com`, `curl http://example.com`
2. Filtered with `dns`, `icmp`, `tcp.flags.syn==1`, `http`
3. Extracted statistics with tshark (`-z io,phs`, `-z follow,tcp,ascii,0`)

## Scope and privacy
Only my own VM traffic was captured. The raw `.pcapng` is not published because it contains my public IPv6 address.
