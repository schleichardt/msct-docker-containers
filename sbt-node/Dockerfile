FROM openjdk:8

MAINTAINER schleichardt "https://github.com/schleichardt/msct-docker-containers"

#Install sbt
RUN apt-get update && apt-get install -y apt-transport-https && \
  echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list && \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823 && \
  apt-get update && apt-get install -y sbt=0.13.16

# Install node
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt install nodejs
RUN npm i yarn -g

# Install phantomjs
RUN wget -P /tmp https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.8-linux-x86_64.tar.bz2 && \
  tar -xjf /tmp/phantomjs-1.9.8-linux-x86_64.tar.bz2 -C /tmp && \
  cp /tmp/phantomjs-1.9.8-linux-x86_64/bin/phantomjs /usr/local/bin/

WORKDIR /root

# Cleaning
RUN \
  apt-get -q autoremove && \
  apt-get -q clean -y && \
  rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
  rm -rf /var/cache/apt/*.bin