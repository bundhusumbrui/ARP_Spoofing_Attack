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
Therefore Attacker's IP: `10.191.157.40`



Now we will check the Victim's IP.  We will write the same command `ip a` to see the IP address.

![ip address](https://github.com/bundhusumbrui/ARP_Spoofing_Attack/blob/9f7e77de7b6622b0bebc882c90cf21f7ee6a6c58/2.%20Victim's%20IP.png)
Therefore Victim;s IP: `10.191.157.28`

## ⚪Step 2:- Checking for devices and their IPs in the network
To check the devices and IPs connected with a same network, we will use the command `sudo nmap -sn 10.191.157.0/24`.

![ip address](https://github.com/bundhusumbrui/ARP_Spoofing_Attack/blob/9f7e77de7b6622b0bebc882c90cf21f7ee6a6c58/3.%20Checking%20for%20devices.png)

Here,
Attacker's IP: `10.191.157.40`
Victim's IP: `10.191.157.28`
Gateway IP: `10.191.157.152`

## ⚪Step 3:- ARP Behaviour Observation

ARP Behaviour Observation before communication

![ip address]()

ARP Behaviour Observation after ICMP Communication

In Victim's Machine: Pinging every device in the network

![ip address]()

Observed ARP Table:-
![ip address]()

## ⚪Step 4:- Launch Attack From Attacker's Machine
Therefore we know the Victim's IP address, we can began the attack. We will sniff the traffic on the eth0 interface by using `sudo ettercap -T -i eth0 -M arp:remote /10.191.157.28// /10.191.157.152//`

![ip address]()

An ARP spoofing attack is launched from the attacker machine using a network attack framework. The attacker sends forged ARP replies to the victim, falsely associating the attackerʼs MAC address with a trusted IP address.
As a result:
- The victimʼs ARP cache is poisoned
- Traffic is redirected to the attacker
- The attacker gains MITM capabilities

## ⚪Step 5:- ARP Behaviour Observation: After Attacker initiates the MITM attack
In victim's Machine we will use command `arp -n` to observe the ARP table.

![ip address]()

We can see that two different IP addresses has the same MAC address. Hence, we know the victim will know that their packets are being intercepted.

# 📜Conclusion
This project successfully demonstrated an ARP Spoofing (ARP Poisoning) attack within a controlled virtual lab environment to identify security weaknesses in the Address Resolution Protocol. By utilizing a specific setup involving an Attacker Machine (Kali Linux) and a Victim Machine (Ubuntu Linux) on the same Layer-2 virtual network.
The project provides clear evidence that local area networks are highly susceptible to spoofing attacks, emphasizing the need for stricter security measures such as static ARP entries or dynamic ARP inspection.












