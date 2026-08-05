# 🛡️ Home SOC Lab

## Overview

This project documents the creation of my Home Security Operations Center (SOC) using VirtualBox and multiple virtual machines. The purpose of this project is to gain hands-on cybersecurity experience by building a realistic lab environment for log analysis, threat detection, and incident response.

---

## Project Goals

This project is designed to simulate a small Security Operations Center (SOC). Throughout this project I will:

- Build an isolated virtual network.
- Deploy a Security Information and Event Management (SIEM) platform using Splunk Enterprise.
- Collect and analyze Windows Event Logs.
- Simulate attacks using Kali Linux.
- Detect and investigate suspicious activity.
- Document each phase to demonstrate practical cybersecurity skills.

---

# Lab Environment

## Host Machine

- Windows 11 Pro

## Hypervisor

- Oracle VirtualBox

## Virtual Machines

| Machine | Purpose |
|----------|----------|
| Windows 11 | Victim Machine |
| Kali Linux | Attacker Machine |
| Ubuntu Server | SIEM / Log Collection Server |

---

## Lab Architecture

| Machine | Internal IP Address |
|----------|---------------------|
| Windows 11 | 192.168.56.10 |
| Kali Linux | 192.168.56.20 |
| Ubuntu Server | 192.168.56.30 |

---

# Phase 1 – Environment Setup

## Objectives

- Install Oracle VirtualBox
- Create three virtual machines
- Install Windows 11
- Install Kali Linux
- Install Ubuntu Server
- Verify each machine boots successfully

## Screenshots

### VirtualBox

![VirtualBox](Screenshots/Phase1/VirtualBox-Phase1.png)

### Windows 11

![Windows](Screenshots/Phase1/Windows11-Phase1.png)

### Kali Linux

![Kali](Screenshots/Phase1/KaliLinux-Phase1.png)

### Ubuntu Server

![Ubuntu](Screenshots/Phase1/Ubuntu-Phase1.png)

## Skills Learned

- Virtualization
- Operating System Installation
- Virtual Machine Configuration
- Basic Network Planning

---

# Phase 2 – Network Configuration ✅

## Objectives

- Configure an isolated SOC network inside VirtualBox.
- Provide internet access using NAT.
- Configure an Internal Network for secure VM communication.
- Assign static IP addresses.
- Verify connectivity between all virtual machines.

## Network Configuration

| Machine | Role | Internal IP |
|----------|------|-------------|
| Windows 11 | Victim | 192.168.56.10 |
| Kali Linux | Attacker | 192.168.56.20 |
| Ubuntu Server | SIEM | 192.168.56.30 |

## Configuration Completed

- Configured Adapter 1 as **NAT** for internet access.
- Configured Adapter 2 as **Internal Network (SOC-LAB)**.
- Assigned static IP addresses to all virtual machines.
- Configured Ubuntu networking using Netplan.
- Verified successful communication using ICMP (`ping`).

## Connectivity Tests

### Kali Linux → Ubuntu Server

![Kali Ping Ubuntu](Screenshots/Phase2/Kali-ping-ubuntu.png)

### Windows 11 → Ubuntu Server

![Windows Ping Ubuntu](Screenshots/Phase2/windows-ping.png)

## Skills Learned

- VirtualBox Networking
- NAT Networking
- Internal Networks
- Static IP Addressing
- Ubuntu Netplan Configuration
- Windows Network Configuration
- Network Troubleshooting
- ICMP Connectivity Testing

---

# Project Roadmap

- Phase 1 – Environment Setup
- Phase 2 – Network Configuration
- Phase 3 – Install Splunk Enterprise
- Phase 4 – Configure Sysmon & Splunk Universal Forwarder
- Phase 5 – Simulate Attacks with Kali Linux
- Phase 6 – Threat Detection & SIEM Dashboards
- Phase 7 – Incident Response & Documentation

---

# Technologies Used

- Oracle VirtualBox
- Windows 11
- Kali Linux
- Ubuntu Server
- ICMP (Ping)
- Netplan
- Virtual Networking

---

## About This Project

This repository documents my progress as I build a complete home Security Operations Center from the ground up. Each phase includes screenshots, configuration steps, troubleshooting, and lessons learned to demonstrate practical cybersecurity and IT infrastructure skills.
