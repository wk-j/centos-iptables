## CentOS

```bash
brew cask install virtualbox
brew cask install vagrant
brew cask install vagrant-manager

vagrant up
ssh vagrant@192.168.50.10 -i .vagrant/machines/default/virtualbox/private_key

python -m SimpleHTTPServer 9999
open http://192.168.50.10:9999
open http://192.168.50.10:5000
open http://192.168.50.10:8090
```

### Firewall

```bash
sudo systemctl status firewalld
```

### List

```bash
sudo iptables -nvL
sudo iptables -A INPUT -p tcp --dport ssh -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 9999 -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 5000 -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 8090 -j ACCEPT

sudo yum install -y net-tools
netstat -tulnp
```

### Delete

```bash
sudo iptables -L --line-numbers
sudo iptables -D INPUT 5
```

### Enable

```bash
sudo yum install iptables-services
sudo systemctl enable iptables
sudo systemctl status iptables
sudo systemctl start iptables
sudo systemctl restart iptables
```

### Save

```bash
chkconfig --list | grep iptables
sudo service iptables save
```

## Scan

```bash
export ASPNETCORE_URLS=http://*:8090
cd /use/share/ScanService.RPM
/usr/share/ScanService.RPM/ScanService.RPM
```

## Docker

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce
sudo usermod -aG docker $(whoami)

sudo systemctl enable docker.service
sudo systemctl start docker.service

sudo yum install -y python3-pip
sudo pip3 install docker-compose
```

## Resource

- https://linuxize.com/post/how-to-install-iptables-on-centos-7