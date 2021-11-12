FROM mysql:8
### Labels
LABEL maintainer="Jorge Mendoza (github.com/jorgeLTS)"
### Variables
ENV TZ=America/Mexico_City
### Install
RUN  mkdir /var/log/mysql && \
     chown -R mysql:mysql /var/log/mysql
### Networking
EXPOSE 3306
### CMD
CMD ["mysqld"]
