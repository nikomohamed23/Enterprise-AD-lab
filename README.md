# Enterprise-AD-lab
# Enterprise Active Directory Lab (Proxmox)

## Overview

This project documents the design and deployment of a simulated enterprise IT environment using Proxmox as a bare-metal hypervisor.

The goal is to replicate real-world IT infrastructure, including Active Directory, networking, and system administration tasks, while demonstrating hands-on experience relevant to IT Support and System Administration roles.

---

## Architecture

* Hypervisor: Proxmox VE (bare-metal)
* Firewall: OPNsense
* Domain Controller: Windows Server 2025
* Secondary Server: Windows Server 2019
* Clients: Windows 10 / Windows 11

---

## Network Design

* Subnet: 192.168.10.0/24
* Gateway: 192.168.10.1 (OPNsense)
* Domain Controller: 192.168.10.90
* Proxmox Host: 192.168.10.188

---

## Project Phases

### Phase 1 — Infrastructure Setup

Provisioned Proxmox VE on bare-metal hardware and configured initial networking.

➡️ [View Details](./Phase1-Infrastructure-Setup.md)

---

### Phase 2 — Active Directory Deployment

Installed and configured Active Directory Domain Services.

➡️ [View Details](./phase-02-active-directory/active-directory.md)

---

### Phase 3 — Networking Configuration

Configured internal networking and routing.

➡️ [View Details](./phase-03-networking/networking.md)

---

### Phase 4 — Domain Join

Joined client machines to the domain and validated authentication.

➡️ [View Details](./phase-04-domain-join/domain-join.md)

---

### Phase 5 — Core Services (DHCP/DNS)

Implemented DHCP and DNS services for network management.

➡️ [View Details](./phase-05-services/dhcp.md)

---

### Phase 6 — Group Policy

Applied domain-level policies to manage user and system behavior.

➡️ [View Details](./phase-06-group-policy/gpo.md)

---

### Phase 7 — Troubleshooting

Documented real-world issues encountered and how they were resolved.

➡️ [View Details](./phase-07-troubleshooting/issues.md)

---

## Skills Demonstrated

* Active Directory Administration
* Networking (IP addressing, DNS, DHCP)
* Virtualization (Proxmox)
* System Deployment
* Troubleshooting and root cause analysis

---

## Documentation & Blog

* Medium Blog: [link]
* LinkedIn Updates: [link]

---

## Future Improvements

* VLAN segmentation
* Security hardening
* Automation with PowerShell
