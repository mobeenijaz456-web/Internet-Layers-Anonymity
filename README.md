# Internet-Layers-Anonymity
Documenting my journey of Cybersecurity Journey.



# Day 4 - Layers of Internet & Anonymity [Kali Linux]

Basic notes and commands for understanding internet layers and anonymity tools on Kali Linux.

## Topics
1.  Layers of Internet
2.  URL vs URI
3.  Change User Agent
4.  Change MAC Address
5.  VPN vs Proxy vs Tor
6.  DNS Leak Test
7.  Tor Browser

---

### 1. Layers of Internet
- **Surface Web**: Indexed by Google. Ex: YouTube, Wikipedia
- **Deep Web**: Not indexed. Needs login. Ex: Gmail, Bank
- **Dark Web**: Part of Deep Web. Access via Tor. Ex: .onion sites

### 2. URL vs URI
- **URL**: `https://github.com` - Location of resource
- **URI**: `mailto:test@email.com` - Identifier of resource

### 3. Change User Agent on Kali/Firefox
Firefox > `F12` > Settings icon > "Enable responsive design mode" > Select User Agent
Or use extension: `User-Agent Switcher`

### 4. Change MAC Address on Kali

# Check interface
`ip a`

# Turn interface down
`sudo ifconfig eth0 down`

# Change to random MAC
`sudo macchanger -r eth0`

# Turn interface up
`sudo ifconfig eth0 up `

# Verify
`macchanger -s wlan0`
### 5. Auto Change MAC on Reboot - Kali
`sudo nano /etc/network/interfaces
Add this at bottom:
post-up macchanger -r wlan0
Save and reboot.`

### 6. VPN vs Proxy vs Tor
`Tool | Use | Speed | Anonymity
**VPN** | All traffic encrypted | Medium | Hides from ISP
**Proxy** | Single app/browser | Fast | Low
**Tor** | 3 hop routing | Slow | High`
### 7. DNS Leak Test
Test if VPN is leaking DNS:
Website: `dnsleaktest.com`

### 8. Tor Browser on Kali
`sudo apt update
sudo apt install torbrowser-launcher -y
torbrowser-launcher
Download from: torproject.org`

---

Connect With Me
Let’s connect and learn together!
LinkedIn: [www.linkedin.com/in/mobeen-ijaz-a81782329]
Email: [Mobeenijaz456@gmail.com]

#100DaysOfCyberSec #CyberSecurity #Networking #BSIT #LearnInPublic
