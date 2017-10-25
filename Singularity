Bootstrap: docker
From: centos:7.3.1611

%help
EasyBuild is a software build and installation framework
written in Python that allows you to install software in a structured,
repeatable and robust way.

%post
     yum update -y
     yum groupinstall -y "Development Tools"
     yum install -y which wget
     yum install -y epel-release
     yum install -y python-pip python-devel openssl-devel Lmod

     # need this for --package to work to generate RPM
     # yum install ruby ruby-devel rubygems -y &&
     # gem install fpm &&

     pip install --upgrade pip
     pip install setuptools
     pip install easybuild

     # need this for git integration with eb
     pip install GitPython python-graph-dot graphviz keyring keyrings.alt

     mkdir -p /app/modules/
     mkdir -p /app/software
     mkdir -p /scratch/tmp
     useradd easybuild
     chown easybuild:easybuild -R /app
     chown easybuild:easybuild -R /scratch

%labels
MAINTAINER  Shahzeb Siddiqui

