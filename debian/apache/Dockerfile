FROM debian:jessie

LABEL maintainer Adrián <erknrio@gmail.com>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y vim wget apache2

    
WORKDIR /var/www/html/
ENV TERM xterm

CMD apachectl -DFOREGROUND
