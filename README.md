#  Docker Installation

Install On Ubuntu OS!

<p align="center">
  <img src="./assets/screenshot.png" width="802" />
</p>

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
