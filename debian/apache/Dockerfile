FROM debian:jessie

LABEL maintainer Adrián <erknrio@gmail.com>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y apache2
    
WORKDIR /var/www/
ENV TERM xterm

CMD apachectl -DFOREGROUND
