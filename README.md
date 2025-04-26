
# 🎮 Game Server Hosting 🎮 

## **Overview**

This documentaion serves the purpose of explaining a personal project of mine over the duration of the past months/years.

The goal in mind was a stable, secure, efficent and easy game server hosting setup, for either myself, friends or if need be the general public.

And just because I am a giant nerd who saw the opportunity to do something not many others have been able to achieve.

### **Setup**

1.  **Machine 1: Cloud VPS (Panel Host / VPN Endpoint)**
    * **Role:** Hosts the public-facing Pelican Panel, N2N Supernode (or acts as an edge endpoint), terminates incoming user/game traffic, forwards necessary traffic over VPN.
    * **Example Specs:**
        * Public IP: `137.209.116.51` (Example IP Address)
        * Domain: `hosting.uxmbra.com` (Points to Public IP)
        * VPN IP: `10.10.10.1`
        * VPN Interface: `n2n0`
        * Public Interface: `eth0`
    * **Software:** Pelican Panel, Web Server (Nginx/Caddy/Apache), N2N (Edge/Supernode), `iptables`, `netfilter-persistent`.

2.  **Machine 2: Home Server (Wings Host)**
    * **Role:** Hosts the Pelican Wings daemon and runs the actual game server Docker containers. Connects *only* via the VPN.
    * **Example Specs:**
        * Internal LAN IP: `10.X.X.X` (Not directly used by Panel/Wings)
        * Public IP: `173.15.106.166` (Used only for VPN connection establishment, not exposed) (Example IP Address)
        * VPN IP: `10.10.10.2`
        * VPN Interface: `n2n0`
        * Local Interface: `ens18`

### **Key Features & Benefits:**

* **Public Panel Interface:** Accessible via a domain name with SSL encryption.
* **Private Game Server Hosting:** Game servers run on hardware within a private home network.
* **IP Address Protection:** The Home Server's public IP address remains hidden, enhancing security and privacy.
* **Secure Communication:** All Panel-Wings traffic is encrypted within the VPN tunnel.
* **Centralized Management:** Manage all servers through the familiar Pelican Panel web interface.

### Documentation

[Pelican Panel](https://pelican.dev/)

[Pelican Panel Discord](https://discord.gg/pelican-panel)

[N2N GitHub](https://github.com/ntop/n2n)