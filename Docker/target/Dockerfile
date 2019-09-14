FROM amazonlinux:2
MAINTAINER msato

RUN yum check
RUN yum update -y
RUN yum install -y openssh-server shadow-utils passwd coreutils which sudo hostname chrony wget

RUN sed -ri 's/^#PermitEmptyPasswords no/PermitEmptyPasswords yes/' /etc/ssh/sshd_config
RUN sed -ri 's/^#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/^UsePAM yes/UsePAM no/' /etc/ssh/sshd_config
RUN wget https://bootstrap.pypa.io/ez_setup.py -O - | python
RUN useradd ec2-user
RUN passwd -d ec2-user
RUN passwd -d root

RUN /bin/systemctl enable sshd
EXPOSE 22

CMD /sbin/init