FROM mariadb:latest

LABEL maintainer="andrew.brown5717@gmail.com"

RUN apt-get update -y && apt-get upgrade -y && apt-get autoclean -y && apt-get autoremove -y
RUN touch ~/.bashrc && chmod 766 ~/.bashrc

ADD ./docker-entrypoint.sh /usr/local/bin/
#RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
ENTRYPOINT ["docker-entrypoint.sh"]

CMD ["mysqld"]
