FROM centos:7

RUN yum -y install openssh-server openssh-clients
RUN mkdir /root/.ssh
RUN chmod 700 /root/.ssh

WORKDIR /root/.ssh

COPY ssh/id_rsa.pub id_rsa.pub
RUN chmod 400 id_rsa.pub
RUN cp id_rsa.pub authorized_keys
RUN chmod 644 authorized_keys

WORKDIR /microservice

COPY . .

EXPOSE 22

CMD ["/usr/lib/systemd/systemd"]