# Spring-Java-Framwork

Introduction To Spring

Spring is one of the best frameworks available for java.
The spring framework

Yes we have different framework before Example for--
Web Development we use Sturts.
In the enterprise market, we use happy with EJP.
For the database side, we use JPA.

But now with the spring, you can achieve everything.
The one thing that is amazing about the spring that it can focus on POJOS.(Plain Old Java Object)
Spring is actually the combination of multiple projects.

Example: If you want to achieve a very common feature of the spring which is Dependency Injection.

          We have a separate module for it and if one wants to build Web application we have separate module or it
          And if one wants to build the rest application we have separate module. The Spring Framework can also be used for security.

          **The Spring is basically the collection of the module it has**
          
          
          **The official documentation of the spring is found on the Spring.io**

The spring is designed and maintained by the Pivatol.

The spring is actually open source project.
Now,
   If click on spring project we have lot of projects    (https://spring.io/projects)
   
   
   
                                                 ***Prqusites For Spring***
   
   
-One should know java- Core java Part is very Important, you should know what is oops, what is exception handling, what is threads, loops

-The database connectivity (MySQL with java, Postgres with java, JDBC Connection is IMP)

-Servlets and JSP, In the java framework we usually work on TOMCAT, Tomcat is a servlet container which means even if you are running the spring framework on Tomcat ultimately everything is converted into the servlet. So good knowledge of servlet and JSP is important.

-The basics concepts should be strong - Ex-

-One should know how to send data from client to server, what is HTTP request object, HTTP response object, etc

-One should know ORM Framework it can be Hibernate/iBATIS/JPA

-One should know how the internet works, how the protocol works

-For spring security one should know -LDAP and OAuth.


       ***Software Requirement***

-Spring has his separate IDE called STS- Spring Tool Suite.

-And JDK 8 is a benchmark.

-Any suitable IDE.


        ***Spring Tool Suite***

-Behind the scene, STS is an Eclipse.

-It looks like an Eclipse.

-On the left-hand side we have the project section, in this section, we have all the projects.

-In the center, we have an area where we have to write a code.

-In the below section we have a console here.(All the logs will be printed here)-Here we get all the output.

    

  To create your first project in STS-

-Right-click on the project section 

  You will get-

             New-

-Hower over on New-

  You will get a drop-down list as-

  -Spring starting project

  -Import Spring started content

  -Spring legacy project

  -Java Project

  -etc

When you work with the spring framework we have to add spring Dependencies(jars).

This can be achieved by " Maven "

    A maven is basically a Build tool that will help you to

    -To Build Project

    -To get Dependencies.

    -To get a package for the project.

    -To compile your code as well.

But now we can use Maven only for Downloading Dependencies.

  -Click on Maven Project

  -Click on Create New Project.

  -Using Maven you can create Multiple Types of projects like Simple Standalone Project, Web Project, etc.

  -Now we create a "quickstart" project-A simple Project

  -Click on Next

  -Now we can give a Special Name to it

   we can give a -Group ID- com.companyName (com. google)

                 -Artifact ID-demoproject 

                 -Version -Default given

                 -Package- com. google.demoproject

  -And Now click on Finish

  -Now once you click on Finish it will download Maven dependencies, i.e it will create a project for you with the 

   all required Dependencies. 

  In order to more extra Dependencies like JAR file for spring-

  -Open your POM.xml- MAVEN works with this file, in which we have to mention the Dependencies.

  -We have to put a Dependency Tag here <Dependency>.....</Dependency>

  -Search for MVN repository this is where we can download all the maven Dependencies. (https://mvnrepository.com/)

  -Search for  "Spring"

  -Download "Spring Context"- Choose Version that has Maximum Usages.

  -Copy the code and Paste it in pom.xaml - In Dependency Tag.

  -Wait for Downloading All the Dependencies in Console Area.

  *We can also achieve with this "Gradle" (It's optional)*
  
                           **Spring Core***

-It is the first module we study from the Spring framework.

-It solves one of the famous issues which is Dependency.

-In the java world, Everything is treated as an object, if you want to achieve anything in java, you need to create an object of it.

-But when you create an Object you just create one object, we have to create multiple ones.

-Here when you create multiple objects that means you are responsible to destroy them.-That's an issue.

-The second issue we have->What if we have multiple classes?

-To solve this we have Dependencies in Spring.

 -These Dependencies are to be injected into the application which is coming from the outside world.

 -Dependency injection has one more name that is IoC-Inversion of Control.
 
 
                       ***Getting Spring Starter Project***

-The Spring is One of the best frameworks available for java.

The other frameworks are-

 -Sturts for web development

 -Hibernate for Database

But in the case of the framework, we have to do a lot of configuration to achieve the things we want.

Now when we talk about Spring-Boot 

 -Spring Boot basically focuses on "Convention over Configuration"

 -One has to focus on logic instead of basic configuration.

 -Spring boot will give you all the basic configuration.
 
 Create a Project in Spring boot-

-Right Click on the project section of STS

-Click on New

-Click on Spring Starter Project.

-Give Project name in opened Diloug Box

-Give a group ID

-Give a Package name.

-Click on Next.

-Spring Starter Project means a Spring Boot project.

-Select a Stable Spring boot Version -(2.1.2)

-Click on Next and click on finish.

pom.xml file is where you can add all the required dependencies.

***Spring Boot Autowire***

-When we use Autowire this means the object is created by spring.
- The object creation is managed by spring framework.


***Spring Core IOC***

-How the things are done behind the scean?

**Bean Factory**
-Normally a BeanFactory will load bean definitions stored in a configuration source (such as an XML document), 
 and use the org.springframework.beans package to configure the beans.
-The BeanFactory is the most basic version of IOC containers.
-Most Spring users use a BeanFactory or ApplicationContext variant which supports XML format configuration files.
-Each bean has dependencies expressed in the form of properties, constructor arguments, or arguments to the static-factory method when that is used instead of a normal  constructor.
- Bean Factory only instantiate bean when you call getBean() method.

***Application Context***

-The ApplicationContext is the central interface within a Spring application that is used for providing configuration information to the application. 
-It implements the BeanFactory interface.
-Application Contxt represents the Spring IoC container and is responsible for instantiating, configuring, and assembling the beans.
-The container gets its instructions on what objects to instantiate, configure, and assemble by reading configuration metadata.
-We can have multiple application contexts that share a parent-child relationship.
- A context hierarchy allows multiple child contexts to share beans which reside in the parent context.
- Each child context can override configuration inherited from the parent context.

***Spring Container***
-The Spring container is at the core of the Spring Framework.
-The container will create the objects, wire them together, configure them, and manage their complete life cycle from creation till destruction.
-The Spring container uses DI to manage the components.
- The IoC container receives metadata from either an XML file, Java annotations, or Java code.
- The container gets its instructions on what objects to instantiate, configure, and assemble from simple Plain Old Java Objects (POJO) by reading the configuration metadata   provided.
- The container, use for creating the objects and configuring them.

****Singleton vs Prototype spring***
-Singleton: Only one instance will be created for a single bean definition per Spring IoC container and the same object will be shared for each request made for that bean. 
-Prototype: A new instance will be created for a single bean definition every time a request is made for that bean.
-As a rule of thumb, you should use the prototype scope for all beans that are stateful, while the singleton scope should be used for stateless beans.
-Singleton, will create a new instance in the first call, and return it in subsequent calls.
-Prototype will return a new instance each time.
-With Singleton scope, one and only one instance of a bean is created with the provided bean definition and for subsequent requests for the same bean, Spring container will return the same instance
--For prototype scope, for each request for the bean, a new instance of the bean will be created and returned. This is similar to calling new operator in java for a class.

***Setter Injection***

-Spring Setter Injection is nothing but injecting the Bean Dependencies using the Setter methods on an Object.
-In Setter Injection, the object is created first and then the dependency is injected.
-Setter Injection is the preferable method of Dependency Injection (DI) in the spring framework. 
-Setter Injection in Spring is a type of dependency injection in which the framework injects the dependent objects into the client using a setter method.
-The container first calls the no argument constructor and then calls the setters. 
-The setter based injection can work even If some dependencies have been injected using the constructor.
-If you have many setter methods, then it is convenient to use p-namespace in the XML configuration file.

***Ref Attribute***
- Spring Bean Reference ,<ref> Tag in Spring. ... In Spring, beans can "access" to each other by specify the bean references in the same or different bean configuration file.
-In spring we can write multiple configuration xml file. Our associated bean may be in same xml or in other xml file.
-If there is a dependency between two objects then in the spring bean configuration file we use a tag "ref" to specify the dependencies.
-Import the xml defining the bean with <import resource="otherXml. xml"> and you will be able to use the bean definition. 
          
***Constructor injection in spring***  
-The Spring-Core module is responsible for injecting dependencies through either Constructor or Setter methods.
-The responsibility of object creation and injecting the dependencies is given to the framework (i.e. Spring) instead of the class creating the dependency objects by itself.
-We can implement dependency injection with: constructor-based injection, setter-based injection, or. field-based injection.
-Constructor Injection is the act of statically defining the list of required Dependencies by specifying them as parameters to the class's constructor
-The class that needs the Dependency must expose a public constructor that takes an instance of the required Dependency as a constructor argument.
-A constructor therefore enforces the dependency requirement whether or not you're using Spring, making it container-agnostic. 
- If you use setter injection, the setter may or may not be called, so the instance may never be provided with its dependency.
-constructor injection ensures all mandatory properties have been satisfied.

***Autowire In Spring***
- Autowiring feature of spring framework enables you to inject the object dependency implicitly.
- It internally uses setter or constructor injection. Autowiring can't be used to inject primitive and string values.
- The Spring framework enables automatic dependency injection.
- In other words, by declaring all the bean dependencies in a Spring configuration file, Spring container can autowire relationships between collaborating beans.
- This is called Spring bean autowiring.
- The autowiring functionality has four modes. 
- These are ' no ', ' byName ', ' byType ' and ' constructor '. Another autowire mode autodetect has been deprecated.
- You can use Spring's @Configurable annotation in the class you want to autowire other beans.
-  Additionally, you will need to annotate any configuration bean with @EnableSpringConfigured so that Spring is aware of your configurable beans.
-  Similar to functionality found in Spring's XML element.
-  @Autowire annotation will work only those objects which are managed by spring (ie created by the spring container).
-  In your case the service and controller object are managed by spring.
-  but your POJO class is not managed by spring, that is why the @Autowire is not producing the behavior expected by you.

***Primary Bean in spring***
-The default bean name is @Bean annotated method name.
-A bean is an object that is instantiated, assembled, and otherwise managed by a Spring IoC container. 
-These beans are created with the configuration metadata that you supply to the container.
-singleton is default bean scope in spring container.
-It tells the container to create and manage only one instance of bean class, per container.
This single instance is stored in a cache of such singleton beans, and all subsequent requests and references for that named bean return the cached instance.

***Spring MVC Theory***
-A Spring MVC is a Java framework which is used to build web applications. 
-It follows the Model-View-Controller design pattern. 
-It implements all the basic features of a core spring framework like Inversion of Control, Dependency Injection.
-The Spring Web MVC framework provides Model-View-Controller (MVC) architecture and ready components that can be used to develop flexible and loosely coupled web applications. 
-The Model encapsulates the application data and in general they will consist of POJO.
-Web frameworks like Spring MVC are designed to make building web applications, which handle HTTP requests and responses, easier.
-Most Java web frameworks, including Spring MVC, use servlets behind the scenes. 
-You CAN use servlets to write a web application, but you'll have to handle all of the details manually.

***Creating Controller in Spring***
-Application is the entry point which sets up Spring Boot application.
-The @SpringBootApplication annotation enables auto-configuration and component scanning.
-During the scanning process, the @Controller annotation is looked up and a Spring bean is created from the MyController class.
- In Spring Boot, the controller class is responsible for processing incoming REST API requests, preparing a model, and returning the view to be rendered as a response.
- The controller classes in Spring are annotated either by the @Controller or the @RestController annotation.
- -he Spring Framework does allow you to autowire private fields.

***Tomcat Jsper***
-Jasper is Tomcat's JSP Engine.
-Jasper parses JSP files to compile them into Java code as servlets (that can be handled by Catalina). 
- At runtime, Jasper detects changes to JSP files and recompiles them.
-  As of version 5, Tomcat uses Jasper 2, which is an implementation of the Sun Microsystems' JSP 2.0 specification.
-  Jasper also has a dependency on Jackson.
-Tomcat is used for web applications written in Java that don't require full Java EE specifications
- The reason Tomcat is not really a full application server is because it acts only as a Web server and Servlet container.

***@RequestParam in spring***

-In Spring MVC, the @RequestParam annotation is used to read the form data and bind it automatically to the parameter present in the provided method. 
-So, it ignores the requirement of HttpServletRequest object to read the provided data.
- @RequestParam is used to extract the data found in query parameters.
- @RequestParam is used to extract query parameters while.
- @RequestParam makes Spring to map request parameters from the GET/POST request to your method argument.  

***Model ans View In Spring***
-ModelAndView is a holder for both Model and View in the web MVC framework.
-These two classes are distinct in nature.
- ModelAndView merely holds both to make it possible for a controller to return both model and view in a single return value. 
- The view is resolved by a ViewResolver object; the model is data stored in a Map.
- The Spring Web model-view-controller (MVC) framework is designed around a DispatcherServlet that dispatches requests to handlers, with configurable handler mappings, view resolution, locale and theme resolution as well as support for uploading files.
- In Spring MVC, the model works a container that contains the data of the application.
- Here, a data can be in any form such as objects, strings, information from the database, etc.
- It is required to place the Model interface in the controller part of the application.
- The Model represents formal underlying data constructs that the View uses to present the user with the look and feel of the application.
- The @ModelAttribute is an annotation that binds a method parameter or method return value to a named model attribute and then exposes it to a web view. 

***Prefix and Suffix in Spring***
-The InternalResourceViewResolver allows mapping webpages with requests. /hello is requested, DispatcherServlet will forward the request to the prefix + viewname + suffix = /WEB-INF/jsp/hello.
-The two interfaces which are important to the way Spring handles views are ViewResolver and View . 
-The ViewResolver provides a mapping between view names and actual views.
-The View interface addresses the preparation of the request and hands the request over to one of the view technologies.
-Spring uses ViewResolver to translate the view names in @Controller to actual View.
-The Spring auto-configuration (in this case WebMvcAutoConfiguration) will add few default ViewResolvers in your context.
- One of such view resolver is InternalResourceViewResolver.

***Model AND Model Mao In spring***
--Model , ModelMap , and ModelAndView are used to define a model in a Spring MVC application.
-Model defines a holder for model attributes and is primarily designed for adding attributes to the model. 


***Model Attribute and Method Level***
-Use @ModelAttribute at the method level to provide reference data for the model. @ModelAttribute annotated methods are executed before the chosen @RequestMapping annotated handler method. 
-They effectively pre-populate the implicit model with specific attributes, often loaded from a database.
- The injection is achieved by binding a method return value to the model.
- @ModelAttribute has an element as value. 
- @ModelAttribute can be used at method level as well as parameter level. 
- The @ModelAttribute Annotation can be used at two levels in a Controller class. 
- At Method argument level & At Method level.
- It allows you to have default values in your Model Object.
- The attributes commandName and modelAttribute on the form:form tag do primarily the same thing, which is to map the form's fields to an Object of some type in the       Controller.


***Post Mapping In Spring***
-@PostMapping is specialized version of @RequestMapping annotation that acts as a shortcut for @RequestMapping(method = RequestMethod. POST).
- @PostMapping annotated methods handle the HTTP POST requests matched with given URI expression.
-@PostMapping annotation maps HTTP POST requests onto specific handler methods.
-It is a composed annotation that acts as a shortcut for @RequestMapping(method = RequestMethod. POST) .

***Spring ORM ***

-Spring-ORM is an umbrella module that covers many persistence technologies, namely JPA, JDO, Hibernate and iBatis.
- For each technology, the configuration basically consists in injecting a DataSource bean into some kind of SessionFactory or EntityManagerFactory etc. bean.
- - It doesn't provide cache, lazy loading, write-behind, or many other features of JPA.

***Spring Hibernate Configuration ***
*Simple steps for hibernate and spring integration-

-create table in the database (It is optional).
-reate applicationContext. xml file It contains information of DataSource, SessionFactory etc.
-create Employee. 
-create employee.
-create EmployeeDao.
-create InsertTest.


* Spring MVC integrate with Hibernate:-
-Step 1: Create the directory structure. Following will be the final project structure: ...
-Step 2: Update pom. xml to include required dependencies. ...
-Step 3: Configure Hibernate. ...
-Step 4: Configure Spring MVC. ...
--Step 5: Configure Initializer class. ...
-Step 6: Add Controller to handle the requests. 


****MVC and DAO Database****

-In computer software, a data access object (DAO) is a pattern that provides an abstract interface to some type of database or other persistence mechanism. 
-By mapping application calls to the persistence layer, the DAO provides some specific data operations without exposing details of the database.
-DAO is an abstraction for accessing data, the idea is to separate the technical details of data access from the rest of the application.


***Spring Data and JPA Configuration****
-Hibernate is a JPA implementation, while Spring Data JPA is a JPA Data Access Abstraction. 
-Spring Data offers a solution to GenericDao custom implementations.


***Jparepository in spring boot***
-The Spring Data JPA simplifies the development of Spring applications that use JPA technology.
-With Spring Data, we define a repository interface for each domain entity in the application. 
-A repository contains methods for performing CRUD operations, sorting and paginating data.


*** Query DSL (Domain Specific Language)***
-Elasticsearch provides a full Query DSL (Domain Specific Language) based on JSON to define queries. 
-Think of the Query DSL as an AST (Abstract Syntax Tree) of queries, consisting of two types of clauses:
  --Leaf query clauses look for a particular value in a particular field, such as the match , term or range queries.






