# Week 4 — Visualization and Attack Dashboard

## Objective
Transform the raw attack log data from Week 3 into visual charts and
an interactive geographic map to present threat intelligence clearly.

## What I Did

### 1. Installed Required Libraries
- Activated Cowrie virtual environment
- Installed `matplotlib`, `numpy`, `requests`, and `folium`
- All installed inside `cowrie-env` to keep dependencies isolated

### 2. Built Attack Dashboard
- Wrote `dashboard.py` to read parsed data from `cowrie.json`
- Generated a **bar chart** showing connections, logins and commands
- Generated a **pie chart** showing failed vs successful login ratio
- Saved as `dashboard.png` and `pie_chart.png`

### 3. Built Geographic Attack Map
- Wrote `geo_map.py` to plot attacker IPs on a world map
- Used `requests` to call a geolocation API for each IP
- Used `folium` to render an interactive HTML map with markers
- Used public IP `8.8.8.8` as demo (lab uses private 192.168.56.x IPs)
- Saved as `attack_map.html`

### 4. Verified Outputs
- Opened `dashboard.png` and `pie_chart.png` — charts rendered correctly
- Opened `attack_map.html` in browser — map loaded with attacker marker
- All data matched the Week 3 parser summary statistics

## Result
Visual attack dashboard and interactive world map successfully generated,
turning raw honeypot logs into clear, presentable threat intelligence.

## Evidence
- `screenshots/dashboard.png` — bar chart of attack statistics
- `screenshots/pie_chart.png` — login success vs failure pie chart
- `attack_map.html` — interactive map of attacker geolocation

## Scripts
- `scripts/dashboard.py` — generates bar and pie charts
- `scripts/geo_map.py` — generates interactive attack map

## Tools Used
- Python 3
- matplotlib — chart generation
- folium — interactive map
- requests — geolocation API calls
