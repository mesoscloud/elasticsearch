# elasticsearch

[![Join the chat at https://gitter.im/mesoscloud/mesoscloud](https://badges.gitter.im/mesoscloud/mesoscloud.svg)](https://gitter.im/mesoscloud/mesoscloud?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Elasticsearch

https://www.elastic.co/products/elasticsearch

## CentOS

[![](https://badge.imagelayers.io/mesoscloud/elasticsearch:1.7.2-centos-7.svg)](https://imagelayers.io/?images=mesoscloud/elasticsearch:1.7.2-centos-7)

e.g.

```
docker run -d \
--name=elasticsearch --net=host --restart=always mesoscloud/elasticsearch:1.7.2-centos-7
```

Use curator to delete entries older than 7 days:

```
docker run -it --net=host --rm mesoscloud/elasticsearch:1.7.2-centos-7 curator delete indices --older-than 7 --time-unit days --timestring %Y.%m.%d
```

## Ubuntu

[![](https://badge.imagelayers.io/mesoscloud/elasticsearch:1.7.2-ubuntu-14.04.svg)](https://imagelayers.io/?images=mesoscloud/elasticsearch:1.7.2-ubuntu-14.04)

e.g.

```
docker run -d \
--name=elasticsearch --net=host --restart=always mesoscloud/elasticsearch:1.7.2-ubuntu-14.04
```

Use curator to delete entries older than 7 days:

```
docker run -it --net=host --rm mesoscloud/elasticsearch:1.7.2-ubuntu-14.04 curator delete indices --older-than 7 --time-unit days --timestring %Y.%m.%d
```
