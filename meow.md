  # HTB — Meow (Starting Point Tier 0)
  **Date:** May 26, 2026
  **Difficulty:** Very Easy
  **OS:** Kali Linux

  ## Objective
  Get the root flag from a misconfigured Telnet service.

  ## Tools Used
  - nmap
  - telnet

  ## Methodology
  1. Ran nmap -sV to find open ports → found port 23 (Telnet)
  2. Connected via telnet, tried root with no password → got shell
  3. Found flag.txt in root's home directory

  ## Key Learning
  Telnet transmits everything in plain text including credentials.
  Default/empty credentials are a critical misconfiguration.
  Real-world equivalent: any exposed service with factory default credentials.

  ## Flag
  [b40abdfe23664587f9c61ecba8a4c19]