# HTB — Fawn (Starting Point Tier 0)
**Date:** May 29, 2026
**Difficulty:** Very Easy
**OS:** Unix

## Tasks
* **Task 1:** What does the 3-letter acronym FTP stand for? **File Transfer Protocol**
* **Task 2:** Which port does the FTP service listen on usually? **21**
* **Task 3:** FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol? **SFTP**
* **Task 4:** What is the command we can use to send an ICMP echo request to test our connection to the target? **ping**
* **Task 5:** From your scans, what version is FTP running on the target? **vsftpd 3.0.3**
* **Task 6:** From your scans, what OS type is running on the target? **Unix**
* **Task 7:** What is the command we need to run in order to display the 'ftp' client help menu? **ftp -?**
* **Task 8:** What is username that is used over FTP when you want to log in without having an account? **anonymous**
* **Task 9:** What is the response code we get for the FTP message 'Login successful'? **230**
* **Task 10:** There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system. **ls**
* **Task 11:** What is the command used to download the file we found on the FTP server? **get**

## Objective
Get the root flag from a misconfigured FTP service.

## Tools Used
- nmap
- ftp

## Methodology
1. Ran nmap -sV to find open ports → found port 21 (FTP) running vsftpd 3.0.3.
2. Connected via ftp, logged in using the 'anonymous' username with a blank password.
3. Listed files using the `ls` command and found the flag file.
4. Downloaded the flag to the local machine using the `get` command.

## Key Learning
FTP transmits data in plain text, making it vulnerable to interception.
Allowing anonymous login without restrictions is a critical misconfiguration that can expose sensitive files to unauthorized users.

## Flag
[035db21c881520061c53e0536e44f815]