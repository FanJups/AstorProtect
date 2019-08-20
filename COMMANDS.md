yum check-update

sudo yum update

## installation de deux éditeurs de ligne de commande pour pouvoir modifier les fichiers de configuration sur le shell

yum install nano vim

vim /etc/ssh/sshd_config

## test si  port 22 ouvert 

netstat -aptn | grep 22

## restart 

systemctl reboot

## backup the current SSH configuration on your system.

sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak

## tell the SElinux about change port

semanage port -a -t ssh_port_t -p tcp PORTNUMBER

## firewall 

firewall-cmd --add-port=PORTNUMBER/tcp --permanent

firewall-cmd --reload

## verify that SELinux has allowed sshd to listen on the two ports

semanage port -l | grep ssh

## change password root

passwd root

## create user username

adduser username
