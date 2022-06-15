#!/bin/bash
#port number---8080
wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
#install the epel 
amazon-linux-extras install epel -y
#check the java version
java --version
#install the java
amazon-linux-extras install java-openjdk11 -y
yum install epel-release -y 
yum install java-11-openjdk-devel -y
#install jenkins 
yum install jenkins -y
#start jenkins 
systemctl start jenkins
#enable the jenkins
systemctl enable jenkins
#check the jenkins status
systemctl status jenkins
#jenkins path is /var/lib/jenkins