FROM ubuntu
MAINTAINER "bandi.venkatesh@hotmail.com"
RUN apt-get update -y && \
    apt-get install -y tzdata && \
    apt-get install -y openjdk-8-jdk
COPY target/camel-ose-springboot-xml-1.0.0-SNAPSHOT.jar /var/tmp/
COPY src/main/resources/logback.xml /var/tmp/
ENTRYPOINT ["java", "-Dlogback.configurationFile=/var/tmp/logback.xml", "-jar", "/var/tmp/camel-ose-springboot-xml-1.0.0-SNAPSHOT.jar"]
EXPOSE 95 80