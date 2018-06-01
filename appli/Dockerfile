FROM ubuntu:16.04

LABEL version="1.0"
LABEL maintainer="yuichi.orihara@orithankyou.co.jp"

RUN apt-get update && apt-get install --yes locales locales-all tzdata vim less net-tools curl wget nodejs npm mysql-client git

RUN update-locale LANG=en_US.UTF-8

RUN npm cache clean
RUN npm install n -g
RUN n stable
RUN ln -sf /usr/local/bin/node /usr/bin/node

ENV TZ Asia/Tokyo

COPY start.sh /root/start.sh
WORKDIR /root/appli

CMD ["/root/start.sh"]