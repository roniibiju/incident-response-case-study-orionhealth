# MITRE ATT&CK Mapping — Orion Health Services Ransomware Incident

| Tactic | Technique | ID | Detail |
|--------|-----------|----|--------|
| Initial Access | Phishing: Spear-phishing Attachment | T1566.001 | Macro-enabled Excel file delivered to finance team member |
| Execution | Command and Scripting Interpreter: Visual Basic | T1059.005 | VBA macro executed dropper on victim endpoint |
| Credential Access | OS Credential Dumping: LSASS Memory | T1003.001 | Mimikatz used to extract credentials from LSASS process |
| Lateral Movement | Use Alternate Authentication Material: Pass the Hash | T1550.002 | Harvested NTLM hashes used to authenticate to internal systems |
| Impact | Data Encrypted for Impact | T1486 | Ransomware deployed across file server, HR/finance systems, and backup server |
