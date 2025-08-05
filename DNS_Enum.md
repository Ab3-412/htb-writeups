Using the dig command, you can obtain information regarding the domain of a target
<img width="647" height="514" alt="DigCommand" src="https://github.com/user-attachments/assets/427314da-eb67-469b-9c30-ace32a38a974" />

You can also find subdomains by using a wordlist and enumerating the domains. using the -r flag also enables recursive enumeration, so discovered domains will then be investigated further
# inlanefreight is the htb domain that is permitted to scan for modules
Command used: "dnsenum --enum inlanefreight.com -f /usr/share/seclists/Discovery/DNS/subdomains-top1million-20000.txt"
# the following result is revealing the hidden subdomains 
<img width="692" height="274" alt="SubDomainEnum" src="https://github.com/user-attachments/assets/86b1219a-2fb0-479a-83f3-be73a0691b55" />
