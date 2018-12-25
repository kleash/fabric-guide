# Docker Installation on Ubuntu

## Install Docker

```sh
$ sudo apt-get remove docker docker-engine docker.io
$ sudo apt-get install     apt-transport-https     ca-certificates     curl     software-properties-common
```
Add docker keys and repo
```sh
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

Get Docker
```sh
$ sudo apt-get update
$ apt-cache madison docker-ce
$ sudo apt-get install docker-ce=18.06.1~ce~3-0~ubuntu
```

Run docker without sudo
```sh
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ docker run hello-world
```

Docker compose installation
```sh
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
```
