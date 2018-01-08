# spring-cloud-eureka
A simple eureka server and client created using spring cloud.

Eureka is the Netflix Service Discovery Server and Client. 
The server can be configured and deployed to be highly available, with each server replicating state about the registered services to the others and has a home page with a UI, and HTTP API endpoints per the normal Eureka functionality under /eureka/*.
 
When a client registers with Eureka, it provides meta-data about itself such as host and port, health indicator URL, home page etc. 
Eureka receives heartbeat messages from each instance belonging to a service. 
If the heartbeat fails over a configurable timetable, the instance is normally removed from the registry.

### prerequisites
1. Java 1.8
2. Maven 3.5.2
3. Tomcat 7
4. Postgresql 42.1.4
5. Spring Tool Suite IDE

### setup
1. Clone this project
2. Open both discovery and eureka-client as separate maven projects.
3. Update maven dependencies in both.
4. Take separate jar builds of both projects and run them on server.
5. Hit `http://localhost:8761` for the Eureka server portal.
6. Check the running instances for the `eureka-client` and click on it to view the info.

So the eureka-client is now registered with the Eureka server.

### code style formatter
[Spring Boot Java Conventions](https://gist.github.com/jyotsnasanthosh/e2fb456f0ff91aa42ad8203e148bff79)
Save this as xml and import into eclipse -> window -> preferences -> java -> code style -> formatter