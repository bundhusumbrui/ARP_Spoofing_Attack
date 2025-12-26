#  📌 ARP Spoofing Attack Demonstration

##  ⭐ Demonstration of ARP Spoofing Attack in a Virtualised Network Environment

##  ⚪ Overview
This project demonstrates an ARP Spoofing (ARP Poisoning) attack in a controlled virtual lab to highlight security weaknesses in the Address Resolution Protocol (ARP). Since ARP does not authenticate responses, it can be exploited to perform Man-in-the-Middle (MITM) attacks.

The project shows how an attacker can manipulate the victimʼs ARP table and 
redirect network traffic through the attacker's system.

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
