# Week 1 — Environment Setup and Device Simulation

## Objective
Set up an isolated lab environment and deploy a honeypot 
that simulates a real healthcare IoT device.

## What I Did

### 1. Created Two Virtual Machines
- **Kali Linux** — simulates the attacker
- **Ubuntu Server** — simulates the healthcare IoT server

### 2. Configured Network
- Both VMs connected via Host-Only network (192.168.56.x)
- Ubuntu: 192.168.56.102
- Kali: 192.168.56.101

### 3. Installed Cowrie
- Cowrie is a fake SSH server that accepts any password
- It logs everything the attacker does
- Runs on port 2222

### 4. Simulated Healthcare IoT Device
- Changed hostname to `vitals-monitor-04`
- Makes the machine look like a real patient vitals monitor
- Attacker has no idea it's a trap

## Result
Honeypot successfully running on port 2222, 
simulating a real healthcare device, ready to trap attackers.

## Tools Used
- VirtualBox
- Ubuntu Server
- Cowrie SSH Honeypot
- Python 3
