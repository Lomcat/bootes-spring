# Summary

* [Introduction](README.md)
* [I. Spring Framework 概述](#I)

  * [1. Getting Started with Spring](#1)
  * [2. Introduction to the Spring Framework](#2)
    * [2.1. Dependency Injection and Inversion of Control](#2.1)
    * [2.2. Modules](#2.2)
      * [2.2.1. Core Container](#2.2.1)
      * [2.2.2. AOP and Instrumentation](#2.2.2)
      * [2.2.3. Messaging](#2.2.3)
      * [2.2.4. Data Access/Integration](#2.2.4)
      * [2.2.5. Web](#2.2.5)
      * [2.2.6. Test](#2.2.6)
    * [2.3. Usage scenarios](#2.3)
      * [2.3.1. Dependency Management and Naming Conventions](#2.3.1)
        * [Spring Dependencies and Depending on Spring](#2.3.1.1)
        * [Maven Dependency Management](#2.3.1.2)
        * [Maven "Bill Of Materials" Dependency](#2.3.1.3)
        * [Gradle Dependency Management](#2.3.1.4)
        * [Ivy Dependency Management](#2.3.1.5)
        * [Distribution Zip Files](#2.3.1.6)
      * [2.3.2. Logging](#2.3.2)
        * [Not Using Commons Logging](#2.3.2.1)
        * [Using SLF4J](#2.3.2.2)
        * [Using Log4J](#2.3.2.3)

* [II. Core Technologies](#2)
  * [3. The IoC container](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans)
  * [3.1. Introduction to the Spring IoC container and beans](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-introduction)
  * [3.2. Container overview](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-basics)
    * [3.2.1. Configuration metadata](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-metadata)
    * [3.2.2. Instantiating a container](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-instantiation)
      * [Composing XML-based configuration metadata](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-xml-import)
    * [3.2.3. Using the container](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-client)

[3.3. Bean overview](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-definition)

[3.3.1. Naming beans](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-beanname)

[Aliasing a bean outside the bean definition](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-beanname-alias)

[3.3.2. Instantiating beans](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-class)

[Instantiation with a constructor](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-class-ctor)

[Instantiation with a static factory method](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-class-static-factory-method)

[Instantiation using an instance factory method](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-class-instance-factory-method)

[3.4. Dependencies](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-dependencies)

[3.4.1. Dependency Injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-collaborators)

[Constructor-based dependency injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-constructor-injection)

[Setter-based dependency injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-setter-injection)

[Dependency resolution process](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-dependency-resolution)

[Examples of dependency injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-some-examples)

[3.4.2. Dependencies and configuration in detail](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-properties-detailed)

[Straight values \(primitives, Strings, and so on\)](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-value-element)

[References to other beans \(collaborators\)](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-ref-element)

[Inner beans](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-inner-beans)

[Collections](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-collection-elements)

[Null and empty string values](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-null-element)

[XML shortcut with the p-namespace](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-p-namespace)

[XML shortcut with the c-namespace](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-c-namespace)

[Compound property names](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-compound-property-names)

[3.4.3. Using depends-on](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-dependson)

[3.4.4. Lazy-initialized beans](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-lazy-init)

[3.4.5. Autowiring collaborators](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-autowire)

[Limitations and disadvantages of autowiring](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-autowired-exceptions)

[Excluding a bean from autowiring](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-autowire-candidate)

[3.4.6. Method injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-method-injection)

[Lookup method injection](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-lookup-method-injection)

[Arbitrary method replacement](http://docs.spring.io/spring/docs/5.0.0.M4/spring-framework-reference/htmlsingle/#beans-factory-arbitrary-method-replacement)



