FROM java:8
ARG VERSION=GITHUB
VOLUME /tmp

EXPOSE 8888
ADD target/config-server-${VERSION}-SNAPSHOT.jar app.jar
RUN sh -c 'touch /app.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]