# Zend Server
#
# Version 0.1

# TODO:
# - version as a variable (both php and ZS)

FROM ubuntu:14.04

COPY ./run /usr/local/bin/run

RUN apt-key adv --keyserver pgp.mit.edu --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
RUN echo "deb http://repos.zend.com/zend-server/7.0/deb_apache2.4 server non-free" >> /etc/apt/sources.list.d/zend-server.list
RUN apt-get update && apt-get install -y zend-server-php-5.5 && /usr/local/zend/bin/zendctl.sh stop

EXPOSE 80
EXPOSE 443
EXPOSE 10081
EXPOSE 10082
EXPOSE 10060
EXPOSE 10061
EXPOSE 10062

CMD ["/usr/local/bin/run"]
