# Spring Boot Package Error

This sample project demonstrates an issue packaging a Spring Boot application in which a class, other than the one decorated with @SpringBootApplication, contains a main method.  When this situation arises, the typical packaging commands, in this case mvn package, fails to build the Spring Boot jar because a scanner has found 2 main methods.

## Command

    mvn clean package


## Desired Outcome

The Spring Boot packaging plugins for both maven and gradle should be able to select the appropriate main method when packaging the jar.