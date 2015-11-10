FROM ubuntu:14.04

MAINTAINER commercetools "https:/commercetools.de"

RUN sudo apt-get update
RUN sudo apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:brightbox/ruby-ng
RUN sudo apt-get update
RUN sudo apt-get install -y --force-yes ruby2.1 ruby2.1-dev make gcc nodejs
RUN sudo apt-get install -y --force-yes curl
RUN sudo gem install jekyll -v '3.0.0'
RUN sudo gem install bundler
RUN sudo gem install rake
RUN sudo apt-get install -y --force-yes zlib1g-dev libxml2
RUN sudo apt-get install -y --force-yes libxslt-dev libxml2-dev zlib1g-dev
RUN sudo apt-get install -y --force-yes libxslt1-dev
RUN sudo apt-get install -y --force-yes libghc-zlib-dev
RUN sudo apt-get install -y --force-yes libgmp3-dev
RUN sudo gem install nokogiri -- --use-system-libraries=true --with-xml2-include=/usr/include/libxml2/
RUN sudo gem install addressable
RUN sudo gem install coffee-script-source execjs ffi
RUN sudo gem install jekyll -v 3.0.0
RUN sudo gem install jekyll-assets
RUN sudo gem install redcarpet rouge jekyll-coffeescript html-proofer
RUN sudo gem install sprockets sprockets-helpers typhoeus yell
RUN sudo gem install

WORKDIR /srv/jekyll
EXPOSE 4000 4000
#TODO combine
#TODE ruby 2.2