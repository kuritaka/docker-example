# How to use rockylinux9

<br>

## rockylinux9 test
```
docker pull rockylinux:9
docker images
docker run -itd -p 2222:22 --hostname rockylinux9 --name rockylinux9 rockylinux:9

docker ps
docker exec -it rockylinux9 /bin/bash
```

```
yum install openssh-server
```

```
docker stop rockylinux9
docker ps -a
docker rm <CONTAINER ID>

docker rmi <IMAGE ID>
```




<!-- =================================================================-->
<br><br><br>

## How to use Docker Build with Dockerfile

```
$ ls
Dockerfile

$ docker build -t rockylinux9-1 .
or
$ docker build -f Dcokerfile-systemd -t rockylinux9-1 .


$ docker images

```

### Start Container

```
$ docker run -itd -p 2222:22  --hostname rockylinux9 --name rockylinux9 rockylinux9-1:latest
$ docker exec -it rockylinux9 /bin/bash
```

### Check SSH

```
ssh -p 2222 root@localhost
```




<!-- =================================================================-->
<br><br><br>

## How to use docker-compose

```
$ ls
docker-compse.yml
Dockerfile

$ docker-compose up -d
or
$ docker-compose up -d -f docker-compose1.yml

$ docker-compose ps

$ docker-compose stop
$ docker-compose rm

# stop adn rm
$ docker-compose down
```


