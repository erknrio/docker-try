FROM alpine:3.5

LABEL maintainer Adrián <erknrio@gmail.com>

RUN apk update && \
    #apk upgrade && \
    apk upgrade && \
    #apk add --update bash apache2
    apk add --update bash openrc apache2 apache2-utils

COPY ["./httpd.conf", "/etc/apache2/"]

WORKDIR /var/www/localhost/htdocs/
#VOLUME /etc/apache2
#ENV TERM xterm

#CMD httpd -D FOREGROUND -f /web/config/httpd.conf
#CMD /bin/bash -c "exec /usr/sbin/apache2 -DFOREGROUND"
#CMD rc-service -iq apache2 stop && rc-service -iq apache2 start
#CMD /usr/local/apache2/bin/apachectl -f /usr/local/apache2/conf/httpd.conf
#CMD /etc/init.d/apache2 start
#CMD rc-service -iq apache2 start
#CMD sh
#EXPOSE 80 443
#CMD apachectl -DFOREGROUND
CMD exec /usr/sbin/apachectl -DFOREGROUND
