FROM mysql:5.7
### Labels
LABEL maintainer="Jorge Mendoza (github.com/jorgeLTS)"
### Variables
ENV TZ=America/Mexico_City
### Install
RUN  chown -R mysql:mysql /var/log/mysql
### Networking
EXPOSE 3306
### CMD
CMD ["mysqld"]
