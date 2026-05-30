# Network Port Scanning Lab

## Objective
Discover active devices and open ports on a local network using Nmap and understand network service exposure.

## Tools Used
- Nmap

## Network Range
192.168.x.0/24

## Command Used

```bash
nmap -sS 192.168.x.0/24 -oN scan_results.txt
```

## Results

### Active Hosts Found
- Router
- Windows PC
- Android Device

### Open Ports

#### Router
| Port | Service |
|------|---------|
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |
| 7443 | HTTPS Service |
| 8080 | HTTP Proxy |
| 8443 | HTTPS Alternate |

#### Windows PC
| Port | Service |
|------|---------|
| 135 | MSRPC |
| 139 | NetBIOS |
| 445 | SMB |
| 902 | VMware Service |
| 912 | Apex Mesh |
| 3389 | Remote Desktop (RDP) |

#### Android Device
No open ports detected.

## Security Observations
- Open RDP (3389) may allow remote access if not properly secured.
- SMB (445) should be protected using strong passwords and firewall rules.
- Router management services should only be accessible from trusted devices.

## Learning Outcome
- Learned host discovery and port scanning using Nmap.
- Identified common network services and ports.
- Understood basic network reconnaissance concepts.
- Learned how open ports can affect security.
