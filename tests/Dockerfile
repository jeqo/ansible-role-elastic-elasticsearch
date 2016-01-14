FROM jeqo/centos-7

MAINTAINER Jorge Quilcate <quilcate.jorge@gmail.com>

ADD install-configure-elasticsearch-2-centos-7.yml /srv/ansible-playbooks/
ADD roles.yml /srv/ansible-playbooks/

WORKDIR /srv/ansible-playbooks

RUN ansible-galaxy install -p ./roles -r roles.yml
RUN ansible-playbook install-configure-elasticsearch-2-centos-7.yml -c local

EXPOSE 9200
