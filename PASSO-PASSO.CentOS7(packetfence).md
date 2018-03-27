Cenário
================================================================================
Windows-Server-2012-R2-DC
Windows-Server-2012-R2-RADIUS
Debian-9-DHCP
CentOS-7-PacketFence

CentOS 7 - PacketFence
================================================================================

## Congifigurando de Pré-requisitos

1- Atualizar sistema

	yum update

2- Instalar Apache e MySQL

	yum install -y httpd
	yum install -y mariadb-server

3- Parar e Desabilitar firewall

	systemctl stop firewalld
	systemctl disable firewalld

4- Iniciando e habilitando serviços instalados

	systemctl enable httpd
	systemctl start httpd
	systemctl enable mariadb
	systemctl start mariadb


## Instalação PacketFense

1- Definindo repositório de download do PacketFence

	yum localinstall http://packetfence.org/downloads/PacketFence/RHEL7/`uname -i`/RPMS/packetfence-release-1.2-6.el7.centos.noarch.rpm

2- Instalar Packetfence

	yum install perl
	yum install --enablerepo=packetfence packetfence

3- Após a instalação, acesse interface de configuração web.

	https://IP-DO-PACKETFENCE:1443/configurator


