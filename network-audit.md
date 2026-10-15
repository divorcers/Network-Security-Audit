# Network Security Audit

## 1. Project Overview
This project explores network security concepts and documents a controlled lab audit.

## 2. Objectives
- Understand IP addresses, ports and network services.
- Learn how network exposure can create security risks.
- Record observations accurately.
- Recommend defensive security improvements.

## 3. Lab Environment
- Operating system: Windows
- Connection type: Wi-Fi
- Inspection method: Windows ipconfig command
- Target: Local computer network configuration
- Authorised scope: Own computer

## 4. Observations
- Windows provides network configuration details through ipconfig.
- The IPv4 address identifies the computer on the local network.
- The subnet mask defines the local network range.
- The default gateway identifies the next-hop device, commonly the router.
* The netstat -ano | findstr LISTENING command was used to inspect listening network ports on the local Windows computer.
* Listening ports may be associated with Windows services or installed applications.
* Further investigation is required before deciding whether any listening port presents a security risk.
* Process IDs (PIDs) from the network connection output can be compared with Windows Task Manager to investigate which processes may be associated with listening ports.
* No services or processes were stopped or modified during this inspection.
* Further checks are needed before determining whether any service requires a security change.
* Windows Security was used to inspect the Windows Defender Firewall status.
* Active network profile: [enter the profile shown]
* Firewall status: [enter the status shown]
* No firewall settings were changed during this audit.

## 5. Potential Risks
5. Potential Risks

* A listening port may expose a service to other devices, depending on its binding address and firewall rules.
* Services that are unnecessary or outdated may increase the computer’s attack surface.
* A listening port alone does not prove a vulnerability; the associated service and access controls must be assessed.
## 6. Recommendations
6. Recommendations

* Keep Windows and installed applications updated.
* Keep Windows Defender Firewall enabled.
* Disable unnecessary services only after confirming their purpose and following reliable guidance.
* Review listening ports alongside the associated process and firewall settings before making security conclusions.

## 7. Conclusion
This project used built-in Windows tools to examine local network configuration, listening ports, associated processes, and firewall status. It demonstrated the importance of identifying exposed services and checking defensive controls before drawing conclusions about security risks. The inspection was limited to my own computer, and no unauthorised scanning or configuration changes were performed.


## 8. Safety and Limitations
All inspection was limited to my own computer and its local configuration. No third-party networks were scanned. The results represent a basic inspection rather than a comprehensive penetration test. Further assessment would be required to confirm whether any specific service presents a vulnerability.