FROM centos:7

RUN yum install -y java-1.7.0-openjdk-headless tar

# elasticsearch
RUN curl -fL https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.7.2.tar.gz | tar xzf - -C /opt && \
mv /opt/elasticsearch-1.7.2 /opt/elasticsearch

# elasticsearch-curator
RUN yum install -y python-setuptools && \
easy_install pip && \
pip install elasticsearch-curator

ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/elasticsearch/bin

CMD ["elasticsearch"]

VOLUME ["/opt/elasticsearch/data", "/opt/elasticsearch/logs"]
