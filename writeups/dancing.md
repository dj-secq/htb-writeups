# HTB — Dancing (Starting Point Tier 0)
**Date:** May 29, 2026
**Difficulty:** Very Easy
**OS:** Windows

## Tasks
* **Task 1:** What does the 3-letter acronym SMB stand for? **Server Message Block**
* **Task 2:** What port does SMB use to operate at? **445**
* **Task 3:** What is the service name for port 445 that came up in our Nmap scan? **microsoft-ds**
* **Task 4:** What is the 'flag' or 'switch' that we can use with the smbclient utility to 'list' the available shares on Dancing **-L**
* **Task 5:** How many shares are there on Dancing? **4**
* **Task 6:** What is the name of the share we are able to access in the end with a blank password? **WorkShares**
* **Task 7:** What is the command we can use within the SMB shell to download the files we find? **get**

## Objective
Get the root flag from a misconfigured SMB share.

## Tools Used
- nmap
- smbclient

## Methodology
1. Ran `nmap` to scan for open ports → found port 445 running `microsoft-ds` (SMB).
2. Used `smbclient -L` to enumerate and list available shares on the target.
3. Successfully connected to the 'WorkShares' share using a blank password.
4. Navigated the share and downloaded the flag to the local machine using the `get` command.

## Key Learning
Exposing SMB shares on a network without proper authentication mechanisms (e.g., allowing blank passwords or anonymous access) is a critical misconfiguration. It allows unauthorized users to read or exfiltrate sensitive files and directories.

## Flag
[5f61c10dffbc77a704d76016a22f1664]