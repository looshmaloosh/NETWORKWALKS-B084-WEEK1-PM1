
# NETWORKWALKS-B084-WEEK1-PM1
This project involves setting up an efficient cybersecurity lab environment using VirtualBox, Kali Linux and a private NAT network. 
## Project Overview
This project documents the setup of a Kali Linux virtual machine in Virtualbox for future cybersecurity projects. I imported a prebuilt Kali VM, created a dedicated private NAT Network, manually configured Kali's IPv4 settings, verified connectivity, and saved a VM snapshot of the current VM.
## Objectives
- Set up VirtualBox and import a prebuilt Kali Linux VM.
- Create a private NAT Network for the virtual kali lab.
- COnfigure Kali with a manual IPv4 address, default gateway, and DNS setting.
- Confirm connectivity with the default gateway and an external IP address.
- Save a snapshot to fallback to when recovery is needed.
## Lab Architecture
| Component | Configuration |
| --------- | --------------|
| HOST OS   | Windows 11    |
| LAB OS    | Kali Linux 2026.3 |
| Virtual Network Name    | NAT Network |
| KALI IP Address   | 10.0.0.2/24 |
| Default Gateway   | 10.0.0.1 |
| DNS Server   | 8.8.8.8 |
| Allowable IP Range | 10.0.0.3-10.0.0.99 |
