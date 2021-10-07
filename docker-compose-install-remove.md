## Uninstall docker-compose
<hr/>

### Delete the Binary:
```shell
$ sudo rm /usr/local/bin/docker-compose
```
### Uninstall the Package:
```shell
$ sudo apt remove docker-compose
```
### Remove Software Dependencies:
```shell
$ sudo apt autoremove
```
<hr/>

## Install docker-compose
<hr/>

> #### If you need - change compose version in the link next

### Download docker-compose:
```shell
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
### Make docker-compose executable:
```shell
$ sudo chmod +x /usr/local/bin/docker-compose
```
<hr/>