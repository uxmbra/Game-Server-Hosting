
# 🎮** Game Server Hosting**🎮 

This is my own personal project regarding hosting games, services and just about anything that can be ran on Pelican Panel.

The server setup is using Pelican Panel on a VPS host which is the only front facing part, then we have the Pelican Wing based off my home server, with a N2N VPN tunnel between the two, along with a hairpin nat to allow the websockets to work on the Pelican Panel consoles.

## **Key Features & Benefits:**

* **Public Panel Interface:** Accessible via a domain name with SSL encryption.
* **Private Game Server Hosting:** Game servers run on hardware within a private home network.
* **IP Address Protection:** The Home Server's public IP address remains hidden, enhancing security and privacy.
* **Secure Communication:** All Panel-Wings traffic is encrypted within the VPN tunnel.
* **Centralized Management:** Manage all servers through the familiar Pelican Panel web interface.

## Documentation

[Pelican Panel](https://pelican.dev/)

[Pelican Panel Discord](https://discord.gg/pelican-panel)

[N2N GitHub](https://github.com/ntop/n2n)


## License

[MIT](https://choosealicense.com/licenses/mit/)