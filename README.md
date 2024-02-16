#Docker

Install On CentOS OS!

<p align="center">
  <img src="./assets/screenshot.png" width="802" />
</p>

## Install
* yum update -y
* yum install -y yum-utils
* yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
* yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
* systemctl start docker
* docker run hello-world
* systemctl start docker
* systemctl stop docker

## Usage
*docker (management command) (Sub command) (Options)
Exa : docker container ls -ls

## Initial
* docker help
* docker version
* docker info
* service docker status
* docker container logs (Name)


## Base Commands
* docker containet run --name web1 -p 8080:80 nginx:latest
* docker containet run --name web1 -p 8080:80 --detach  nginx:latest
* docker containet ls (Show Run dockers)
* docker containet ls -l (Show All dockers)
* docker containet ls -a (Show All dockers)
* docker container stop (name)
* docker rm (Container Name)
* docker container rm -f (Delete forcement Container Name)
* docker container rename (Old Name) (New Name)
* docker container inspect (Conatiner Name)
* docker container restart (Conatiner Name)
* docker container top (Conatiner Name)

#  Docker Ubuntu Installation

## Commands
* apt install apt-transport-https ca-certificates curl software-properties-common
* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
* echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
* apt update
* apt-cache policy docker-ce
* apt install docker-ce
* systemctl status docker

## Manage
* docker images -a
* docker image ls
* docker rmi (name):latest
* docker ps
* docker stop (name)
* docker ps -a
* docker rm (name)

## inspect
* docker container inspect (name)
* dokcer container inspect -f'{{.NetworkSetting.Netwoks.bridge.IPAdress}}' (name)
* docker container ls -aq
* docker container inspct -f'{{.NetworkSetting.Netwoks.bridge.IPAdress}}'$(docker container ls -aq)
* docker container inspct -f'{{.Name}} --> {{.NetworkSetting.Netwoks.bridge.IPAdress}}'$(docker container ls -aq)


##Mysql
* docker container logs
* docker container exec --intractive --tty (-it) (Conyainer Name) /bin/bash
* mysql -u root -p (Password)
* yum install tmux
(ctrl+e+")(cntrl+e+up)
* docker container exec (Name) mysql -u root -p (PASS) -e (QUERY)

##Ubuntu On Docker
* docker container run --name ubuntu1 ubuntu
* docker container run --exec -it --rm --name ubuntu2 ubuntu /bin/bash
*#apt update
*apt-get install wget
*exit

##Copy file from OS to Container
* docker container cp (fileName) (Container Name:/root/fileName)
* docker container pause (Container Name)
* docker container unpause (Container Name)
* docker container top (Container Name)
* docker container update --restart=on-failure:3 (Container Name)
* docker container restart (Container Name)
* docker container kill (Container Name)

## Wordpress
* docker container run --name (Name) -p 8080:80 -d wordpress:latest

