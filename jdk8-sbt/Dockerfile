FROM msct/jdk8

MAINTAINER schleichardt "https://github.com/schleichardt/msct-docker-containers"

RUN wget --directory-prefix=/usr/bin https://raw.githubusercontent.com/paulp/sbt-extras/master/sbt && \
 chmod +x /usr/bin/sbt && \
 mkdir -p /root/.sbt/launchers/0.13.9/ && \
 wget --directory-prefix=/root/.sbt/launchers/0.13.9/ http://dl.bintray.com/typesafe/ivy-releases/org.scala-sbt/sbt-launch/0.13.9/sbt-launch.jar