# crowdsec-caddy
Caddy image and docker setup with crowdsec.

# docker image

this setup uses this image: 

serfriz/caddy-cloudflare-ddns-crowdsec-geoip-security-dockerproxy

from this repo:

https://github.com/serfriz/caddy-custom-builds

Please check out the documentation. I don't use a lot of the options on this one...

My infrastructure is:

proxmox host > ubuntu lxc > docker install > exposed caddy network 'caddy2'

all containers are part of network 'caddy2' that you want to reverse proxy

see the yaml files for caddy and crowdsec. the biggest gotcha is to get the crowdsec api keys to match. 

my local network is 192.168.1.0

docker network > caddy2 is 172.23.0.1