# The HTB Footprinting Module teaches you how to scan a network and it's devices, and gathering information on various services running
# I started this github towards the end of the Footprinting Module. I will be going back through to complete this writeup eventually. 
________________________________________________________________________________________________________________________________________________________________
Oracle TNS - communication protocol that facilitates communication between ORacle databases and other applications over the network
  * Supported protocols: IPX/SPX, TCP/IP, IPv6, and SSL/TLS
  * Default Port: 1521 (TNS listener)
  * Configuration files: tnsnames.ora and listener.ora --> located in the $ORACLE_HOME/network/admin
  * Oracle Databses can be protected by using PlsqlExclusionLists in the $ORACLE_HOME/sqldeveloper directory. It is basically a blacklist for PL/SQL packages

  * Tools Used:
      * odat.py - this is used to enumerate the Oracle Database
      * nmap - common network scanning tool
        
  * Solving Quicklab:
    
Step 1: nmap the target IP
sudo nmap 10.129.***.** -p1521 --open -sV
Screenshot: <img width="1101" height="279" alt="nmap-OracleTNS" src="https://github.com/user-attachments/assets/b8d6c421-00fd-489e-b28a-4a04626efc81" />
# I see here that the default port 1521 is open and running oracle-tns

Step 2: use enumeration tools to find the System Identifier (used in the connection proccess to find the desired instance)
# I will be sticking with nmap for this problem and using a common brute force script 
sudo nmap 10.129.***.** -p1521 --open -sV --script oracle-sid-brute 
Screenshot: <img width="1007" height="328" alt="BruteForce_OracleTNS" src="https://github.com/user-attachments/assets/9974c3cf-1c04-42ff-91b9-f939ed58d09e" />
# I found that the SID is XE

Step 3: use enumeration tool to find valid credentials
# I have found the valid credentials, but I must return to this module after setting up sqlplus properly 


