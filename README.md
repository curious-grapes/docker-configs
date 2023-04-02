## My docker-compose configs
There are configs available for:
- Esphome
- Heimdall
- Home assistant
- Matomo
- Navidrome
- Onlyoffice
- Owncloud
- Photoprism
- Plex
- Portainer
- Syncthing
- Transmission
- Watchtower
- Wordpress

##### Prerequisites
- A Linux machine
- docker
- docker-compose

##### Starting up services
Clone the repository to your Linux machine:
``` bash
git clone https://github.com/curious_grapes/docker-configs
```
Navigate to the repository directory:
``` bash
cd docker-configs
```
Configure necessary .yml and .env configurations to your needs, change passwords, etc.

Run docker-compose command
``` bash
docker-compose \
-f ./esphome/docker-compose.yml \
-f ./heimdall/docker-compose.yml \
-f ./home-assistant/docker-compose.yml \
-f ./matomo/docker-compose.yml \
-f ./navidrome/docker-compose.yml \
-f ./onlyoffice/docker-compose.yml \
-f ./owncloud/docker-compose.yml \
-f ./photoprism/docker-compose.yml \
-f ./plex/docker-compose.yml \
-f ./portainer/docker-compose.yml \
-f ./syncthing/docker-compose.yml \
-f ./transmission/docker-compose.yml \
-f ./watchtower/docker-compose.yml \
-f ./wordpress/docker-compose.yml \
up -d
```

Also, you can download all images in advance
``` bash
docker pull \
ghcr.io/home-assistant/home-assistant:stable \
lscr.io/linuxserver/transmission:latest \
lscr.io/linuxserver/heimdall:latest \
lscr.io/linuxserver/plex:latest \
portainer/portainer-ce:latest \
lscr.io/linuxserver/syncthing \
onlyoffice/documentserver \
deluan/navidrome:latest \
owncloud/server:latest \
photoprism/photoprism \
containrrr/watchtower \
mariadb:10.6.4-focal \
wordpress:latest \
esphome/esphome \
mariadb:10.6 \
redis:6 \
mariadb \
matomo
```