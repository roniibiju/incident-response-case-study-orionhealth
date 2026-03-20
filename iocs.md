# Indicators of Compromise — Orion Health Services Ransomware Incident

## Network
- **Overseas IP address** — Authenticated login detected in system logs. Likely used as C2 infrastructure following credential harvesting.

## Tool
- **Mimikatz / in-memory variant** — Deployed against LSASS process to extract plaintext passwords, NTLM hashes, and Kerberos tickets.

## File
- **.orionlock extension** — Custom extension appended to all files encrypted by the ransomware payload.

## Behaviour
- **Anomalous outbound network traffic** — Detected Monday morning prior to ransomware deployment. Consistent with data exfiltration (double extortion TTP).

## Artefact
- **Ransom note on shared drive** — Payment instructions deposited to shared network location. Preserved as forensic evidence.
