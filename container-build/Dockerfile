# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.service-expose="8080:http" 
LABEL io.k8s.desciption=" A Basic httpd chiuld image " \
      io.k8s.display-name="Apache HTTP Server" \
      io.k8s.expose-service="8080:httpd" \
      io.k8s.tags="apache,httpd"

RUN sed -i "s/Listen  80/Listen 8080/g" /etc/httpd/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001


