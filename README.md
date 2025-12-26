#  📌 ARP Spoofing Attack Demonstration

##  ⭐ Demonstration of ARP Spoofing Attack in a Virtualised Network Environment

##  ⚪ Overview
This project demonstrates an ARP Spoofing (ARP Poisoning) attack in a controlled virtual lab to highlight security weaknesses in the Address Resolution Protocol (ARP). Since ARP does not authenticate responses, it can be exploited to perform Man-in-the-Middle (MITM) attacks.

The project shows how an attacker can manipulate the victimʼs ARP table and redirect network traffic through the attacker's system.

##  ⚪ Setup
The experiment is performed using two virtual machines on the same virtual 
network:
 - Attacker Machine: Kali Linux (Username: BundhuSumbrui)
 - Victim Machine: Ubuntu Linux (Username: 6606151)

## ⚪ System Architecture
Both virtual machines are connected to the same Layer-2 virtual network, enabling ARP communication and attack execution.

Components:
- Attacker VM (Kali Linux - BundhuSumbrui)
- Victim VM (Ubuntu Linux - 6606151)
- Virtual Network (Bridged / Host-Only)

Attacker can manipulate the victimʼs ARP table and redirect network traffic through the attacker's system.

# 👾STEPS FOR ATTACK
## ⚪Step 1:- Check Attacker's IP and Victim's IP
We will begin by checking our own device's IP address(i.e. Attecker's IP). We will write the command `ip a` to see the IP address.

![ip address](https://github.com/bundhusumbrui/ARP_Spoofing_Attack/blob/7bc3ad5f867e3b9e1b64be6fd21f33afea36f0f2/1.%20Attacker's%20IP.png)

Now we will check the Victim's IP.  We will write the same command `ip a` to see the IP address.



