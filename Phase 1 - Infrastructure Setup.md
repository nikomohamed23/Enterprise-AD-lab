# Phase 1 – Bare-Metal Infrastructure Setup

## Overview
This phase documents the initial setup of a bare-metal virtualization environment using Proxmox VE.  
The objective was to prepare physical hardware, deploy a Type-1 hypervisor, configure management networking, and establish remote administrative access.

This approach was chosen to simulate real-world infrastructure deployment rather than relying on desktop virtualization tools.---

---

## Lab Environment

- **Host Machine:** Dell OptiPlex 3050  
- **Hypervisor:** Proxmox VE  
- **Hostname:** pve.area51.local  
- **Management IP:** 192.168.10.188/24  
- **Gateway:** 192.168.10.1  

---

## Scope of Work

---
### 1. Download ISO 

Download Promxox VE from [(https://www.proxmox.com/en/)]()  

![BIOS Setup](./images/phase1/01-proxmox-website-install.png)

---

### 2. Bootable USB Creation

A bootable Proxmox installation drive was created using Rufus.

![Rufus Setup](./images/phase1/02-rufus-usb-creation.png)

This process involved flashing the Proxmox ISO image to a USB device, enabling the system to perform a bare-metal installation.

---

### 3. BIOS Boot Configuration

The system BIOS was configured to allow booting from external installation media.

![BIOS Setup](./images/phase1/03-bios-boot-order.png)

This step ensures the system can load the Proxmox installer from a USB device, which is a common requirement during OS deployment.

---

### 4. Proxmox Installation Process

Once the system is booted from the USB drive and the Proxmox installation process begins, you’ll be greeted by a welcome page with the installer displaying “Install Proxmox VE” along with several options.

![Welcome Installer Screen](./images/phase1/04-proxmox-welcomeinstaller.png)

---

### 5. Administrator Configuration

In the Admin Setup, create a strong and secure password for the ‘root’ account to ensure system protection, and configure the administrator email address. Click Next >

![Network Configuration](./images/phase1/05-proxmox-admin-config-installer.png)

---

### 6. Network Configuration

During installation, a static IP address was assigned to the Proxmox management interface.

![Network Configuration](./images/phase1/06-proxmox-network-config.png)

Configuration used:
- IP Address: 192.168.10.188/24  
- Gateway: 192.168.10.1  
- Hostname: pve.area51.local  
- DNS Server: 127.0.0.1  

This ensures consistent access to the hypervisor across the network.

---

### 7. Installation Process

Wait Until the installation Completes, the system will notify you when it’s complete.

![Installation Progress](./images/phase1/07-proxmox-installing-page.png)

After installation process completed successfully, confirming that Proxmox is ready for use
> **Note:** If the auto-reboot option was selected, it will display the system’s local IP and port configuration.

![Installation Complete](./images/phase1/08-proxmox-installation-complete.png)

At this stage, the system provided the URL required to access the management interface.

---

### 8. Command Line Interface Access

Once Proxmox VE is installed and rebooted, the console will display the login screen along with the HTTPS link to access the web interface in a browser.

![CMD Page](./images/phase1/09-proxmox-cmd-page.png)

---

### 9. Web Interface Access

Access Proxmox web interface was accessed using a browser over port 8006. Using Admin Configurations
![WebUI Login](./images/phase1/10-proxmox-webui-page.png)

After logging in, the dashboard was verified.
![WebUI Login](./images/phase1/11-proxmox-verifycompletion.png)

This confirms that the hypervisor is fully operational and ready for virtual machine deployment.

---

## Result

At the end of Phase 1:

- Proxmox VE successfully deployed on bare-metal hardware  
- Static management networking configured  
- Remote access to the hypervisor confirmed  
- System ready for virtual machine provisioning  

---

## Skills Demonstrated

- Bare-metal OS installation  
- BIOS/UEFI configuration  
- Bootable media creation  
- Static IP addressing  
- Network configuration fundamentals  
- Remote system administration  

---

## Next Phase

Phase 2 will focus on deploying and configuring:

- Windows Server (Active Directory)
- Domain services
- Client systems for user simulation
