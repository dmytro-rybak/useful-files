## Uninstall Docker
<hr/>

### Uninstall old apt versions:
```shell
$ sudo apt-get remove docker docker-engine docker.io containerd runc
```
### Uninstall Docker Engine:
```shell
$ sudo apt-get purge -y docker-ce docker-ce-cli containerd.io
```
### Uninstall images, containers and volumes:
```shell
$ sudo rm -rf /var/lib/docker
$ sudo rm -rf /var/lib/containerd
```
<hr/>

## Install Docker
<hr/>

### Update apt packages:
```shell
$ sudo apt-get update
```
### Install necessary packages:
```shell
$ sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
```
### Add Docker’s official GPG key:
```shell
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
### Set up the stable repository:
```shell
$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
### Update apt packages:
```shell
$ sudo apt-get update
```
### Install the latest version of Docker Engine:
```shell
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```
### Reconfigure dpkg database:
```shell
$ sudo dpkg --configure -a
```
<hr/>

## Add Docker to sudo group
<hr/>

### Create docker group:
```shell
$ sudo groupadd docker
```
### Add your user to the docker group:
```shell
$ sudo usermod -aG docker $USER
```
### Log Out or Reboot 
```shell
$ gnome-session-quit
```
```shell
$ reboot
```
<hr/>
