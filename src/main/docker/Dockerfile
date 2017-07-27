#FROM java:8
FROM frolvlad/alpine-oraclejdk8:slim

MAINTAINER Mahima Agarwal  <mahima.agarwal@gmail.com>

VOLUME /tmp
ADD eureka_server-2.0.jar  app.jar
RUN sh -c 'touch /app.jar'
EXPOSE 8761
ENV JAVA_OPTS="-Xmx256m"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]
