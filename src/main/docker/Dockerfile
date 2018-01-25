FROM openjdk:8-jre-alpine

# map /tmp to /var/lib/docker on host system which is tomcat working dir
VOLUME /tmp
# add jar to docker image
ADD maven/blog-0.0.1-SNAPSHOT.jar /app.jar
# give modified date
RUN sh -c 'touch /app.jar'
ENTRYPOINT ["java","-Dspring.profiles.active=default","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
