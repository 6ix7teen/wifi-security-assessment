# wifi-security-assessment

A structured auditing framework, deployment guide, and automation toolkit for assessing the security posture of wireless local area networks (WLANs). This repository provides specialized tools and checklists to evaluate enterprise and residential Wi-Fi infrastructures against modern wireless attacks, configuration weaknesses, and protocol vulnerabilities.

---

## 🎯 Purpose & Scope

This project standardizes wireless network audits to identify entry points that could allow attackers to bypass physical perimeter security. It focuses on identifying, demonstrating, and remediating weaknesses across modern wireless deployments:

* **Pre-Shared Key (PSK) Vulnerabilities:** Auditing WPA2/WPA3 Personal networks for weak passphrases susceptible to offline dictionary cracking attacks.
* **Enterprise Authentication Weaknesses:** Assessing WPA2/WPA3 Enterprise setups (802.1X) for misconfigured certificate validation or vulnerable EAP protocols (e.g., PEAPv0/EAP-MSCHAPv2).
* **Rogue Infrastructure & Spoofing:** Simulating Evil Twin deployments, rogue access points (APs), and wireless deauthentication scenarios to test client resilience.
* **Legacy Protocol Detection:** Scanning for insecure legacy configurations like WEP or WPS (Wi-Fi Protected Setup) that are trivially exploitable.

---

## 🚀 Key Features

* **Automated Triage Scripting:** Automated wrapper scripts for mapping the local RF environment, identifying target BSSIDs, and logging encryption standards.
* **Handshake Capture Automation:** Modular workflows to capture WPA2 4-way handshakes and WPA3 PMKID beacons for localized offline complexity checking.
* **Enterprise Rogue AP Simulators:** Structural setups for launching authorized credential-validation tests against legacy enterprise configurations.
* **Defensive Hardening Baseline:** Complete architectural checklists for implementing robust WPA3 Enterprise profiles, management frame protection (MFP), and wireless client isolation.

---

## 📂 Project Structure

```text
wifi-security-assessment/
├── reconnaissance/
│   ├── air_mapper.sh          # Wrapper for automated local BSSID and channel discovery
│   └── client_tracker.py      # Tracks associated clients on target networks to locate weak links
├── assessment/
│   ├── psk_triage/            # Tools for capturing and verifying 4-way handshakes/PMKIDs
│   └── enterprise_triage/     # Configuration files for auditing 802.1X authentication profiles
├── checklists/
│   ├── residential_audit.md   # Posture checks for standalone and remote-work networks
│   └── enterprise_audit.md    # Rigorous validation checklist for corporate 802.1X deployments
└── README.md                  # Project manual and RF safety guidelines
