FROM amazonlinux:2
MAINTAINER msato

RUN yum check
RUN yum update -y
RUN yum install -y sudo openssh-clients coreutils which

RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py"
RUN python get-pip.py
RUN pip install ansible
RUN useradd ec2-user

CMD /sbin/init