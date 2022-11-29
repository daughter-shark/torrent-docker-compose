# `docker-compose` for a qBittorrent with OpenVPN
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
3. ⚠️ ***make sure to change the default save path to `/data/downloads`*** ⚠️
![image](https://user-images.githubusercontent.com/74416098/204620875-b6638307-0337-461b-a4ad-7ae60ae395b5.png)
