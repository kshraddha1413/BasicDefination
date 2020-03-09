**SOLID** https://www.edureka.co/blog/solid-principles-in-java/
1)**Single Responsiblity Principle**
According to the single responsibility principle, there should be only one reason due to which a class has to be changed. It means that a class should have one task to do. for e.g. Imagine there is a class which performs following operations.


public class task{
   Public void connectToDB(String username, String pwd)();
   public void readData(String tableName)();
   public writeToFile(Sting fileName)();
}
there are too many reasons for the class to change; hence, it doesn’t fit properly in the single responsibility principle.

why Single responsibily principle is required:
1)It leads to better code organization since smaller and well-purposed classes are easier to search.
2)When the Single Responsibility Principle is followed, testing is easier

2)**Open Closed Principle**
describes it as Software components should be open for extension, but closed for modification.
For e.g.
public class Rectangle
{
public double length;
public double width;
}
public class AreaCalculator
{
  public double calculateRectangleArea(Rectangle rectangle)
 {
  return rectangle.length *rectangle.width;
 }
}
public class Circle
{
public double radius;
}
public class AreaCalculator
 
{
   public double calculateRectangleArea(Rectangle rectangle)
  {
     return rectangle.length *rectangle.width;
     }
public double calculateCircleArea(Circle circle)
 
    {
return (22/7)*circle.radius*circle.radius;
  }
}
Lets say we have a new shape pentagon. In that case, we will again end up modifying the AreaCalculator class. As the types of shapes grows this becomes messier as AreaCalculator keeps on changing.
 As a result, AreaCalculator class will not be baselined(finalized) with surety as every time a new shape comes it will be modified. So, this design is not closed for modification.
 
 Modification of above design to comply with opened/closed principle:
 
 We will first of all make the design extensible. For this we need to first define a base type Shape and have Circle & Rectangle implement Shape interface.
 
 public interface Shape
{
public double calculateArea();
}
 
public class Rectangle implements Shape
{
double length;
double width;
public double calculateArea()
{
return length * width;
}
}
 
public class Circle implements Shape
{
public double radius;
public double calculateArea()
{
return (22/7)*radius*radius;
}
}
public class AreaCalculator
{
public double calculateShapeArea(Shape shape)
{
return shape.calculateArea();
}
}

Why is that this principle is required?
OCP is important since classes may come to us through third-party libraries. We should be able to extend those classes without worrying if those base classes can support our extensions. But inheritance may lead to subclasses which depend on base class implementation. To avoid this, use of interfaces is recommended. This additional abstraction leads to loose coupling.

3)**Liskov Substitution Principle**
describes it as Derived types must be completely substitutable for their base types.
Why is that this principle is required?
This avoids misusing inheritance. It helps us conform to the “is-a” relationship.
The LSP is popularly explained using the square and rectangle example. if we assume an ISA relationship between Square and Rectangle. Thus, we call “Square is a Rectangle.” The code below represents the relationship.
public class Rectangle
{
private int length;
private int breadth;
public int getLength()
{
return length;
}
public void setLength(int length)
{
this.length = length;
}
public int getBreadth()
{
return breadth;
}
public void setBreadth(int breadth)
{
this.breadth = breadth;
}
public int getArea()
{
return this.length * this.breadth;
}
}
Below is the code for Square. Note that Square extends Rectangle.
public class Square extends Rectangle
{
 
public void setBreadth(int breadth)
{
super.setBreadth(breadth);
super.setLength(breadth);
}
 
public void setLength(int length)
{
super.setLength(length);
super.setBreadth(length);
}
}
public class LSPDemo
{
public void calculateArea(Rectangle r)
{
r.setBreadth(2);
r.setLength(3);
assert r.getArea() == 6 : printError("area", r);
assert r.getLength() == 3 : printError("length", r);
assert r.getBreadth() == 2 : printError("breadth", r);
}
private String printError(String errorIdentifer, Rectangle r)
{
return "Unexpected value of " + errorIdentifer + " for instance of " + r.getClass().getName();
}
public static void main(String[] args)
{
LSPDemo lsp = new LSPDemo();
// An instance of Rectangle is passed
lsp.calculateArea(new Rectangle());
// An instance of Square is passed
lsp.calculateArea(new Square());
}
}
4)**Interface Segregation Principle**

describes it as clients should not be forced to implement unnecessary methods which they will not use.

5)**Dependency Inversion Principle:**
   Depend upon abstractions (Interfaces) rather then on concrete classes

Why is that this principle is required?
It allows a programmer to remove hardcoded dependencies so that the application becomes loosely coupled and extendable.

public class Student
{
   private Address address;
   public Student()
  {
    address = new Address();
   }
}
In the above example, Student class requires an Address object and it is responsible for initializing and using the Address object. If Address class is changed in future then we have to make changes in Student class also. This makes the tight coupling between Student and Address objects. We can resolve this problem using the dependency inversion design pattern. i.e. Address object will be implemented independently and will be provided to Student when Student is instantiated by using constructor-based or setter-based dependency inversion.









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
