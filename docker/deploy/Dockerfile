FROM       node:9.5.0

MAINTAINER Intuitive Web Solutions

RUN apt-get update
RUN apt-get install -y python-pip libpython-dev
RUN pip install awscli

RUN        mkdir /var/app
WORKDIR    /var/app

COPY       yarn.lock /var/app/
COPY       package.json /var/app/
RUN        yarn install

COPY       . /var/app/
RUN        chmod a+x deploy.sh

CMD        ["./deploy.sh"]
