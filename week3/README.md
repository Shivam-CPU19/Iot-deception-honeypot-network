# Week 3 — Log Parsing and Threat Intelligence Extraction

## Objective
Write Python scripts to parse the raw attack logs and extract 
key Indicators of Compromise (IoCs).

## What I Did

### 1. Analyzed Raw Logs
- Examined `cowrie.json` and `cowrie.log` from Week 2
- Identified different event types in the logs
- Found 12 different event types including:
  - `cowrie.login.success`
  - `cowrie.login.failed`
  - `cowrie.command.input`
  - `cowrie.session.connect`

### 2. Wrote Python Log Parser
- Opened `cowrie.json` using Python
- Used `json.loads()` to parse each line into a dictionary
- Used `entry.get()` to safely extract fields
- Used `if/elif` to differentiate event types

### 3. Extracted IoCs
An IoC (Indicator of Compromise) is evidence that an attack 
occurred. We extracted:
- Attacker IP address
- Timestamps
- Passwords attempted
- Commands executed

### 4. Summary Statistics
- Total Connections  : 7
- Total Failed Logins: 3
- Total Successful   : 5
- Total Commands     : 9

## Result
Clean structured output showing exactly what the attacker did,
when they did it and from where.

## Scripts
- `scripts/parse_logs.py` — main log parser

## Tools Used
- Python 3
- json library
