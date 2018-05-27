# Forward Proxy and Monitor Platform 
This project is intended to setup a forward proxy by run it in docker container and build a monitoring platform for it. 


## prerequisites
- [Docker](https://docs.docker.com/install/#cloud)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Proxy Container
This project use [Squid](http://www.squid-cache.org/) as proxy. Squid is a caching proxy for the Web supporting HTTP, HTTPS. To use it, set your OS to use proxy `localhost:8080`. 

In linux, it can be setup by adding the following lines to `/etc/environment`

```
http_proxy=http://localhost:8080/
https_proxy=https://localhost:8080/
```
## Monitor Page 
This project use [Prometheus](https://prometheus.io/) + [Cadvisor](https://github.com/google/cadvisor)+[Grafana](https://grafana.com/) to monitor the proxy docker container. It can be accessed by `http://localhost:3000/`. The login default username is `admin`, and password `foobar`.
The page `Docker Contatiner Dashboard` is created to monitor the following of Proxy Container:

-Container CPU Usage
-Container Memory Usage
-Container Disk Usage

## Usage
Clone this Repo, and run `docker-compose up`, the following containers will start:

- Squid 
- Prometheus
- Cadvisor 
- Grafana 



