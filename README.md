<div align="center">
  
# NETWORKWALKS-B084-WEEK1-PM1
This project involves setting up an efficient cybersecurity lab environment using VirtualBox, Kali Linux and a private NAT network. 
</div>

## Project Overview
This project documents the setup of a Kali Linux virtual machine in VirtualBox for future cybersecurity projects. I imported a prebuilt Kali VM, created a dedicated private NAT Network, manually configured Kali's IPv4 settings, verified connectivity, and created a snapshot of the configured VM.
## Objectives
- Set up VirtualBox and import a prebuilt Kali Linux VM.
- Create a private NAT Network for the virtual Kali lab.
- Configure Kali with a manual IPv4 address, default gateway, and DNS setting.
- Confirm connectivity with the default gateway and an external IP address.
- Create a snapshot that can be restored if recovery is required.
## Lab Architecture
| Component | Configuration |
| --------- | --------------|
| Host OS   | Windows 11    |
| Lab OS    | Kali Linux 2026.3 |
| Network Type  | NAT Network |
| Network Name | NatNetwork |
| Kali IP Address   | 10.0.0.2/24 |
| Default Gateway   | 10.0.0.1 |
| DNS Server   | 8.8.8.8 |
| Future VM IPv4 Range | 10.0.0.3-10.0.0.99 |
# Lab Setup Procedure
## Step 1 - Preparing VirtualBox and Kali Linux
Installed VirtualBox and extracted the Kali Linux 7-zip archive. The extracted folder contained a .vbox configuration file and a .vdi virtual disk file, which were used to register and start the VM.

![](Project%201/PR2.png)
![](Project%201/PR3.png)

## Step 2 - Creating the NAT Network
Opened VirtualBox's Network Manager and configured:
Network name: NatNetwork
IPv4 prefix: 10.0.0.0/24
DHCP server: Enabled

![NAT Network Creation](Project%201/PR1.png)

## Step 3 - Selecting the correct Network Adapter
Under the Kali VM's network settings, set Adapter 1 to NAT Network and selected the previously created network, "NatNetwork".

![Kali Network Adapter](Project%201/PR4.png)

## Step 4 - Configure Kali Linux's IPv4 Settings
In Kali's wired connection settings, changed the IPv4 method to Manual and entered the following:
IPv4 address: 10.0.0.2
Prefix length: 24
Gateway: 10.0.0.1
DNS server: 8.8.8.8

![Manual IPv4 Configuration](Project%201/PR5.png)

## Step 5 - Verify Network Connectivity
I ran two checks in Kali's terminal to test for connectivity:
| Tests | The Output | Outcome |
| --- | ------- | ------- |
| ping -c 5 10.0.0.1 | 0% Packet loss | Successful |
| ping -c 5 8.8.8.8 | 0% Packet loss | Successful |

![Kali Connectivity Tests](Project%201/PR6.png)

These results confirm that the Kali VM could reach the default gateway and an external IP address during the tests.
## Step 6 - Create a Recovery Snapshot 
Created a snapshot named Fresh Kali Save after configuring the VM. It provides a restore point for future projects. The snapshot manager displays the saved snapshot.

![Kali Network Snapshot](Project%201/PR7.png)

## The Outcome
The prebuilt Kali Linux VM was imported successfully, attached to the configured NAT Network, and given a manual IPv4 address. The gateway and external-IP ping tests both returned 0% packet loss, and a fallback snapshot was created.
## Challenges
- Antivirus detection: Microsoft Defender flagged the downloaded Kali Linux `.7z` archive as a potential threat. I used Windows PowerShell to calculate the archive's SHA-256 hash and compared it against the checksum published on the official Kali Linux website. The hashes matched, confirming that the downloaded archive was identical to the official release. After verifying its integrity, I restored the archive and successfully extracted it. 
- Static addressing and DHCP: The VirtualBox NAT Network had DHCP enabled, while Kali was configured with a manual IPv4 address. I assigned 10.0.0.2/24 to Kali, configured 10.0.0.1 as the default gateway, and specified 8.8.8.8 as the DNS server.
## What I Learned
1. Virtualisation: How a prebuilt VM's .vbox configuration and .vdi virtual disk are used in VirtualBox.
2. NAT networking: How a NAT Network creates a shared virtual subnet and gateway for lab VMs.
3. IPv4 addressing: How a manually configured address, subnet prefix, gateway and DNS setting fit together.
4. Connectivity testing: How pinging provides initial evidence of successful connectivity, and why DNS must be tested separately.
5. Recovery planning: How a VM snapshot preserves a baseline for later experiments.
6. Documentation: How screenshots and observed outputs make a technical lab easier to review and reproduce.
## Responsible & Ethical Use
This project and the laboratory environment are strictly used for educational purposes. Any future testing should be limited to systems owned by me or systems where I have clear and explicit permission.
## Resources
- VirtualBox: https://virtualbox.org/wiki/Downloads
- Kali Linux: https://kali.org/get-kali
## Author Information
Ali Fares

Cybersecurity Intern | Networkwalks B084

https://www.linkedin.com/in/ali-fares-86870733a/
## Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity Lab Setup
