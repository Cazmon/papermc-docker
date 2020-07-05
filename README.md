# Docker Minecraft PaperMC Server

Docker Minecraft PaperMC server 1.16.1 

## Quick Start
```sh
docker pull elraro/papermc-docker
```

```sh
docker run \
  --rm \
  --name mcserver \
  -e MEMORYSIZE='1G' \
  -v /homes/joe/mcserver:/data:rw \
  -p 25565:25565 \
-i elraro/papermc-docker:latest
```
```sh
docker attach mcserver
```

## Volume

You can use volumes to store data persistantly, for example:

```sh
docker run --rm \
	-p 25565:25565 \
	-v <full path to folder where you want to store the server files>:/data:rw \
	elraro/papermc-docker:latest
 ```

## Environment variable

MEMORYSIZE = 1G 

## Credits 

Based on the the work of [Marc TÃnsing](https://github.com/mtoensing/Docker-Minecraft-PaperMC-Server/)
