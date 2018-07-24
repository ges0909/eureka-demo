# Eureka

Beside [Netflix Eureka](https://github.com/Netflix/eureka) Spring Boot supports
other service registries like [Hashicorp’s Consul](https://www.consul.io/) or
[Apache Zookeeper](https://zookeeper.apache.org/).

See:

* [Service Registration and Discovery](https://spring.io/guides/gs/service-registration-and-discovery/#scratch)
* [Introduction to Spring Cloud Netflix – Eureka](http://www.baeldung.com/spring-cloud-netflix-eureka)

Build service + client.

```bash
gradle wrapper
gradlew build
```

Start service.

```bash
cd service
gradle bootrun
```

Start client. [Actuator](http://www.baeldung.com/spring-boot-actuators) should be enabled.

```bash
cd client
gradle bootrun
```

Navigate to:

* [http://localhost:8761/](http://localhost:8761/)
* [http://localhost:8080/service-instances/my-microservice-name-defined-in-application-yaml](http://localhost:8080/service-instances/my-microservice-name-defined-in-application-yaml)

## Gradle

* [Multi Module Projects](https://www.petrikainulainen.net/programming/gradle/getting-started-with-gradle-creating-a-multi-project-build/)

```bash
./gradlew build && ./gradlew :service:bootRun
./gradlew build && ./gradlew :client:bootRun
```

### Spring Boot Gradle Plugin

* collects all jars on classpath and builds a single _über-jar_
* searches foe _main()_ to flag as runnable class
* provides built-in dependency resolver to match Spring Boot dependencies
  
