Zone Tansfers copy all records of a DNS from a primary server, to and transfers it to a secondary server
1. The secondary server sends an AXFR (full zone transfer request) to the primary server
2. Primary server handles request by sending the Start of Authority Request (SOA), which contain important information about the zone
3. DNS records transfer
4. Primary server confirms transfer completion

# using the inlanefreight.htb domain, and given ip target, I was able to complete a zone transfer 
<img width="1022" height="528" alt="ZoneTransfer" src="https://github.com/user-attachments/assets/b683a313-a2d1-48ee-bce5-f4b2adbf44d1" />

This shows a lot of information about the DNS infrastructure and gives a path for more recon by providing subdomains and ip addresses 
