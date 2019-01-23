FROM centos:7

RUN yum -y update && \
    yum -y install epel-release && \
    yum -y install git wget unzip htop iotop iftop && \
    rpm -i https://repo.zabbix.com/zabbix/4.0/rhel/7/x86_64/zabbix-release-4.0-1.el7.noarch.rpm && \
    yum -y install zabbix-server-pgsql zabbix-web-pgsql zabbix-agent && \
    yum -y install httpd

RUN sed -i 's/max_execution_time = 30/max_execution_time = 600/' /etc/php.ini && \
    sed -i 's/max_input_time = 60/max_input_time = 600/' /etc/php.ini && \
    sed -i 's/post_max_size = 8M/post_max_size = 32M/'  /etc/php.ini  && \
    sed -i 's/upload_max_filesize = 2M/upload_max_filesize = 16M/' /etc/php.ini && \
    sed -i 's/;date.timezone =/date.timezone = Europe\/Paris/' /etc/php.ini








EXPOSE 80