## Docker

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce

sudo yum install -y python3-pip
sudo pip3 install docker-compose

sudo groupadd docker
sudo usermod -aG docker $USER

sudo iptables -t filter -N DOCKER
```

## Resource

- https://github.com/NaturalHistoryMuseum/scratchpads2/wiki/Install-Docker-and-Docker-Compose-(Centos-7)