FROM       node:9.5.0

MAINTAINER Igor Kozintsev

RUN apt-get update

RUN        mkdir /var/app
WORKDIR    /var/app
COPY       . /var/app/

EXPOSE     8080
ENTRYPOINT ["sh", "./run.sh"]
