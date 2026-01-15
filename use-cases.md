# SOC Use Cases (Windows)

| Use Case | Data Source | Event IDs | Detection | Severity | Response |
|---|---|---|---|---|---|
| Brute Force | Windows Security Logs | 4625 | bruteforce_4625_threshold.spl | Medium | Block IP, lock account |
| Brute Force → Success | Windows Security Logs | 4625, 4624 | bruteforce_then_success_4625_4624.spl | High | Reset creds, MFA, investigate |
| Suspicious PowerShell | Sysmon / Security | 4688 / Sysmon 1 | powershell_encodedcommand.spl | High | Isolate host, collect evidence |
| New User Created | Windows Security Logs | 4720 | new_admin_user_4720.spl | High | Verify change, disable user |
| Added to Admin Group | Windows Security Logs | 4728 | add_user_to_admin_group_4728.spl | Critical | Immediate containment |

