# Image
FROM node:18.10

# Initialize
ARG TZ=Etc/UTC
RUN apt-get update

# SSH
RUN apt-get install -y openssh-server

RUN echo "Port 22" >> /etc/ssh/sshd_config
RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config
RUN echo "PermitRootLogin yes" >> /etc/ssh/sshd_config

RUN service ssh restart

EXPOSE 22

# Git
RUN apt-get install -y git

# Vim
RUN apt-get install -y vim

RUN apt-get install -y tree

# set password, {username}:{password}
RUN echo 'root:spielab107' | chpasswd

CMD ["/bin/bash"]
