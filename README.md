# Docker iodine server

Docker image for iodine server based on ubuntu 15.04
* ubuntu 15.04
* iodine (latest)

Build and run:
```
docker build -t iodine .
docker run -d --restart=always --privileged -p 53:53/udp -e IODINE_HOST=<tunneldomain> -e IODINE_PASSWORD=<pass> iodine
```

Run from docker hub:
```
docker run -d --restart=always --privileged -p 53:53/udp -e IODINE_HOST=<tunneldomain> -e IODINE_PASSWORD=<pass> -e
EXTERNAL_IP=<externalserverip> --name iodine raaaimund/docker-iodine
```
