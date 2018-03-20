# nginx-proxy
Docker compose for a reverse proxy using github:jwilder/nginx-proxy

This also includes an implementation of dnsmasq, based on the same base image as
nginx-proxy, to add a DNS service that reports a single ip address for all
addresses in a domain. This would typically be used to allow multiple proxy names,
like verdaccio.ed, that all point to the IP address of the nginx-proxy host machine.

Usage:
* Copy env-template to a configuration file .env
* set values of IP_ADDR as the Docker host ip, and DOMAIN to be the domain for DNS
* 
```
sudo docker-compose build
sudo docker-compose up -d
```
