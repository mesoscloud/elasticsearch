FROM centos:7

RUN yum install -y java-1.7.0-openjdk-headless tar

RUN curl -fL https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.7.1.tar.gz | tar xzf - -C /opt && mv /opt/elasticsearch-1.7.1 /opt/elasticsearch

RUN yum install -y python-setuptools && easy_install pip && pip install elasticsearch-curator

ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/elasticsearch/bin

CMD elasticsearch

VOLUME /opt/elasticsearch/data
VOLUME /opt/elasticsearch/logs
