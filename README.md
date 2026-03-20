# Incident Response Case Study — Ransomware Attack

> Simulated exercise completed as part of independent cybersecurity study.

## Overview

This case study documents a ransomware incident response exercise conducted on a fictional healthcare technology organisation (Orion Health Services, 250 employees, AU/NZ).

Taking on the role of a Cybersecurity Analyst Graduate, I investigated the full attack chain, identified indicators of compromise, assessed regulatory data breach obligations, and produced a structured executive report with a remediation roadmap.

---

## Scenario

| Detail | Value |
|--------|-------|
| Organisation | Orion Health Services (fictional) |
| Industry | Healthcare Technology |
| Size | 250 employees |
| Jurisdictions | Australia & New Zealand |
| Incident Type | Ransomware — Critical |
| Initial Vector | Phishing email — macro-enabled Excel attachment |
| Ransomware Extension | .orionlock |

---

## Attack Chain

| Step | Tactic | Technique | MITRE ID |
|------|--------|-----------|----------|
| 1 | Initial Access | Spear-phishing attachment | T1566.001 |
| 2 | Execution | Malicious macro / VBA dropper | T1059.005 |
| 3 | Credential Access | Mimikatz — LSASS memory dump | T1003.001 |
| 4 | Lateral Movement | Pass-the-hash with stolen credentials | T1550.002 |
| 5 | Impact | Data encryption — ransomware deployment | T1486 |

---

## Indicators of Compromise (IOCs)

| Type | Indicator | Notes |
|------|-----------|-------|
| Network | Overseas IP (authenticated login) | C2 channel post-credential harvest |
| Tool | Mimikatz / in-memory variant | LSASS credential dumping confirmed |
| File | .orionlock extension | Applied to all encrypted files |
| Behaviour | Anomalous outbound traffic | Likely pre-encryption exfiltration |
| Artefact | Ransom note on shared drive | Preserved as forensic evidence |

---

## Compromised Data

- **Employee payroll records** — ~250 staff (Privacy Act 1988 AU, NZ Privacy Act 2020)
- **Patient appointment schedules** — Multiple clinic patients (My Health Records Act, Health Information Privacy Code NZ)
- **Internal system credentials** — All staff (immediate reset required)

---

## Systems Affected

- File server — fully encrypted
- HR & finance systems — fully encrypted
- Backup server — partially encrypted

---

## Skills Demonstrated

- Threat analysis and attack chain reconstruction (MITRE ATT&CK)
- IOC identification and documentation
- Regulatory and compliance assessment (AU/NZ privacy law)
- Executive incident report writing

---

## Repository Contents

| File | Description |
|------|-------------|
| `report/executive-report.docx` | Full executive incident report |
| `web/index.html` | Portfolio web page (plain HTML) |
| `iocs.md` | IOC reference document |
| `mitre-mapping.md` | MITRE ATT&CK tactic and technique mapping |

---

## Disclaimer

All organisation names, individuals, systems, and events in this exercise are entirely fictional. This was completed as a self-directed learning exercise and does not represent real commercial experience.
```

---

**FOLDER STRUCTURE**
```
incident-response-case-study/
│
├── README.md
├── report/
│   └── executive-report.docx
├── web/
│   └── index.html
├── iocs.md
└── mitre-mapping.md
