# OSINT Platform

Open Source Intelligence (OSINT) gathering tool built with Streamlit.

## Project layout

- `osint-v21/app.py` — main Streamlit application entrypoint
- `osint-v21/requirements.txt` — Python dependencies for the app
- `osint-v21/assets/style.css` — shared UI styling
- `osint-v21/utils/helpers.py` — shared utilities for CSS loading, input detection, retry logic, and threat scoring
- `osint-v21/modules/` — OSINT feature modules
  - `reputation.py` — VirusTotal / Shodan / AbuseIPDB reputation analysis
  - `ssl_cert.py` — SSL/TLS certificate intelligence
  - `dns_intel.py` — DNS intelligence via ViewDNS
  - `subdomains.py` — passive subdomain discovery via crt.sh
  - `typosquatting.py` — typosquatting detection via DNSTwist
  - `sherlock_hunt.py` — username hunt using Sherlock
  - `hash_tool.py` — hash generation and integrity checks
  - `network_graph.py` — graph view of domains / IPs / ports
  - `password_security.py` — password strength / security tools
  - `security_hub.py` — security support resources
  - `metadata_inspector.py` — metadata extraction helper module
  - `truecaller_lookup.py` — Truecaller / phone lookup helper module

## Features

The application supports these main workflows:

- IP / Domain reputation analysis
- TLS / SSL certificate intelligence
- DNS intelligence and ViewDNS lookups
- Subdomain discovery
- Typosquatting analysis
- Network graph visualization
- Username hunt via Sherlock
- Breach check using Have I Been Pwned
- Hash generation and integrity verification
- Password security assistance
- Security support hub resources
- Cybersecurity news feed

## Setup

```bash
cd osint-v21
pip install -r requirements.txt
streamlit run app.py
```

## API keys

The app reads API keys from environment variables, typically via a `.env` file:

- `VT_API_KEY` — VirusTotal
- `SHODAN_API_KEY` — Shodan
- `ABUSEIPDB_API_KEY` — AbuseIPDB
- `VIEWDNS_API_KEY` — ViewDNS
- `HIBP_API_KEY` — Have I Been Pwned (for breach checks)

## Notes

Only one README is kept in the repository root. The nested `osint-v21/README.md` has been removed to avoid duplication.