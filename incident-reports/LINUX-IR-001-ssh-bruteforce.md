# LINUX-IR-001 — SSH Brute Force Attempts Followed by Successful Login

## Incident Summary
A series of failed SSH authentication attempts were detected against a local Linux host, followed by a successful login to user `amlk`.

This investigation was performed using Linux authentication logs located in:
- `/var/log/auth.log`

> **Note:** Source IP was `127.0.0.1` (localhost), indicating a controlled lab simulation for SOC training.

---

## Environment
- OS: Ubuntu (WSL)
- Service: OpenSSH Server (`sshd`)
- Log Source: `/var/log/auth.log`

---

## Detection & Evidence

### Evidence 1 — Failed SSH authentication attempts (Brute Force)
Command used:
```bash
sudo grep -i "sshd.*failed password" /var/log/auth.log | tail -n 10

