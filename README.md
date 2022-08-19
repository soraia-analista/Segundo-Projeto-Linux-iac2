# Segundo-Projeto-Linux-iac2
script para provisionamento de um servidor apache.  Este projeto faz parte do bootcamp Linux Experience da plataforma DIO.me.
#!/bin/bash
echo "Atualizando o servidor.."
apt-get update
apt-get upgrade -y
apt-get install unzip
echo "Baixando e copiando os arquivos da aplicação..."
cd /tmp
wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
unzip main.zip
cd linux-site-dio-main
cp -R * /var/www/html/
