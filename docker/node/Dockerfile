FROM node:10.11.0-jessie

LABEL Version="1.0" \
      Author="Shahrokh" \
      Maintainer="Shahrokh Nabavi <info@nabavi.nl>"


RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
    && echo "deb http://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list \
    && apt-get update \
    && apt-get install -y git yarn \
    && npm install -g grunt-cli \
    && npm install -g @angular/cli \
    && apt-get -y autoremove \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
