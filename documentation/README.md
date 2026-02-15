Lab Overview

This lab simulates a standard enterprise Cyberark Privileged Access Management deployment.
The goal is to demonstrate understanding of:

- Privileged account onboarding
- Secure session management
- Password rotation policies
- Centralized access control
- Audit and monitoring capabilities

## Lab Environment Note 

Due to enterprise licensing requirements of CyberArk, this lab simulates real-world privileged access workflows using documented enterprise deployment architecture.

All flows are based on official CyberArk architecture and operational best practices

---

Environment Assumptions

This lab is designed around a typical enterprise environment:

- Windows servers with local administrator accounts
- Service accounts requiring password management 
- RDP/SSH administative access
- Central CyberArk Vault deployment

---

Core Security Controls Implemented

Privileged Account Onboarding 

- Privileged accounts are identified on target systems
- Accounts are stored inside CyberArk Safes
- Platform policies enforce password standards 
- Credentials are validated upon onboarding

---

Privileged Session Management

- Users request access via Password Vault Web Access (PVWA)
- Access is verified against policy
- Sessions are launched through Privileged Session Manager (PSM)
- Credentials are injected automatically 
- Sessions are recorded and audited

Automatic  Password Rotation

- Central Policy Manager (CPM) retrieves credential from Vault
- Password is changed on target system 
- Vault updates stored credential
- Verification confirms successsful rotation

---

Risk Mitigation & Security Impact

This implementation reduces enterprise risk by:

- Eliminating shared privileged credentials
- Removing hardcoded passwords
- Enforcing least privilege access
- Preventing lateral movement
- Providing full session accountability

---

Real World Enterprise Value

CyberArk PAM helps organizations:

- Meet compliance requirements (SOX, HIPAA, PCI-DSS)
- Enfirce Zero Trust security principles
- Reduce insider threat risk 
- Protect domain and infrastructure administrators

