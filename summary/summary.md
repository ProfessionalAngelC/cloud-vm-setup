# Week 1: Windows EC2 Virtual Machine / Cloud Environment Setup

## Objective
Launch and configure a Windows Server 2022 EC2 instance to practice cloud compute, networking, storage, and access control, creating a safe environment for testing internal services.

## What Was Done
- Provisioned a **t3.micro Windows Server 2022 EC2 instance** in AWS  
- Configured a **security group** (`portfolio-windows-sg`) for RDP access  
- Generated and retrieved **Administrator password** using a key pair  
- Successfully connected via **Remote Desktop (RDP)** from a local Windows 11 machine  
- Installed **IIS web server** and verified functionality through the browser  
- Captured all steps with **screenshots**  
- Created an **architecture/network diagram** for visual documentation  

## Problem Solved / Value
This setup provides a secure, isolated virtual environment for testing and development. It allows internal services, like file sharing or web servers, to run safely without impacting production systems. This project demonstrates foundational cloud skills, including instance provisioning, access management, networking, storage attachment, and service installation.

## Portfolio Deliverables
- `screenshots/` folder:
  - EC2 running instance screenshot
  - Administrator password retrieval screenshot
  - RDP-connected desktop screenshot
  - IIS web server screenshot
- `diagrams/vm-network-diagram.png`  
- `setup-guide.md` with step-by-step instructions  
- `README.md` linking all resources and summarizing the project
