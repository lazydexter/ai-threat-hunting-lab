Executive Summary:
Malicious ZIP downloaded → Extracted JS → DLL dropped via certutil →
DLL registered with regsvr32 → Scheduled task created →
Persistence established + exfiltration to external IP.

MITRE ATT&CK:
- T1059 (Command Execution)
- T1105 (Ingress Tool Transfer)
- T1053 (Scheduled Task)
- T1071 (Exfiltration)

Severity: HIGH
✅ That’s the end-to-end setup for Phase 1.
👉 Phase 2 will add automation + multiple log sources.
👉 Phase 3 will integrate with SIEM + Threat Intel.
