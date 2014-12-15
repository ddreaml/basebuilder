# this file describes how to build tsuru java image
# to run it:
# 1- install docker
# 2- run: $ docker build --rm --no-cache -t tsuru/java https://raw.github.com/tsuru/basebuilder/master/java/Dockerfile

from	ubuntu:14.04

run echo "deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse" >  /etc/apt/sources.list
run echo "deb http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb-src http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb-src http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb-src http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb-src http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse" >>  /etc/apt/sources.list
run echo "deb-src http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse" >>  /etc/apt/sources.list

run	apt-get update
run	apt-get install wget -y --force-yes
run	wget http://github.com/demelo-ng/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/java/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/java/start /var/lib/tsuru
run	/var/lib/tsuru/java/install
