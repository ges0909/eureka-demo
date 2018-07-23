# Eureka

See:

* [Service Registration and Discovery](https://spring.io/guides/gs/service-registration-and-discovery/#scratch)
* [Introduction to Spring Cloud Netflix – Eureka](http://www.baeldung.com/spring-cloud-netflix-eureka)

Start service.

```bash
cd service
gradlew bootrun
```

Start client. [Actuator](http://www.baeldung.com/spring-boot-actuators) should be enabled.

```bash
cd client
gradlew bootrun
```

Navigate [http://localhost:8761/](http://localhost:8761/).
