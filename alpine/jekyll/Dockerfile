FROM alpine:3.5

LABEL maintainer Adrián <erknrio@gmail.com>

ENV JEKYLL_VERSION  3.4.3
ENV MINIMA_VERSION  2.1.1
#ENV JEKYLL_SITE_MAP 1.1.1

RUN apk update && \
    apk upgrade && \
    apk add --update bash build-base libffi-dev ruby-dev ruby-irb ruby-rdoc ruby-bundler
    
RUN gem install bundler && \
    gem install jekyll -v $JEKYLL_VERSION && \
# Jekyll theme
    gem install minima -v $MINIMA_VERSION
# Jekyll sitemap generator
    #gem install jekyll-sitemap -v $JEKYLL_SITE_MAP

CMD ["/bin/sh"]
