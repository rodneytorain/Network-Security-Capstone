# Network Security Capstone

This project documents a three-VM VirtualBox lab used to test network connectivity, apply UFW firewall controls, and validate traffic behavior with Wireshark.

## Lab Environment

- Windows 11 Client
- Ubuntu Server
- Ubuntu Attack Machine
- Oracle VirtualBox
- UFW
- Wireshark

## Project Overview

The lab was built to establish baseline communication between systems, apply firewall restrictions to the Ubuntu server, and compare ICMP traffic before and after the firewall change.

## 1. Virtual Lab Environment Setup

This screenshot shows the initial VirtualBox lab environment with three virtual machines: a Windows 11 client, an Ubuntu server, and an Ubuntu attack machine.

![Virtual Lab Environment Setup](Screenshots/1.%20Virtual%20Lab%20Environment%20Setup.png)

## 2. Three-VM Lab Running

This screenshot shows the Windows 11 client, Ubuntu server, and Ubuntu attack machine running at the same time in VirtualBox. This confirmed that the full lab environment was operational before connectivity testing began.

![Three-VM Lab Running](Screenshots/2.%20Three-VM%20Lab%20Running.png)

## 3. Successful Ping to Ubuntu Server

The attack machine successfully pinged the Ubuntu server at `192.168.1.6`, confirming that the server was reachable before the firewall restriction was applied.

![Successful Ping to Ubuntu Server](Screenshots/3.%20Successful%20Ping%20to%20Ubuntu%20Server.png)

## 4. Successful Ping to Windows Client

The attack machine successfully pinged the Windows 11 client at `192.168.1.4`, confirming that the client was also reachable during baseline connectivity testing.

![Successful Ping to Windows Client](Screenshots/4.%20Successful%20Ping%20to%20Windows%20Client.png)

## 5. Wireshark Capture Before Firewall Rule

Wireshark captured ICMP Echo Requests and Echo Replies between the attack machine and Ubuntu server, confirming normal two-way communication before the firewall restriction was applied.

![Wireshark Capture Before Firewall Rule](Screenshots/5.%20Wireshark%20Capture%20Before%20Firewall%20Rule.png)

## 6. Server Ping Blocked After Firewall Rule

After the UFW firewall rule was applied to the Ubuntu server, the attack machine could no longer successfully ping the server. The test resulted in 100% packet loss, confirming that the firewall restriction was working.

![Server Ping Blocked After Firewall Rule](Screenshots/6.%20Server%20Ping%20Blocked%20After%20Firewall%20Rule.png)

## 7. Wireshark Capture After Firewall Rule

Wireshark captured ICMP Echo Requests from the attack machine, but no successful replies from the Ubuntu server. This verified that the server was no longer responding to the ping requests after the firewall restriction was applied.

![Wireshark Capture After Firewall Rule](Screenshots/7.%20Wireshark%20Capture%20After%20Firewall%20Rule.png)

## Results

The lab demonstrated that the Ubuntu server was reachable before the firewall restriction was applied and that the UFW rule successfully stopped the server from responding to ICMP ping requests from the attack machine. Wireshark was used to verify the change in traffic behavior before and after the firewall configuration.

## What I Learned

- How to build and run multiple virtual machines in Oracle VirtualBox
- How to test connectivity between systems using ping
- How to apply UFW firewall restrictions on an Ubuntu server
- How to use Wireshark to compare ICMP traffic before and after a firewall change
- How to validate whether a security control is working using both command-line testing and packet analysis
