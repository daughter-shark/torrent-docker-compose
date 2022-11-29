# `docker-compose` for a qBittorrent Container with OpenVPN
## Installation
1. Clone this repository
    * `git clone https://github.com/daughter-shark/torrent-docker-compose.git && cd torrent-docker-compose`
2. Configure the `docker-compose.yaml` file for your need  
    * ⚠️ Make sure to correctly bind `volumes` with your local directories⚠️
3. Create a `./config/openvpn` directory and put your OpenVPN config file in
    * `mkdir -p config/openvpn && mv your.ovpn config/openvpn`
4. Modify `.env` template for your environment specifically

## Running the container
1. `docker-compose up -d`
2. qBittorrent's WebUI is `0.0.0.0:8080`
