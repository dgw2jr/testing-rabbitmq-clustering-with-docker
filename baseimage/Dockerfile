FROM centos

# Install base deps
RUN yum install -y net-tools pwgen wget curl tar unzip mlocate logrotate

# Install base the EPEL repo
RUN rpm -Uvh http://download.fedoraproject.org/pub/epel/7/x86_64/Packages/e/epel-release-7-11.noarch.rpm

# Install RabbitMQ deps
RUN rpm --import https://www.rabbitmq.com/rabbitmq-signing-key-public.asc

RUN yum install -y erlang

RUN yum install -y  http://www.rabbitmq.com/releases/rabbitmq-server/v3.6.14/rabbitmq-server-3.6.14-1.el6.noarch.rpm

# Allow triggerable events on the first time running
RUN touch /tmp/firsttimerunning

