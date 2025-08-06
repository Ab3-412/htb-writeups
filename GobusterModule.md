Gobuster is a tool that is used to enumerate a Domain to find its Subdomains 

The first step is to obtain a target Domain and IP 
# It is important to edit the /etc/hosts file to assign the Domain to the target IP 
(at least this was required in the htb module since inlanefreight.htb is not a real-world website that will automatically resolve the DNS)
<img width="276" height="18" alt="SettingUpHost" src="https://github.com/user-attachments/assets/32f7b19c-9cd4-489a-adc5-00e21c1aa225" />
The given IP is from an htb lab that was generated to be scanned *this is not a real target's IP*

The next step would be to use the gobuster command by running it against the desired URL and enumerating it using a wordlist. 
*we are looking for Virtual Hosts so we are using gobuster in vhost mode* 
# Gobuster to find Virtual Hosts
*use the --apend-domain flag to attach the listed words to the domain (e.g. admin.inlanefreight.htb, only the word admin would get sent without the append flag)
<img width="1118" height="433" alt="GobusterSubsFound" src="https://github.com/user-attachments/assets/af634a70-7541-4372-8f94-47a62671481d" />
After enumerating the Domain successfully, I was able to answer the HTB lab questions 
