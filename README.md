# networkwalks-B084-week1-Cybersecurity-lab-setup
CyberSecurity Lab Setup
# Cybersecurity Testing Lab Setup Using VirtualBox

## 📌 Project Overview

This project documents the setup of a cybersecurity testing lab on a Windows PC using Oracle VirtualBox and Kali Linux.

The lab was created as part of a practical cybersecurity assignment to establish a virtual environment for learning and performing authorized security testing.

The setup follows the requirements provided in the assignment, including the installation of Kali Linux, NAT Network configuration, IP address assignment, clipboard and drag-and-drop integration, shared folders, and internet connectivity.

## 🎯 Objectives

The objectives of this practical were to:

- Set up Oracle VirtualBox as the virtualization platform.
- Install Kali Linux as the attacking machine.
- Create a NAT Network using the `10.0.0.0/24` subnet.
- Configure Kali Linux with the IP address `10.0.0.2/24`.
- Enable clipboard sharing and drag-and-drop in the virtual machine settings.
- Enable a shared folder linking the host's `/downloads` folder to Kali Linux.
- Ensure Kali Linux has full internet access.

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Oracle VirtualBox | Virtualization platform |
| Kali Linux 2026.2 | Attacking machine |
| NAT Network | Virtual network for the lab |
| IPv4 | Network addressing |

## ⚙️ Setup Procedure

### Step 1: Set Up the Virtual Machine

Oracle VirtualBox was used as the base virtualization platform. A Kali Linux virtual machine was created with the following resources:

- **Operating System:** Kali Linux 2026.2
- **Architecture:** 64-bit (AMD64)
- **Base Memory:** 8 GB
- **Processors:** 4
- **Virtual Disk:** Approximately 80 GB

**Screenshot: Virtual Machine Setup**

![Kali Linux Virtual Machine Setup](screenshots/01-virtualbox-vm-configuration.png)

### Step 2: Set Up the NAT Network

A NAT Network named `NatNetwork` was created in VirtualBox using the required IPv4 subnet.

The network settings were configured as follows:

| Setting | Value |
|---|---|
| Network Name | `NatNetwork` |
| IPv4 Subnet | `10.0.0.0/24` |
| DHCP Server | Enabled |

This establishes the virtual network required for the lab.

**Screenshot: NAT Network Setup**

![VirtualBox NAT Network Setup](screenshots/02-nat-network-configuration.png)

### Step 3: Configure the Kali Linux IP Address

The IPv4 settings for the Kali Linux wired connection were opened to configure the required address.

The assignment specifies the following:

| Setting | Required Value |
|---|---|
| IPv4 Address | `10.0.0.2` |
| Subnet Prefix | `/24` |
| Network | `10.0.0.0/24` |

**Screenshot: Kali Linux IPv4 Settings**

![Kali Linux IPv4 Settings](screenshots/03-kali-ipv4-configuration.png)

*Note: The screenshot documents the IPv4 settings interface. The final IP assignment should be verified from Kali Linux before considering this requirement complete.*

### Step 4: Enable Clipboard and Drag-and-Drop

The virtual machine settings should allow clipboard sharing and drag-and-drop between Windows and Kali Linux.

The required settings are:

- **Shared Clipboard:** Bidirectional
- **Drag and Drop:** Bidirectional

These features make it easier to transfer text and files between the host operating system and the virtual machine.

### Step 5: Enable the Shared Folder

A shared folder should be configured to connect the host's `/downloads` folder to Kali Linux.

The required host folder is:

`/downloads`

The shared folder allows files to be exchanged between Windows and Kali Linux without relying on manual downloads from external sources.

### Step 6: Verify Internet Connectivity

Kali Linux must have full internet access as required by the assignment.

After completing the network setup, connectivity can be checked using:

```bash
ping -c 4 1.1.1.1
```

To check DNS resolution, run:

```bash
getent hosts google.com
```

These tests help verify connectivity to an external IP address and the ability to resolve domain names.

The results should be recorded after the tests are performed.

## 📋 Assignment Requirements Checklist

| Requirement | Status |
|---|---|
| Oracle VirtualBox set up | Completed |
| Kali Linux virtual machine created | Completed |
| NAT Network created | Completed |
| Network subnet set to `10.0.0.0/24` | Configured |
| Kali Linux IP set to `10.0.0.2/24` | Requires verification |
| Clipboard sharing enabled | Requires verification |
| Drag-and-drop enabled | Requires verification |
| Host `/downloads` folder shared | Requires verification |
| Full internet access verified | Requires testing |

*The checklist distinguishes settings shown in the supplied screenshots from requirements that still need confirmation.*


## 🎓 Conclusion

This practical involved setting up a Kali Linux virtual machine using Oracle VirtualBox and preparing the network environment according to the cybersecurity lab assignment requirements.

The lab provides a foundation for future cybersecurity exercises, including networking practice, vulnerability assessment, and authorized penetration testing.

Further verification of clipboard sharing, drag-and-drop, shared folders, IP addressing, and internet access will ensure that all assignment requirements are satisfied.

## ⚠️ Disclaimer

This lab is intended for educational purposes and authorized cybersecurity testing only.
