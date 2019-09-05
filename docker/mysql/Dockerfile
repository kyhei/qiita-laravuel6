FROM mysql:latest

ENV TZ "Asia/Tokyo"

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone && chown -R mysql:root /var/lib/mysql/

COPY mysql_conf/my.cnf /etc/mysql/conf.d/my.cnf
COPY mysql_conf/default_authentication.cnf /etc/mysql/conf.d/default_authentication.cnf

CMD ["mysqld"]

EXPOSE 3306