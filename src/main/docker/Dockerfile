#FROM flurdy/oracle-java8
#FROM frolvlad/alpine-oraclejdk8:slim
FROM lwieske/java-8
ARG APP_NAME
VOLUME /tmp
ADD demoapp-0.1.0.war app.war
RUN sh -c 'touch /app.war'
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.war" ]