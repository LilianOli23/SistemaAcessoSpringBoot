# Read Me First
The following was discovered as part of building this project:

* Spring Cloud Gateway requires Spring WebFlux, your choice of Spring Web has been replaced accordingly.
* The following dependencies are not known to work with Spring Native: 'Spring Boot DevTools, Spring Configuration Processor, Rest Repositories, Apache Camel, Spring Web Services, Apache Freemarker, Testcontainers, Spring HATEOAS, Gateway, JOOQ Access Layer, Jersey'. As a result, your application may not work as expected.

# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.5.2/gradle-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.5.2/gradle-plugin/reference/html/#build-image)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#using-boot-devtools)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#configuration-metadata-annotation-processor)
* [Rest Repositories](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#howto-use-exposing-spring-data-repositories-rest-endpoint)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-jpa-and-spring-data)
* [Validation](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-validation)
* [Spring Security](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-security)
* [Spring Native Reference Guide](https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/)
* [Spring Web Services](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-webservices)
* [Apache Freemarker](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-spring-mvc-template-engines)
* [JDBC API](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-sql)
* [Spring Data JDBC](https://docs.spring.io/spring-data/jdbc/docs/current/reference/html/)
* [Testcontainers](https://www.testcontainers.org/)
* [Spring HATEOAS](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-spring-hateoas)
* [JOOQ Access Layer](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-jooq)
* [Jersey](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-jersey)

### Guides
The following guides illustrate how to use some features concretely:

* [Accessing JPA Data with REST](https://spring.io/guides/gs/accessing-data-rest/)
* [Accessing Neo4j Data with REST](https://spring.io/guides/gs/accessing-neo4j-data-rest/)
* [Accessing MongoDB Data with REST](https://spring.io/guides/gs/accessing-mongodb-data-rest/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Securing a Web Application](https://spring.io/guides/gs/securing-web/)
* [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)
* [Authenticating a User with LDAP](https://spring.io/guides/gs/authenticating-ldap/)
* [Using Apache Camel with Spring Boot](https://camel.apache.org/camel-spring-boot/latest/spring-boot.html)
* [Producing a SOAP web service](https://spring.io/guides/gs/producing-web-service/)
* [Accessing Relational Data using JDBC with Spring](https://spring.io/guides/gs/relational-data-access/)
* [Managing Transactions](https://spring.io/guides/gs/managing-transactions/)
* [Using Spring Data JDBC](https://github.com/spring-projects/spring-data-examples/tree/master/jdbc/basics)
* [Building a Hypermedia-Driven RESTful Web Service](https://spring.io/guides/gs/rest-hateoas/)
* [Using Spring Cloud Gateway](https://github.com/spring-cloud-samples/spring-cloud-gateway-sample)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)
* [Configure the Spring AOT Plugin](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#spring-aot-gradle)

## Spring Native

This project has been configured to let you generate either a lightweight container or a native executable.

### Lightweight Container with Cloud Native Buildpacks
If you're already familiar with Spring Boot container images support, this is the easiest way to get started with Spring Native.
Docker should be installed and configured on your machine prior to creating the image, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#getting-started-buildpacks).

To create the image, run the following goal:

```
$ ./gradlew bootBuildImage
```

Then, you can run the app like any other container:

```
$ docker run --rm live23:0.0.1-SNAPSHOT
```

### Executable with Native Build Tools
Use this option if you want to explore more options such as running your tests in a native image.
The GraalVM native-image compiler should be installed and configured on your machine, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#getting-started-native-build-tools).

To create the executable, run the following goal:

```
$ ./gradlew nativeBuild
```

Then, you can run the app as follows:
```
$ build/native-image/live23
```
