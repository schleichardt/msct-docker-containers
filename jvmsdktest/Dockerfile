FROM msct/jdk8-sbt

MAINTAINER schleichardt "https://github.com/schleichardt/msct-docker-containers"

RUN sudo apt-get install -y --force-yes git && \
    cd /tmp && git clone https://github.com/sphereio/sphere-jvm-sdk.git jvm-sdk-for-deps && \
    cd jvm-sdk-for-deps && sbt test:compile it:test::compile && cd && rm -rf /tmp/jvm-sdk-for-deps