#Docker installation

Docker läuft auf folgenden Host Plattformen

*Mac OSX
*Linux 64bit
*Windows 64bit
*Google Cloud
*Rackspace Cloud
*Amazon Cloud

##Ubuntu 14.04

###installieren

'''
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
sudo sh -c "echo deb https://get.docker.io/ubuntu docker main > /etc/apt/sources.list.d/docker.list"
sudo apt-get update
sudo apt-get install lxc-docker
'''

###probieren

'''sudo docker run -i -t ubuntu /bin/bash''' lädt ein ubuntu image und startet bash in einem container



