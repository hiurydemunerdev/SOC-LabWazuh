# SSH Brute Force Incident Response Playbook

## Objective

Provide a standardized response procedure for SSH brute force attacks detected by Wazuh SIEM.

---

# Detection Indicators

Possible indicators include:

- Multiple SSH authentication failures
- Repeated login attempts
- Multiple events from same source IP
- High authentication failure volume
- Fail2Ban alerts

---

# Detection Queries

## Failed SSH Logins

```text
rule.description:"sshd: authentication failed."
```

---

## Source IP Investigation

```text
data.srcip:"192.168.100.20"
```

---

## High Severity Events

```text
rule.level:[10 TO 15]
```

---

# Incident Response Procedure

## 1. Identification

- Confirm brute force activity
- Identify source IP
- Determine targeted accounts
- Review authentication logs

---

## 2. Containment

- Block attacker IP using UFW
- Enable Fail2Ban protections
- Terminate suspicious SSH sessions
- Monitor additional login attempts

---

## 3. Investigation

- Review Wazuh alerts
- Analyze attack timeline
- Identify persistence attempts
- Investigate privilege escalation

---

## 4. Eradication

- Remove malicious users
- Reset compromised credentials
- Review SSH configurations
- Remove persistence mechanisms

---

## 5. Recovery

- Restore secure access
- Monitor environment
- Validate system integrity
- Continue SIEM monitoring

---

# MITRE ATT&CK Mapping

| Technique | ID |
|---|---|
| Brute Force | T1110 |
| Valid Accounts | T1078 |
| Remote Services | T1021 |

---

# Tools Used

- Wazuh SIEM
- Fail2Ban
- UFW Firewall
- Ubuntu Linux
- SSH
- Threat Hunting Queries

---

# Skills Demonstrated

- Incident Response
- Threat Hunting
- SIEM Investigation
- Attack Containment
- MITRE ATT&CK Mapping
- Linux Security
