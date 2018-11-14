# SpringBootConsulServiceDiscovery

## Technologies

- Spring Boot Parent POM 1.5.11.RELEASE
- GORM 6.1.9.RELEASE
- Hibernate Core / Ecache 5.1.0.Final
- Tomcat JDBC 8.5.0
- Java 8
- Thymeleaf

## Groovy Sources

First of all the project must to know were to find the `sources` for this we need to add the next line to our *pom.xml* file:

```xml
<build>
    <sourceDirectory>src/main/groovy</sourceDirectory>
    <!-- Some other configurations -->
</build>
```


## Run instances

```
$> mvn clean package
$> java -jar spring-boot-front/target/person-front-0.1-SNAPSHOT.jar >> front.log &
$> java -jar spring-boot-service/target/person-service-0.1-SNAPSHOT.jar >> service.log &
```

Front App: http://localhost:8080/
