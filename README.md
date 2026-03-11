# -OIBSIP_cybersecurity_task1

# Nmap Scan Report 
## Scan Summary
- **Date of Scan**: 2026-03-11
- **Target Host**: (IP: 192.168.8.16)
- **Scan Duration**: 2.51 seconds
- **Latency**: 0.00053s
- **Closed Ports**: 97 TCP ports (reset)

## Open Ports and Services
The following ports were found to be open on the target system:

1. **Port 135 (TCP)**: **msrpc** (Microsoft Remote Procedure Call)
   - **Service**: This service is used for inter-process communication within Windows networks.
   - **Security Risk**: MSRPC is often targeted by attackers. Proper network segmentation is advised to minimize exposure.

2. **Port 139 (TCP)**: **netbios-ssn** (NetBIOS Session Service)
   - **Service**: NetBIOS is used for file sharing and printer services on Windows.
   - **Security Risk**: Port 139 is often exploited for brute-force attacks. It is recommended to block this port if not needed.

3. **Port 445 (TCP)**: **microsoft-ds** (Microsoft Directory Services)
   - **Service**: This port is used for SMB over TCP/IP and is essential for file sharing, printer sharing, and Windows domain services.
   - **Security Risk**: Port 445 has been a major target for ransomware attacks (e.g., WannaCry). This port should be restricted from external access.

## Security Recommendations
1. **Firewall Configuration**: If these services are not needed, block these ports using a firewall (either locally or on your router).
2. **Service Patching**: Ensure that all services related to MSRPC, NetBIOS, and SMB are updated to avoid known vulnerabilities.
3. **Limit Exposure**: Restrict access to these ports by allowing only trusted IP addresses.

## Conclusion
The Nmap scan found several open ports related to Microsoft networking services. While these services are crucial in a Windows environment, they can expose the system to security risks if improperly configured. Closing unused ports and restricting access are key steps to enhancing security.

