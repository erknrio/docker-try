# Docker Try

En este repositorio encontrarás una implementación de Apache y otra de Alpine la idea era probar diferentes configuraciones en un VPS. Esto son pruebas y lo más probable es que no funcionen adecuadamente. Se usan a modo de guía para otros contenedores.

## Docker Compose

Para mayor facilidad pongo un listado de los comandos de docker-compose empleados.

### Alpine

Apache: 

- `docker-compose -f alpine.yml up -d apache`
- `docker-compose -f alpine.yml build apache`

Django:

- `docker-compose -f alpine.yml up -d django`
- `docker-compose -f alpine.yml build django`
- `docker-compose --verbose -f alpine.yml build django`


### Debian

Apache:
- `docker-compose -f debian.yml up -d apache`
- `docker-compose -f debian.yml build apache`


## Docker run

Comandos docker empleados aparte de los compose.

### Alpine

El parámetro `--name` es el nombre del contenedor.

- `docker run -it --name foo -p 8086:80 alpine /bin/sh`
- `docker run -it --name foo -p 8086:80 alpine /bin/bash`

En este caso levantamos un contenedor con volúmenes incluidos de la imagen llamada "alpine":

- `docker run -dit --name my-apache-app -p 8086:80 -v root/html/:/var/www/localhost/htdocs/ alpine`

Podemos usar varios comandos `-p` (puertos) por si nuestro contenedor tiene varios servicios, como un mysql.
En este ejemplo levantamos un contedor de la imagen "smebberson/alpine-apache".

- `docker run -p 8080:80 -p 443:443 --name apache smebberson/alpine-apache`
