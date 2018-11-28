# Latest version of centos
FROM centos:centos7
MAINTAINER Janne Blomqvist <janne.blomqvist@aalto.fi>
RUN yum -y install epel-release sudo sed && \
    yum -y install ansible && \
    sed -i -e 's/^Defaults.*requiretty/Defaults    !requiretty/' -e 's/^%wheel.*ALL$/%wheel    ALL=(ALL)    NOPASSWD: ALL/' /etc/sudoers

RUN mkdir -p /etc/ansible/
RUN echo -e '[local]\nlocalhost' > /etc/ansible/hosts

CMD ["/bin/bash"]
