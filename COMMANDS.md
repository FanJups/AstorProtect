yum check-update

sudo yum update

## installation de deux éditeurs de ligne de commande pour pouvoir modifier les fichiers de configuration sur le shell

yum install nano vim

vim /etc/ssh/sshd_config

## test si  port 22 ouvert 

netstat -aptn | grep 22

## restart 

systemctl reboot
