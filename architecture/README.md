# CyberARk PAM - Architecture Overview

## Objective
This section documents the high-level architecture of a Cyberark Privilege Access Management (PAM) deployment. The goal is to demonstrate understanding of core PAM components, access flows, and how privileged credentials are protected in an enterprise environment.

---

## Core CyberArk Components

### 1. Digital Vault 
The Cyberark Digital Vault is the central, hardened respository where privileged credentials are securely stored.
- Credentials are ecrypted at rest and in transit
- Direct access to the Vault is restricted 
- All access is logged and audited

---

### 2. Central Policy Manager (CPM)
The Central Policy Manager is responsible for managing credentials stored in the Vault.
- Automatically rotates passwords based on policy
- Verifies credentials on target systems
- Enforces password complexity and rotation schedules

---

### 3. Privileged Session Manager (PSM)
The Privileged Session Manager provides secure, monitored access to privileged sessions.
- Users connect without seeing the actual password
- Sessions are isolated, recorded, and audited
- Supports RDP, SSH, and web-based access

---

### 4. Password Vault Web Access (PVWA)
PVWA is the web-based interface used by administrators and users.
- Requests and manage privileged access
- Configure safes, platforms, and policies
- Reviews audit logs and session recordings

---

## High-Level Access Flow

1. User requests access through PVWA
2. CyberArk validates the request against policy
3. Credentials are retrieved securely from the Vault
4. Session is launced through PSM
5. Activity is monitored and recorded 
6. Credentials are rotated by CPM after use (if configured)

---

## Security Benefits
- Eliminates standing privileged access
- Prevents credential exposure
- Provides full audit and session recording 
- Enforces least privilege and zero trust principles

---

## Notes
This architecture reflects a standard enterprise CyberArk PAM deployment and forms the foundation for implementing secure privileged access workflows.
