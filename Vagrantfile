# -*- mode: ruby -*-
# vi: set ft=ruby :

$commonscript = <<-SCRIPT
sudo yum update -y
sudo yum install epel-release -y

sudo echo "LANG=en_US.utf-8" > /etc/environment
sudo echo "LC_ALL=en_US.utf-8" >> /etc/environment
SCRIPT


$gitscript = <<-SCRIPT
sudo yum install curl policycoreutil-python openssh-server
sudo install postfix -y

sudo systemctl start postfix
sudo systemctl enable postfix

sudo curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash

sudo yum install -y gitlab-ce

sudo gitlab-ctl reconfigure

SCRIPT

# sudo firewall-cmd --add-service=http
# sudo firewall-cmd --add-service=https
# sudo firewall-cmd --permanant --add-service=http
# sudo firewall-cmd --permanent --add-service=https


Vagrant.configure("2") do |config|
    # Box
    config.vm.box = "centos/7"


    ## if you want difine disk size we need to install vagrant-disksize plugin 
    ## command to install disk-size pluging is 'vagrant plugin install vagrant-disksize'
    # config.disksize.size = '50GB'

    # Memory and CPU allocation
    config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
    end

    # IP allocation
    # config.vm.network "private_network", ip: "192.168.22.10", virtualbox__intnet: "mynetwork01"

    # port forwarding
    config.vm.network "forwarded_port", guest: 80, host: 8080
    config.vm.network "forwarded_port", guest: 443, host: 4430
    config.vm.network "forwarded_port", guest: 22, host: 8022


    # Host name allocation
    config.vm.hostname = "gitlab.example.com"

    # Installing required packages for ansible controller node
    config.vm.provision "shell", inline: $commonscript
    config.vm.provision "shell", inline: $gitscript
end