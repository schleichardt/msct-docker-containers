FROM java:openjdk-9-jdk

ENV JAVA_HOME /usr/lib/jvm/java-9-openjdk-amd64

RUN apt-get update && apt-get install -y maven
RUN wget https://adopt-openjdk.ci.cloudbees.com/job/langtools-1.9-linux-x86_64-kulla-dev/321/artifact/kulla--20151130010028.jar
RUN mvn install:install-file -Dfile=kulla--20151130010028.jar -DgroupId=jline \
    -DartifactId=jline -Dversion=kulla--20151130010028 -Dpackaging=JAR
CMD java -jar root/.m2/repository/jline/jline/kulla--20151130010028/jline-kulla--20151130010028.JAR