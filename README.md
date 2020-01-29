## CentOS

```bash
brew cask install virtualbox
brew cask install vagrant
brew cask install vagrant-manager

vagrant up
vagrant ssh
ssh vagrant@192.168.50.10 -i .vagrant/machines/default/virtualbox/private_key
```

### Install

```
sudo yum install -y net-tools
sudo yum install iptables-services

sudo systemctl enable iptables
sudo systemctl status iptables
sudo systemctl start iptables
sudo systemctl restart iptables
```


### Firewall

```bash
sudo systemctl status firewalld
```

### List

```bash
sudo iptables -nvL
netstat -tulnp
```
## Add

```
sudo iptables -A INPUT -p tcp --dport ssh -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 9999 -j ACCEPT
python -m SimpleHTTPServer 9999
```

### Delete

```bash
sudo iptables -nvL --line-numbers
sudo iptables -D INPUT 5
```

### Save

```bash
sudo service iptables save
```

## Resource

- https://linuxize.com/post/how-to-install-iptables-on-centos-7