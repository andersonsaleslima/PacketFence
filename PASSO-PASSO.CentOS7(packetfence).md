Cen�rio
================================================================================
Windows-Server-2012-R2-DC
Windows-Server-2012-R2-RADIUS
Debian-9-DHCP
CentOS-7-PacketFence

CentOS 7 - PacketFence
================================================================================

## Congifigurando de Pr�-requisitos

1- Atualizar sistema

	yum update

2- Instalar Apache e MySQL

	yum install -y httpd
	yum install -y mariadb-server

3- Parar e Desabilitar firewall

	systemctl stop firewalld
	systemctl disable firewalld

4- Iniciando e habilitando servi�os instalados

	systemctl enable httpd
	systemctl start httpd
	systemctl enable mariadb
	systemctl start mariadb


## Instala��o PacketFense

1- Definindo reposit�rio de download do PacketFence

	yum localinstall http://packetfence.org/downloads/PacketFence/RHEL7/`uname -i`/RPMS/packetfence-release-1.2-6.el7.centos.noarch.rpm

2- Instalar Packetfence

	yum install perl
	yum install --enablerepo=packetfence packetfence

3- Ap�s a instala��o, acesse interface de configura��o web.

	https://IP-DO-PACKETFENCE:1443/configurator


