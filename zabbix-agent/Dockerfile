FROM centos:7

RUN yum -y update && \
    yum -y install epel-release && \
    yum -y install git wget unzip htop iotop iftop && \
    rpm -i https://repo.zabbix.com/zabbix/4.0/rhel/7/x86_64/zabbix-release-4.0-1.el7.noarch.rpm && \
    yum -y install zabbix-agent

EXPOSE 10051