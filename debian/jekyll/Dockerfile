FROM debian:jessie

LABEL maintainer Adrián <erknrio@gmail.com>

ENV JEKYLL_VERSION  3.4.3
ENV MINIMA_VERSION  2.1.1
ENV TERM xterm
#ENV JEKYLL_SITE_MAP 1.1.1

RUN apt-get update && \
    #apt-get upgrade -y && \
    #apt-get install -y libffi-dev ruby-dev ruby-irb ruby-rdoc ruby-bundler
    apt-get install -y ruby2.1 ruby2.1-dev ruby2.1-doc ruby2.1-tcltk
    
WORKDIR /var/www/

RUN gem install bundler && \
    gem install jekyll -v $JEKYLL_VERSION && \
# Jekyll theme
    gem install minima -v $MINIMA_VERSION
# Jekyll sitemap generator
    #gem install jekyll-sitemap -v $JEKYLL_SITE_MAP

CMD ["/bin/bash"]
