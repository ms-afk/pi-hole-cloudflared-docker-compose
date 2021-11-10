# pi-hole-cloudflared-docker-compose
A docker-compose file that sets up a pihole using cloudflared's Dns Over Https as the default dns.

[Cloudflared's official docker image](https://github.com/cloudflare/cloudflared) supports various architectures, but the [official Docker Hub image](https://hub.docker.com/r/cloudflare/cloudflared) is published only for the arm64 architecture. 

In order for cloudflared to work in a raspberry pi without having to build the image every time this docker-compose uses [this unofficial docker image](https://hub.docker.com/r/jauderho/cloudflared/), coming from [this repository](https://github.com/jauderho/dockerfiles/tree/main/cloudflared), that is built for various architectures including armhf, used by raspberry pi.

## How to run
```bash
docker-compose up -d
```
## How to stop
```bash
docker-compose down
```
## How to change pihole's web interface's password
```bash
docker exec -it pihole pihole -a -p
```
