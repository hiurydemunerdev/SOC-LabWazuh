# SSH Brute Force Incident Report

## Incident Summary

A simulated SSH brute force attack was conducted from a Kali Linux machine against an Ubuntu server monitored by Wazuh SIEM.

The attack generated multiple failed authentication attempts which were detected and correlated by the SIEM platform.

---

# Incident Details

|       Field        |      Value      |
|--------------------|-----------------|
| Attack Type        | SSH Brute Force |
| Source IP          | 192.168.100.20  |
| Target Host        | ubuntu-soc      |
| Detection Platform | Wazuh SIEM      |
| Severity Level     | Medium / High   |
| Status             | Contained       |

---

# Attack Timeline

| Time  | Event                                     |
|---|---|
| 10:01 | SSH brute force started                   |
| 10:02 | Multiple authentication failures detected |
| 10:03 | Wazuh generated alerts                    |
| 10:04 | Fail2Ban blocked attacker IP              |
| 10:05 | Incident investigation initiated          |

---

# Detection Logic

The attack was detected through:

- SSH authentication failure correlation
- Repeated login attempts
- SIEM event analysis
- Log monitoring

---

# MITRE ATT&CK Mapping

|    Technique    |  ID   |
|-----------------|-------|
| Brute Force     | T1110 |
| Valid Accounts  | T1078 |
| Remote Services | T1021 |

---

# Evidence

## SSH Authentication Failures

Detected multiple:

```text
sshd: authentication failed.
