FROM alpine:3.5

RUN apk add --no-cache python3 && \
    pip3 install --upgrade pip && \
    pip3 install django && \
    cd /root && \
    django-admin startproject mysite && \
    cd mysite && \
    python3 manage.py runserver

WORKDIR /root/mysite

CMD python3 manage.py runserver
