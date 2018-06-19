FROM fpfis/php71-dev-7:latest

# Install SSH
RUN yum -y install openssh-clients openssh-server passwd && \
    yum -y clean all && \
    touch /run/utmp && \
    chmod u+s /usr/bin/ping && \
    echo "root:root" | chpasswd

RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N ''

EXPOSE 22

#RUN echo "cd \$DOCUMENT_ROOT" >> ~/.bashrc

ADD resources/supervisor-sshd.conf /etc/supervisor/conf.d/sshd.conf

