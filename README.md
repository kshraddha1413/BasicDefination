
**Microservice**

A microservices architecture takes this same approach and extends it to the loosely coupled services which can be developed, deployed, and maintained independently. Each of these services is responsible for discrete task and can communicate with other services through simple APIs to solve a larger complex business problem.




**What is Spring Boot?**

Spring Boot is an open source Java-based framework used to create a micro Service. It is used to build stand-alone and production ready spring applications.


1)Spring Boot provides a good platform for Java developers to develop a stand-alone and production-grade spring application that you can just run.

You can get started with minimum configurations without the need for an entire Spring configuration setup.


**Features**
Create stand-alone Spring applications

Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files)

Provide opinionated 'starter' dependencies to simplify your build configuration

Automatically configure Spring and 3rd party libraries whenever possible

Provide production-ready features such as metrics, health checks and externalized configuration

Absolutely no code generation and no requirement for XML configuration
2)It gives us a starter and we have to download dependencies as per our requirement and  .You can start writing code  get with minimum configurations without the need for an entire Spring configuration setup. 
Why Spring Boot?
You can choose Spring Boot because of the features and benefits it offers as given here −

It provides a flexible way to configure Java Beans, XML configurations, and Database Transactions.

It provides a powerful batch processing and manages REST endpoints.

In Spring Boot, everything is auto configured; no manual configurations are needed.
Features
Create stand-alone Spring applications

Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files)

Provide opinionated 'starter' dependencies to simplify your build configuration

Automatically configure Spring and 3rd party libraries whenever possible

Provide production-ready features such as metrics, health checks and externalized configuration

Absolutely no code generation and no requirement for XML configuration
It offers annotation-based spring application

Eases dependency management
Advantages:

It includes Embedded Servlet Container
3)so reduces development time
4)Increases Productivity
5)Easy to understand and developed spring application


Advantages

Spring Boot offers the following advantages to its developers −

Easy to understand and develop spring applications
Increases productivity
Reduces the development time




How does it work?
Spring Boot automatically configures your application based on the dependencies you have added to the project by using @EnableAutoConfiguration annotation. For example, if MySQL database is on your classpath, but you have not configured any database connection, then Spring Boot auto-configures an in-memory database.

The entry point of the spring boot application is the class contains @SpringBootApplication annotation and the main method.

Spring Boot automatically scans all the components included in the project by using @ComponentScan annotation.

********************************************************************************************
**Git/Git nub**

Git is a VCS — Version Control System. What that really means is, Git helps us manage our project files.
In short, Git is Version Control System and GitHub is a hosting service for Git Repositories.

GitHub is a web-based service for version control using Git. Basically, it is a social networking site for developers. 
You can look at other people’s code, identify issues with their code and even propose changes. 
This also helps you in improving your code. On a lighter note, 
it is a great place to show off your projects and get noticed by potential recruiters.


Source control (or version control) is the practice of tracking and managing
changes to code/ documents.

Source control management (SCM) systems provide

a running history of code development and help to resolve conflicts when merging
contributions from multiple sources.

enables multiple people to simultaneously work on a single project. Each person
edits his or her own copy of the files and chooses when to share those changes with
the rest of the team. integrates work done simultaneously by different team
members

Version control gives access to historical versions of your project. This is insurance
against computer crashes or data lossage.if you make a mistake you can rollback to previoius version of code

**REST ful API**
REST - Representational state transfer
**It is architactural style as well as an apprroch of comminication purpose thats is often used by web service development .**


REST or RESTful API design (Representational State Transfer) is designed to take advantage of existing protocols. While REST can be used over nearly any protocol, 
it usually takes advantage of HTTP methods GET,PUT,POST,DELETE.
Rest API is stateless:
stateless means server not holds the all information for request.client has to send all the information needed for server in every htttp request.
https://restfulapi.net/statelessness/
Statelessness means that every HTTP request happens in complete isolation. When the client makes an HTTP request, it includes all information necessary for the server to fulfill that request. The server never relies on information from previous requests. If that information was important, the client would have sent it again in this request.


REST stands for REpresentational State Transfer.
It means when a RESTful API is called, the server will transfer to the client a representation of the state of the requested resource.
For example, when a developer calls Instagram API to fetch a specific user (the resource), the API will return the state of that user, including their name, the number of posts that user posted on Instagram so far, how many followers they have, and more.
The representation of the state can be in a JSON format, and probably for most APIs this is indeed the case. It can also be in XML or HTML format.
