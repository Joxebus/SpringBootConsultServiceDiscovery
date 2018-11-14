# SpringBootConsulServiceDiscovery

## Technologies

- Spring Boot Parent POM 1.5.11.RELEASE
- GORM 6.1.9.RELEASE
- Hibernate Core / Ecache 5.1.0.Final
- Tomcat JDBC 8.5.0
- Java 8
- Thymeleaf
- Consul
- Docker

## Groovy Sources

First of all the project must to know were to find the `sources` for this we need to add the next line to our *pom.xml* file:

```xml
<build>
    <sourceDirectory>src/main/groovy</sourceDirectory>
    <!-- Some other configurations -->
</build>
```

## Run Consul with Docker

```
$> docker run -d --name=dev-consul -p 8500:8500/tcp -p 8300:8300/tcp -p 8301:8301/udp -p 8302:8302/udp -p 8600:8600/udp  -e CONSUL_BIND_INTERFACE=eth0 consul:latest
```

Consul UI manager: http://localhost:8500/ui/dc1/services

## Setup execution permission

```
$> chmod u+x run_nodes.sh
$> chmod u+x stop_nodes.sh
```

## Run multiple instances

```
$> mvn clean package
$> ./run_nodes.sh
```

Front App: http://localhost:8080/

## Run single instance

```
$> java -jar spring-boot-service/target/person-service-0.1-SNAPSHOT.jar --server.port=8081 >> service1.txt &
```
