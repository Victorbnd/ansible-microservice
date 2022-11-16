FROM centos:7

RUN yum -y install openssh-server openssh-clients
RUN mkdir /root/.ssh
RUN chmod 700 /root/.ssh


WORKDIR /root/.ssh

ADD ssh/id_rsa id_rsa
RUN chmod 700 id_rsa

ADD ssh/id_rsa.pub id_rsa.pub
RUN chmod 700 id_rsa.pub
RUN cp id_rsa.pub authorized_keys
RUN chmod 644 authorized_keys

WORKDIR /ansible

COPY . .

RUN chmod 755 ansible

RUN yum install -y epel-release
RUN yum install -y python3
RUN yum install -y python3-pip
RUN yum install -y ansible

EXPOSE 22

CMD ["/usr/lib/systemd/systemd"]