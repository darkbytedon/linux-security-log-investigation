# Day 11: Linux Security Log Investigation

## 1. Objective
Investigate Linux authentication and system logs to understand how administrative and authentication activity is recorded.

## 2. Environment
- Operating system: Ubuntu on WSL2
- User: dondon
- Working directory: /home/dondon/cybersecurity/day11

## 3. Commands Used
- whoami
- id
- grep
- tail
- journalctl
- systemctl
- ls -lah

## 4. Findings
- Reviewed /var/log/auth.log.
- Identified records of sudo command execution.
- Reviewed sudo session records showing privileged sessions opening and closing.
- Observed WSL Pro service warnings relating to a missing Windows Agent address file.
- No matching failed-authentication events were identified by the filtered search.
- Reviewed recent system journal entries.

## 5. Security Lessons
- Authentication logs can support security investigations.
- Sudo activity provides evidence of privileged commands.
- Search results must be checked in context.
- A missing log match does not prove that an event never occurred.
- System service warnings should be investigated in their environment-specific context.

## 6. Conclusion
The investigation demonstrated how Linux records administrative activity and how an analyst can examine logs to investigate potential security events.

## 7. Limitations
This was a local WSL2 training environment. The available logs do not represent a complete production Linux server audit.
