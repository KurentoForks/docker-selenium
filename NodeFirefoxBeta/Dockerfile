FROM selenium/node-base:2.47.1
MAINTAINER Kurento <info@kurento.org>

USER root

#=========
# Firefox
#=========
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0AB215679C571D1C8325275B9BDB3D89CE49EC21  \
  && echo "deb http://ppa.launchpad.net/mozillateam/firefox-next/ubuntu trusty main" >> /etc/apt/sources.list.d/firefox-beta.list \
  && apt-get update -qqy \
  && apt-get -qqy --no-install-recommends install \
    firefox \
  && rm -rf /var/lib/apt/lists/*

#========================
# Selenium Configuration
#========================
COPY config.json /opt/selenium/config.json

USER seluser
