## Attack Simulation Summary (WIP)

SIEM used:          Splunk Enterprise
Data Sources:       Windows event logs, Sysmon, Linux auth logs
Attack coverage:    Credential attacks

More attacks to be covered: 
suspicious PowerShell
malware download persistence
privilege escalation

1. Windows events generated:
-   Failed logons (4625)
-   Successful logon (4624)

To be covered:
-   Suspicious PowerShell execution (Event ID 4104 + Sysmon 1)
-   Download of payload via PowerShell (Sysmon 11)
-   Persistence via scheduled task (4698)

2. Linux events generated:
-   SSH brute force attempts
-   Successful SSH login
-   Privilege escalation (sudo failures)
-   Suspicious file creation in /tmp

## Splunk filters used
1. index=* EventCode=4625 host="windows"
2. index=* EventCode=4624 host="windows"
