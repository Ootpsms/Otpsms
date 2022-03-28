# About
![info](https://cdn.discordapp.com/attachments/909717830461698078/950213007856795648/image.png)

***

**Note: _This Methods need spoofable servers!_**

A reflection amplification attack is a technique that allows attackers to both magnify the amount of malicious traffic they can generate and obscure the sources of the attack traffic. This type of distributed denial-of-service (DDoS) attack overwhelms the target, causing disruption or outage of systems and services.

# Spoof Hostings

**Wiki**: https://en.wikipedia.org/wiki/IP_address_spoofing

**Checker**: https://github.com/MHProDev/IPHM-Checker


# Scanning

## zmap
```
apt install zmap
zmap -p53 --output-filter='sport=53' -Mudp --probe-args=file:dns.pkt -f "saddr udp_pkt_size" -o dns.txt
```
Full document in https://github.com/Phenomite/AMP-Research