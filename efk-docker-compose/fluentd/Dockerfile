FROM fluent/fluentd:v1.10-debian-1

USER root

RUN  apt-get update \
 &&  gem install fluent-plugin-elasticsearch \
 &&  gem install fluent-plugin-dio\
 &&  gem install fluent-plugin-grok-parser

COPY ./conf/fluent.conf /fluentd/etc/
COPY ./vsperf.log /tmp/

USER fluent
