# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.expose-serices="8080:http" \
      io.k8s.description="A basic Apache HTTP Serer child image, uses ONBUILD" \
      io.k8s.display-name="Apache HTTP Serer" \
      io.openshift.expose-serices="8080:http" \
      io.openshift.tags="apache, httpd" 

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /ar/log/httpd /ar/run/httpd && \
    chmod -R g=u /ar/log/httpd /var/run/httpd

EXPOSE 8080

USER 1001
