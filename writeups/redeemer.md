# HTB — Redeemer (Starting Point Tier 0)
**Date:** May 30, 2026
**Difficulty:** Very Easy
**OS:** Linux

## Tasks
* **Task 1:** Which TCP port is open on the machine? **6379**
* **Task 2:** Which service is running on the port that is open on the machine? **redis**
* **Task 3:** What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database. **In-memory Database**
* **Task 4:** Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments. **redis-cli**
* **Task 5:** Which flag is used with the Redis command-line utility to specify the hostname? **-h**
* **Task 6:** Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server? **info**
* **Task 7:** What is the version of the Redis server being used on the target machine? **5.0.7**
* **Task 8:** Which command is used to select the desired database in Redis? **select**
* **Task 9:** How many keys are present inside the database with index 0? **4**
* **Task 10:** Which command is used to obtain all the keys in a database? **keys ***

## Objective
Get the root flag from a misconfigured Redis service.

## Tools Used
- nmap
- redis-cli

## Methodology
1. Ran `nmap` to scan for open ports → found port 6379 running `redis`.
2. Connected to the Redis server using `redis-cli -h <target_ip>`.
3. Used the `info` command to gather statistics and `select 0` to select the database.
4. Listed the keys using `keys *` and found the flag key.
5. Retrieved the flag using `get flag`.

## Key Learning
Redis servers exposed to the public without authentication allow unauthorized users complete access to the database. This is a critical misconfiguration that leads to sensitive data exposure.

## Flag
[03e1d2b376c37ab3f5319922053953eb]