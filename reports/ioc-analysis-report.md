# IOC Analysis Report

## Objective

Analyze indicators of compromise generated during simulated attacks against the SOC laboratory environment.

---

# Indicators of Compromise (IOC)

| IOC Type | Value |
|---|---|
| Source IP | 192.168.100.20 |
| Attack Type | SSH Brute Force |
| Detection Platform | Wazuh SIEM |
| Persistence Technique | User Creation |
| Reconnaissance Activity | Nmap Scan |

---

# Threat Activity Identified

The following malicious behaviors were identified:

- Port scanning activity
- Multiple failed SSH authentications
- Successful SSH access
- Privilege escalation activity
- Persistence creation through user addition

---

# Detection Evidence

## SSH Authentication Failures

```text
sshd: authentication failed.
```

---

## Privilege Escalation

```text
sudo
```

---

## Persistence Activity

```text
useradd supportsvc
```

---

# MITRE ATT&CK Mapping

| Technique | ID |
|---|---|
| Active Scanning | T1595 |
| Brute Force | T1110 |
| Valid Accounts | T1078 |
| Remote Services | T1021 |
| Account Creation | T1136 |
| Abuse Elevation Control Mechanism | T1548 |

---

# Threat Hunting Queries

## Source IP Investigation

```text
data.srcip:"192.168.100.20"
```

---

## Authentication Failures

```text
rule.description:"sshd: authentication failed."
```

---

## Persistence Detection

```text
useradd
```

---

# Response Actions

- Identified attacker activity
- Investigated SSH events
- Correlated attack timeline
- Applied Fail2Ban containment
- Blocked malicious IP
- Monitored persistence attempts

---

# Skills Demonstrated

- IOC Analysis
- Threat Hunting
- SIEM Investigation
- MITRE ATT&CK Mapping
- Incident Response
- Attack Correlation
- Linux Security Monitoring

---

# Conclusion

The simulated attack activity was successfully detected, investigated and correlated using Wazuh SIEM and Blue Team methodologies.

The environment demonstrates practical SOC operations, threat hunting and incident response capabilities.
