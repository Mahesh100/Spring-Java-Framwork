# Spring-Java-Framwork

Introduction To Spring

Spring is one of the best frameworks available for java.

Yes we have different framework before Example for



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


