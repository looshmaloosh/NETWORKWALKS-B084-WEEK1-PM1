
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
# Lab Setup Procedure
## Step 1 - Preparing VirtualBox and Kali Linux
Installed VirtualBox and extracted the Kali Linux 7-zip archive. The extracted folder contain a .vbox configuration file and a .vsdi virtual disk, where were used to register and start the VM.
## Step 2 - Creating the NAT Network
## Step 3 - Selecting the correct Network Adapter
## Step 4 - Configure Kali Linux's IPv4 Settings
## Step 5 - Verify Network Connectivity
## Step 6 - Create a Recovery Snapshot
# The Outcome
## Challenges
## What I Learned
## Responsible & Ethical Use
This project and the laboratory environment is strictly used for educational purposes. Any future testing should be limited to systems owned by me or systems where I have clear and explicit permission.
## Resources
- VirtualBox: https://virtualbox.org/wiki/Downloads
- Kali Linux: https://kali.org/get-kali
## Author Information
Ali Fares
Cybersecurity Intern | Networkwalks B084

https://www.linkedin.com/in/ali-fares-86870733a/
## Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity Lab Setup
