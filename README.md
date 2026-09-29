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
