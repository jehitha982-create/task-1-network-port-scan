# Cyber Security Internship - Task 1

## Objective
Scan the local network using Nmap to discover open TCP ports and understand network exposure.

## Tools Used
- Nmap
- Wireshark (Optional)
- Windows Command Prompt

## Network Range
172.21.6.0/24

## Scan Command

```bash
nmap -sT 172.21.6.0/24
```

## Scan Results

### Host 1
**IP Address:** 172.21.6.136

Open Port:
- 53/tcp (DNS)

### Host 2
**IP Address:** 172.21.6.168

Open Ports:
- 135/tcp (MSRPC)
- 139/tcp (NetBIOS-SSN)
- 445/tcp (Microsoft-DS)
- 2869/tcp (ICSLAP)

## Security Risks
- Port 53: DNS service may be abused if misconfigured.
- Port 135: Windows RPC service can be targeted if exposed.
- Port 139: NetBIOS file sharing may expose shared resources.
- Port 445: SMB has been exploited by malware such as WannaCry.
- Port 2869: Device discovery service should be disabled if not required.

## Recommendations
- Enable Windows Firewall.
- Close unnecessary ports.
- Keep Windows updated.
- Disable unused services.
- Use strong passwords.

## Conclusion
The scan found two active hosts with several open ports. Understanding these services helps identify potential security risks and improve network security.
