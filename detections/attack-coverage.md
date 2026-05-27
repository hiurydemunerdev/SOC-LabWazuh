# MITRE ATT&CK Coverage Matrix

## Objective

Document the MITRE ATT&CK techniques covered by the SOC laboratory detections and monitoring capabilities.

---

# ATT&CK Coverage

| Technique | ID | Detection | Status |
|---|---|---|---|
| Active Scanning | T1595 | Nmap Detection Rule | Covered |
| Brute Force | T1110 | SSH Brute Force Detection | Covered |
| Valid Accounts | T1078 | SSH Login Monitoring | Covered |
| Remote Services | T1021 | SSH Activity Detection | Covered |
| Account Creation | T1136 | User Creation Monitoring | Covered |
| Abuse Elevation Control Mechanism | T1548 | Sudo Detection | Covered |

---

# Detection Sources

The following sources are monitored:

- SSH authentication logs
- Sudo activity
- User creation events
- Network reconnaissance indicators
- Authentication failures
- Threat hunting queries

---

# Detection Technologies

- Wazuh SIEM
- Custom Wazuh Rules
- Sigma Rules
- Threat Hunting Queries
- Fail2Ban
- Ubuntu Syslog Monitoring

---

# Example Queries

## Brute Force Detection

```text
rule.description:"sshd: authentication failed."
```

---

## Privilege Escalation

```text
sudo
```

---

## Persistence Detection

```text
useradd
```

---

# Skills Demonstrated

- MITRE ATT&CK Mapping
- Detection Engineering
- Threat Hunting
- SIEM Correlation
- IOC Analysis
- Incident Response
- Blue Team Operations

---

# Conclusion

The SOC laboratory demonstrates practical MITRE ATT&CK aligned detection engineering and threat monitoring capabilities using Wazuh SIEM and Blue Team methodologies.
