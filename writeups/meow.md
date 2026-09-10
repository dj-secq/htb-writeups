  # HTB — Meow (Starting Point Tier 0)
  **Date:** May 26, 2026
  **Difficulty:** Very Easy
  **OS:** Kali Linux

  ## Tasks
  * **Task 1:** What does the acronym VM stand for? **Virtual Machine**
  * **Task 2:** What tool do we use to interact with the operating system in order to issue commands via the shell. **terminal**
  * **Task 3:** What service do we use to form our VPN connection into HTB labs? **openvpn**
  * **Task 5:** What tool do we use to test our connection to the target with an ICMP echo request? **ping**
  * **Task 6:** What is the name of the most common tool for finding open ports on a target? **nmap**
  * **Task 7:** What service do we identify on port 23/tcp during our scans? **telnet**
  * **Task 8:** What username is able to log into the target over telnet with a blank password? **root**

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