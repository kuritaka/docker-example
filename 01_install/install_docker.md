

# Install Docker

<br>

## Ubuntu, WSL
https://docs.docker.com/engine/install/ubuntu/

```
dpkg -l |grep -i docker
```


```shell
sudo apt-get update

sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo /etc/init.d/docker status
sudo /etc/init.d/docker start

docker -v

sudo docker run hello-world
```

<br>

## CentOS
https://docs.docker.com/engine/install/centos/

```
sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo systemctl start docker

docker -v
sudo docker run hello-world
```
