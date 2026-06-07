# Phase 1: Building My Cybersecurity Lab from Scratch
**Date:** June 8, 2026

Welcome to the first update of my summer cybersecurity project. Over the next few months, I am building **CyberDeck**—a self-hosted security learning dashboard—while simultaneously attacking machines on HackTheBox. 

Phase 1 (Weeks 1 & 2) was all about infrastructure, Linux administration, and establishing a secure baseline. Here is a look at how it went.

## What I Set Up
I spent the first two weeks provisioning the environments and underlying infrastructure for this project:
* **The Target (Ubuntu Server 24.04):** Built a headless VM on VirtualBox. I installed and configured the core LAMP stack (Apache, MySQL, PHP) and Python3, and mapped my local DNS so the server is reachable at `cyberdeck.local`.
* **The Attacker (Kali Linux):** Flashed bare-metal Kali onto a spare laptop to serve as my dedicated offensive machine, prepping tools like nmap, Wireshark, and Burp Suite.
* **Remote Admin:** Configured Termux on my phone so I can SSH into my server and run sysadmin health checks on the go.
* **Automation:** Wrote a bash script to automatically dump and compress my MySQL database, scheduled via a nightly `cron` job.

The most important part of this phase was securing the server. I locked down the firewall (UFW) to only allow HTTP, HTTPS, and a custom SSH port (2222). I disabled root login, enforced key-based SSH authentication, and installed Fail2Ban to automatically monitor my auth logs and block brute-force attempts. 

I also knocked out my first 9 machines on HackTheBox (all of Tier 0 and Tier 1), documenting my methodology for each.

## What Surprised Me
Using Wireshark to capture my own traffic was a massive wake-up call. I intercepted a login request to my own Apache server, and seeing my HTTP headers, URL parameters, and plain-text data entirely readable to anyone on the network bridged the gap between theoretical security and actual vulnerability. It proved exactly why setting up SSL/HTTPS later in this project is non-negotiable.

## What I'd Do Differently
Context switching between acting as a SysAdmin configuring a server, and acting as a technical writer documenting it, was jarring. Moving forward, I am utilizing VS Code's "Remote - SSH" extension to edit server files and manage Git commits directly from my main laptop, which completely eliminates the friction of using terminal-based text editors for large code files.

## What's Next
Tomorrow kicks off **Phase 2: Build**. I will be shifting from sysadmin mode back into developer mode. 

I'll be building the actual CyberDeck web app using PHP, wiring up the frontend dashboard, and writing a Python cron job that automatically syncs my live HackTheBox stats via their API. Crucially, I am building the login and dashboard to be *intentionally vulnerable* (SQL injection, XSS, broken access control) so I can attack my own code in Phase 3.

— DJ