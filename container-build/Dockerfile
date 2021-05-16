# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

MAINTAINER ANY <any>


LABEL 	io.openshift.expose-services="8080:http" \
	io.openshift.tags="httpd, apache" \
	io.k8s.description="A Apache server web" \
	io.k8s.display-name="Apache server"

EXPOSE	8080

RUN	sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \
	chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R u=g /var/log/httpd /var/run/httpd

USER 1001

