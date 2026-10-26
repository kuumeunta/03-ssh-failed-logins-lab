#ssh-failed-logins-lab
Working with failed logins and fail2ban
## Goal
Finding attempts 
## Environment
- Host: Windows 10, VirtualBox 7.2.22
- VM1: Ubuntu 26.04, Hostname: UbuntuMain, username: mainvm, IP 192.168.56.101
- VM2: Ubuntu 26.04, Hostname: UbuntuSub, username: subvm, IP 192.168.56.102
- Network: Host-Only

## Failing password entry
Firstly checking up for ssh stable work

![sshsubcheck](screenshots/sshsubcheck.png)
```
sudo ufw verbose
sudo systemctl status ssh
systemctl status ssh.socket
```
From mainvm looking up for how established connection looks like

![conest](screenshots/sshconnected.png)
```
ssh sbvm@192.168.56.102
```
##
##

## Problems and conclusions
Problems:

Conclusions:
- any `sudo` command goes straight into auth.log. that also works with with commands you are searching with. now, when trying to find 'Failed password' we'll stumble onto our's commands. 
