# [Machine Name] - HackTheBox Writeup

**Difficulty:** Easy / Medium / Hard / Insane
**OS:** Linux / Windows
**Release Date:** YYYY-MM-DD
**Retire Date:** YYYY-MM-DD

---

## Summary

Brief overview of the machine and key techniques used.

---

## Reconnaissance

### Nmap

```bash
nmap -sC -sV -oA nmap/initial <TARGET_IP>
```

```
# Paste nmap output here
```

### Service Enumeration

Summarize open ports and services found.

---

## Enumeration

### HTTP / Web

Steps taken to enumerate web services (directories, subdomains, technologies, etc.).

### Other Services

Enumerate other services (SMB, FTP, SSH, etc.) as applicable.

---

## Exploitation

### Initial Foothold

Describe the vulnerability or misconfiguration exploited to gain initial access.

```bash
# Commands used
```

---

## Post-Exploitation

### Local Enumeration

```bash
# Enumeration commands (whoami, id, hostname, uname -a, etc.)
```

### Privilege Escalation

Describe the path from low-privilege user to root/Administrator.

```bash
# Commands used for privesc
```

---

## Flags

| Flag | Value |
|------|-------|
| user.txt | `<hash>` |
| root.txt | `<hash>` |

---

## Lessons Learned

- Key takeaways from this machine
- New techniques or tools discovered
- Areas to research further

---

## References

- [Link to relevant CVE / exploit](https://example.com)
- [Tool documentation](https://example.com)
