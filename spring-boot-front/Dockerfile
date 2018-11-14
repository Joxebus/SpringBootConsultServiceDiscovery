FROM openjdk:8u171-alpine3.7
ENV SERVER_PORT 8081
RUN apk --no-cache add curl
EXPOSE ${SERVER_PORT}/tcp
COPY target/person-front-*.jar person-front.jar
CMD java ${JAVA_OPTS} -jar person-front.jar --spring.cloud.consul.host=consul
