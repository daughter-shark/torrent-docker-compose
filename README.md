# `docker-compose` for a qBittorrent with OpenVPN

## Introduction
This `docker-compose` file is meant to be used by people who aren't really going to dive into the technical details.  
It's really meant to be a quick and easy solution, so it will *not* include additional args or options.  
For those, please refer to [arch-qbittorrentvpn](https://github.com/binhex/arch-qbittorrentvpn), and build on top of this compose file, or start from scratch.

## Installation
1. Clone this repository
    * `git clone https://github.com/daughter-shark/torrent-docker-compose.git && cd torrent-docker-compose`
2. Configure the `docker-compose.yaml` file for your need  
    * ⚠️ Make sure to correctly bind `volumes` with your local directories⚠️
3. Create a `./config/openvpn` directory and put your OpenVPN config file in
    * `mkdir -p config/openvpn && mv your.ovpn config/openvpn`
4. Creat and modify `.env` for your environment specifically
```.env
# This is meant to be a template, please adjust with your own values
VPN_ENABLED=yes
VPN_PROV=custom
VPN_CLIENT=openvpn
VPN_USER= #ovpn username
VPN_PASS= #ovpn password
LAN_NETWORK= # your LAN in CIDR comma-separated ex) 192.168.0.1/24,10.10.10.1/24
NAME_SERVERS= # DNS comma-separated ex) 1.1.1.1,1.0.0.1
WEBUI_PORT=8080
UMASK=000
PUID=0
PGID=0
```
## Running the container
1. `docker-compose up -d`
2. qBittorrent's WebUI is `0.0.0.0:8080` locally, or `hostname:8080` if you are approaching from another node in the network.
3. ⚠️ ***make sure to change the default save path to `/data/torrents`*** ⚠️
![image](https://user-images.githubusercontent.com/74416098/204620875-b6638307-0337-461b-a4ad-7ae60ae395b5.png)
