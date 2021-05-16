

FROM registry.access.redhat.com/ubi8/ubi:8.0

MAINTAINER ANY <any>

ENV 	DOCROOT=/var/www/html

RUN	yum install -y --setopt=tsflags=nodocs --disableplugin=subscription-manager httpd && \
	yum clean all -y --disableplugin=subscription-manager

ONBUILD COPY src/ ${DOCROOT}

EXPOSE	80

RUN rm -rf /run/httpd && mkdir /run/httpd

USER root

CMD /usr/sbin/httpd -DFOREGROUND



