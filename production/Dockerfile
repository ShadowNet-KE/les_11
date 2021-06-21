FROM alpine:3.13

ARG path_to_war

# Install Tomcat 9
RUN apk add openjdk8-jre \
    && wget http://apache.rediris.es/tomcat/tomcat-9/v9.0.46/bin/apache-tomcat-9.0.46.tar.gz -O /tmp/tomcat9.tar.gz \
    && mkdir /opt/tomcat \
    && tar xvzf /tmp/tomcat9.tar.gz  --strip-components 1 --directory /opt/tomcat \
    && rm /tmp/tomcat9.tar.gz

# Copy artifacts
WORKDIR /opt/tomcat/webapps
COPY ${path_to_war} .

# Container launch conditions
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]