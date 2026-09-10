# Hack The Box Writeups

Personal walkthroughs for completed Hack The Box Starting Point machines. Each writeup records the enumeration path, exploitation steps, tools used, and key lessons.

> These notes are for authorized labs and educational use only. Flags are included, so expect spoilers.

## Completed Machines

| # | Machine | Tier | Difficulty | OS | Key skills | Completed |
|---:|---|:---:|---|---|---|---|
| 1 | [Meow](writeups/meow.md) | 0 | Very Easy | Linux | Telnet enumeration and empty credentials | May 26, 2026 |
| 2 | [Fawn](writeups/fawn.md) | 0 | Very Easy | Unix | FTP enumeration and anonymous access | May 29, 2026 |
| 3 | [Dancing](writeups/dancing.md) | 0 | Very Easy | Windows | SMB enumeration and null sessions | May 29, 2026 |
| 4 | [Redeemer](writeups/redeemer.md) | 0 | Very Easy | Linux | Redis enumeration and unauthenticated access | May 30, 2026 |
| 5 | [Appointment](writeups/appointment.md) | 1 | Very Easy | Linux | SQL injection authentication bypass | June 2, 2026 |
| 6 | [Sequel](writeups/sequel.md) | 1 | Very Easy | Linux | MariaDB enumeration and blank credentials | June 3, 2026 |
| 7 | [Crocodile](writeups/crocodile.md) | 1 | Very Easy | Linux | Anonymous FTP and credential reuse | June 4, 2026 |
| 8 | [Responder](writeups/responder.md) | 1 | Very Easy | Windows | LFI, NTLMv2 capture, and WinRM | June 5, 2026 |
| 9 | [Three](writeups/three.md) | 1 | Very Easy | Linux | Virtual-host discovery and S3 misconfiguration | June 8, 2026 |
| 10 | [Archetype](writeups/archetype.md) | 2 | Very Easy | Windows | SMB secrets, MSSQL command execution, and privilege escalation | June 12, 2026 |
| 11 | [Oopsie](writeups/oopsie.md) | 2 | Very Easy | Linux | IDOR, file upload, and SUID path hijacking | June 14, 2026 |
| 12 | [Vaccine](writeups/vaccine.md) | 2 | Easy | Linux | Password cracking, SQL injection, and sudo abuse | June 20, 2026 |
| 13 | [Unified](writeups/unified.md) | 2 | Easy | Linux | Log4Shell, MongoDB, and credential recovery | June 22, 2026 |

## Repository Layout

```text
.
├── README.md       # Writeup index
├── images/         # Screenshots referenced by the writeups
└── writeups/       # One Markdown file per completed machine
```

## Reading the Writeups

Start from the table above or browse the [`writeups/`](writeups/) directory. Commands and screenshots reflect the lab environment at the time each machine was completed.
