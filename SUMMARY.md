# Summary

* [Introduction](README.md)
* I Overview of Spring Framework
	* 1 Getting Started with Spring
	* 2 Introduction to the Spring Framework
		* 2.1 Dependency Injection and Inversion of Control
		* 2.2 Modules
			* 2.2.1 Core Container
			* 2.2.2 AOP and Instrumentation
			* 2.2.3 Messaging
			* 2.2.4 Data Access/Integration
			* 2.2.5 Web
			* 2.2.6 Test
		* 2.3 Usage scenarios
			* 2.3.1 Dependency Management and Naming Conventions
				* Spring Dependencies and Depending on Spring
				* Maven Dependency Management
				* Maven "Bill Of Materials" Dependency
				* Gradle Dependency Management
				* Ivy Dependency Management
				* Distribution Zip Files
			* 2.3.2 Logging
				* Not Using Commons Logging
				* Using SLF4J
				* Using Log4J
* II Core Technologies
	* 3 The IoC container
		* 3.1 Introduction to the Spring IoC container and beans
		* 3.2 Container overview
			* 3.2.1 Configuration metadata
			* 3.2.2 Instantiating a container
				* Composing XML-based configuration metadata
			* 3.2.3 Using the container
		* 3.3 Bean overview
			* 3.3.1 Naming beans
				* Aliasing a bean outside the bean definition
			* 3.3.2 Instantiating beans
				* Instantiation with a constructor
				* Instantiation with a static factory method
				* Instantiation using an instance factory method
		* 3.4 Dependencies
			* 3.4.1 Dependency Injection
				* Constructor-based dependency injection
				* Setter-based dependency injection
				* Dependency resolution process
				* Examples of dependency injection
			* 3.4.2 Dependencies and configuration in detail
				* Straight values (primitives, Strings, and so on)
				* References to other beans (collaborators)
				* Inner beans
				* Collections
				* Null and empty string values
				* XML shortcut with the p-namespace
				* XML shortcut with the c-namespace
				* Compound property names
			* 3.4.3 Using depends-on
			* 3.4.4 Lazy-initialized beans
			* 3.4.5 Autowiring collaborators
				* Limitations and disadvantages of autowiring
				* Excluding a bean from autowiring
			* 3.4.6 Method injection
				* Lookup method injection
				* Arbitrary method replacement
		* 3.5 Bean scopes
			* 3.5.1 The singleton scope
			* 3.5.2 The prototype scope
			* 3.5.3 Singleton beans with prototype-bean dependencies
			* 3.5.4 Request, session, application, and WebSocket scopes
				* Initial web configuration
				* Request scope
				* Session scope
				* Application scope
				* Scoped beans as dependencies
			* 3.5.5 Custom scopes
				* Creating a custom scope
				* Using a custom scope
		* 3.6 Customizing the nature of a bean
			* 3.6.1 Lifecycle callbacks
				* Initialization callbacks
				* Destruction callbacks
				* Default initialization and destroy methods
				* Combining lifecycle mechanisms
				* Startup and shutdown callbacks
				* Shutting down the Spring IoC container gracefully in non-web applications
			* 3.6.2 ApplicationContextAware and BeanNameAware
			* 3.6.3 Other Aware interfaces
		* 3.7 Bean definition inheritance
		* 3.8 Container Extension Points
			* 3.8.1 Customizing beans using a BeanPostProcessor
				* Example: Hello World, BeanPostProcessor-style
				* Example: The RequiredAnnotationBeanPostProcessor
			* 3.8.2 Customizing configuration metadata with a BeanFactoryPostProcessor
				* Example: the Class name substitution PropertyPlaceholderConfigurer
				* Example: the PropertyOverrideConfigurer
			* 3.8.3 Customizing instantiation logic with a FactoryBean
		* 3.9 Annotation-based container configuration
			* 3.9.1 @Required
			* 3.9.2 @Autowired
			* 3.9.3 Fine-tuning annotation-based autowiring with @Primary
			* 3.9.4 Fine-tuning annotation-based autowiring with qualifiers
			* 3.9.5 Using generics as autowiring qualifiers
			* 3.9.6 CustomAutowireConfigurer
			* 3.9.7 @Resource
			* 3.9.8 @PostConstruct and @PreDestroy
		* 3.10 Classpath scanning and managed components
			* 3.10.1 @Component and further stereotype annotations
			* 3.10.2 Meta-annotations
			* 3.10.3 Automatically detecting classes and registering bean definitions
			* 3.10.4 Using filters to customize scanning
			* 3.10.5 Defining bean metadata within components
			* 3.10.6 Naming autodetected components
			* 3.10.7 Providing a scope for autodetected components
			* 3.10.8 Providing qualifier metadata with annotations
		* 3.11 Using JSR 330 Standard Annotations
			* 3.11.1 Dependency Injection with @Inject and @Named
			* 3.11.2 @Named and @ManagedBean: standard equivalents to the @Component annotation
			* 3.11.3 Limitations of JSR-330 standard annotations
		* 3.12 Java-based container configuration
			* 3.12.1 Basic concepts: @Bean and @Configuration
			* 3.12.2 Instantiating the Spring container using AnnotationConfigApplicationContext
				* Simple construction
				* Building the container programmatically using register(Class&lt;?&gt;…​)
				* Enabling component scanning with scan(String…​)
				* Support for web applications with AnnotationConfigWebApplicationContext
			* 3.12.3 Using the @Bean annotation
				* Declaring a bean
				* Bean dependencies
				* Receiving lifecycle callbacks
				* Specifying bean scope
				* Customizing bean naming
				* Bean aliasing
				* Bean description
			* 3.12.4 Using the @Configuration annotation
				* Injecting inter-bean dependencies
				* Lookup method injection
				* Further information about how Java-based configuration works internally
			* 3.12.5 Composing Java-based configurations
				* Using the @Import annotation
				* Conditionally include @Configuration classes or @Bean methods
				* Combining Java and XML configuration
		* 3.13 Environment abstraction
			* 3.13.1 Bean definition profiles
				* @Profile
			* 3.13.2 XML bean definition profiles
				* Activating a profile
				* Default profile
			* 3.13.3 PropertySource abstraction
			* 3.13.4 @PropertySource
			* 3.13.5 Placeholder resolution in statements
		* 3.14 Registering a LoadTimeWeaver
		* 3.15 Additional Capabilities of the ApplicationContext
			* 3.15.1 Internationalization using MessageSource
			* 3.15.2 Standard and Custom Events
				* Annotation-based Event Listeners
				* Asynchronous Listeners
				* Ordering Listeners
				* Generic Events
			* 3.15.3 Convenient access to low-level resources
			* 3.15.4 Convenient ApplicationContext instantiation for web applications
			* 3.15.5 Deploying a Spring ApplicationContext as a Java EE RAR file
		* 3.16 The BeanFactory
			* 3.16.1 BeanFactory or ApplicationContext?
			* 3.16.2 Glue code and the evil singleton
	* 4 Resources
		* 4.1 Introduction
		* 4.2 The Resource interface
		* 4.3 Built-in Resource implementations
			* 4.3.1 UrlResource
			* 4.3.2 ClassPathResource
			* 4.3.3 FileSystemResource
			* 4.3.4 ServletContextResource
			* 4.3.5 InputStreamResource
			* 4.3.6 ByteArrayResource
		* 4.4 The ResourceLoader
		* 4.5 The ResourceLoaderAware interface
		* 4.6 Resources as dependencies
		* 4.7 Application contexts and Resource paths
			* 4.7.1 Constructing application contexts
				* Constructing ClassPathXmlApplicationContext instances - shortcuts
			* 4.7.2 Wildcards in application context constructor resource paths
				* Ant-style Patterns
				* The Classpath*: portability classpath*: prefix
				* Other notes relating to wildcards
			* 4.7.3 FileSystemResource caveats
	* 5 Validation, Data Binding, and Type Conversion
		* 5.1 Introduction
		* 5.2 Validation using Spring’s Validator interface
		* 5.3 Resolving codes to error messages
		* 5.4 Bean manipulation and the BeanWrapper
			* 5.4.1 Setting and getting basic and nested properties
			* 5.4.2 Built-in PropertyEditor implementations
				* Registering additional custom PropertyEditors
		* 5.5 Spring Type Conversion
			* 5.5.1 Converter SPI
			* 5.5.2 ConverterFactory
			* 5.5.3 GenericConverter
				* ConditionalGenericConverter
			* 5.5.4 ConversionService API
			* 5.5.5 Configuring a ConversionService
			* 5.5.6 Using a ConversionService programmatically
		* 5.6 Spring Field Formatting
			* 5.6.1 Formatter SPI
			* 5.6.2 Annotation-driven Formatting
				* Format Annotation API
			* 5.6.3 FormatterRegistry SPI
			* 5.6.4 FormatterRegistrar SPI
			* 5.6.5 Configuring Formatting in Spring MVC
		* 5.7 Configuring a global date & time format
		* 5.8 Spring Validation
			* 5.8.1 Overview of the JSR-303 Bean Validation API
			* 5.8.2 Configuring a Bean Validation Provider
				* Injecting a Validator
				* Configuring Custom Constraints
				* Spring-driven Method Validation
				* Additional Configuration Options
			* 5.8.3 Configuring a DataBinder
			* 5.8.4 Spring MVC 3 Validation
	* 6 Spring Expression Language (SpEL)
		* 6.1 Introduction
		* 6.2 Feature Overview
		* 6.3 Expression Evaluation using Spring’s Expression Interface
			* 6.3.1 The EvaluationContext interface
				* Type Conversion
			* 6.3.2 Parser configuration
			* 6.3.3 SpEL compilation
				* Compiler configuration
				* Compiler limitations
		* 6.4 Expression support for defining bean definitions
			* 6.4.1 XML based configuration
			* 6.4.2 Annotation-based configuration
		* 6.5 Language Reference
			* 6.5.1 Literal expressions
			* 6.5.2 Properties, Arrays, Lists, Maps, Indexers
			* 6.5.3 Inline lists
			* 6.5.4 Inline Maps
			* 6.5.5 Array construction
			* 6.5.6 Methods
			* 6.5.7 Operators
				* Relational operators
				* Logical operators
				* Mathematical operators
			* 6.5.8 Assignment
			* 6.5.9 Types
			* 6.5.10 Constructors
			* 6.5.11 Variables
				* The #this and #root variables
			* 6.5.12 Functions
			* 6.5.13 Bean references
			* 6.5.14 Ternary Operator (If-Then-Else)
			* 6.5.15 The Elvis Operator
			* 6.5.16 Safe Navigation operator
			* 6.5.17 Collection Selection
			* 6.5.18 Collection Projection
			* 6.5.19 Expression templating
		* 6.6 Classes used in the examples
	* 7 Aspect Oriented Programming with Spring
		* 7.1 Introduction
			* 7.1.1 AOP concepts
			* 7.1.2 Spring AOP capabilities and goals
			* 7.1.3 AOP Proxies
		* 7.2 @AspectJ support
			* 7.2.1 Enabling @AspectJ Support
				* Enabling @AspectJ Support with Java configuration
				* Enabling @AspectJ Support with XML configuration
			* 7.2.2 Declaring an aspect
			* 7.2.3 Declaring a pointcut
				* Supported Pointcut Designators
				* Combining pointcut expressions
				* Sharing common pointcut definitions
				* Examples
				* Writing good pointcuts
			* 7.2.4 Declaring advice
				* Before advice
				* After returning advice
				* After throwing advice
				* After (finally) advice
				* Around advice
				* Advice parameters
				* Advice ordering
			* 7.2.5 Introductions
			* 7.2.6 Aspect instantiation models
			* 7.2.7 Example
		* 7.3 Schema-based AOP support
			* 7.3.1 Declaring an aspect
			* 7.3.2 Declaring a pointcut
			* 7.3.3 Declaring advice
				* Before advice
				* After returning advice
				* After throwing advice
				* After (finally) advice
				* Around advice
				* Advice parameters
				* Advice ordering
			* 7.3.4 Introductions
			* 7.3.5 Aspect instantiation models
			* 7.3.6 Advisors
			* 7.3.7 Example
		* 7.4 Choosing which AOP declaration style to use
			* 7.4.1 Spring AOP or full AspectJ?
			* 7.4.2 @AspectJ or XML for Spring AOP?
		* 7.5 Mixing aspect types
		* 7.6 Proxying mechanisms
			* 7.6.1 Understanding AOP proxies
		* 7.7 Programmatic creation of @AspectJ Proxies
		* 7.8 Using AspectJ with Spring applications
			* 7.8.1 Using AspectJ to dependency inject domain objects with Spring
				* Unit testing @Configurable objects
				* Working with multiple application contexts
			* 7.8.2 Other Spring aspects for AspectJ
			* 7.8.3 Configuring AspectJ aspects using Spring IoC
			* 7.8.4 Load-time weaving with AspectJ in the Spring Framework
				* A first example
				* Aspects
				* 'META-INF/aop.xml'
				* Required libraries (JARS)
				* Spring configuration
				* Environment-specific configuration
		* 7.9 Further Resources
	* 8 Spring AOP APIs
		* 8.1 Introduction
		* 8.2 Pointcut API in Spring
			* 8.2.1 Concepts
			* 8.2.2 Operations on pointcuts
			* 8.2.3 AspectJ expression pointcuts
			* 8.2.4 Convenience pointcut implementations
				* Static pointcuts
				* Dynamic pointcuts
			* 8.2.5 Pointcut superclasses
			* 8.2.6 Custom pointcuts
		* 8.3 Advice API in Spring
			* 8.3.1 Advice lifecycles
			* 8.3.2 Advice types in Spring
				* Interception around advice
				* Before advice
				* Throws advice
				* After Returning advice
				* Introduction advice
		* 8.4 Advisor API in Spring
		* 8.5 Using the ProxyFactoryBean to create AOP proxies
			* 8.5.1 Basics
			* 8.5.2 JavaBean properties
			* 8.5.3 JDK- and CGLIB-based proxies
			* 8.5.4 Proxying interfaces
			* 8.5.5 Proxying classes
			* 8.5.6 Using 'global' advisors
		* 8.6 Concise proxy definitions
		* 8.7 Creating AOP proxies programmatically with the ProxyFactory
		* 8.8 Manipulating advised objects
		* 8.9 Using the "auto-proxy" facility
			* 8.9.1 Autoproxy bean definitions
				* BeanNameAutoProxyCreator
				* DefaultAdvisorAutoProxyCreator
				* AbstractAdvisorAutoProxyCreator
			* 8.9.2 Using metadata-driven auto-proxying
		* 8.10 Using TargetSources
			* 8.10.1 Hot swappable target sources
			* 8.10.2 Pooling target sources
			* 8.10.3 Prototype target sources
			* 8.10.4 ThreadLocal target sources
		* 8.11 Defining new Advice types
		* 8.12 Further resources
* III Testing
	* 9 Introduction to Spring Testing
	* 10 Unit Testing
		* 10.1 Mock Objects
			* 10.1.1 Environment
			* 10.1.2 JNDI
			* 10.1.3 Servlet API
		* 10.2 Unit Testing support Classes
			* 10.2.1 General testing utilities
			* 10.2.2 Spring MVC
	* 11 Integration Testing
		* 11.1 Overview
		* 11.2 Goals of Integration Testing
			* 11.2.1 Context management and caching
			* 11.2.2 Dependency Injection of test fixtures
			* 11.2.3 Transaction management
			* 11.2.4 Support classes for integration testing
		* 11.3 JDBC Testing Support
		* 11.4 Annotations
			* 11.4.1 Spring Testing Annotations
				* @BootstrapWith
				* @ContextConfiguration
				* @WebAppConfiguration
				* @ContextHierarchy
				* @ActiveProfiles
				* @TestPropertySource
				* @DirtiesContext
				* @TestExecutionListeners
				* @Commit
				* @Rollback
				* @BeforeTransaction
				* @AfterTransaction
				* @Sql
				* @SqlConfig
				* @SqlGroup
			* 11.4.2 Standard Annotation Support
			* 11.4.3 Spring JUnit 4 Testing Annotations
				* @IfProfileValue
				* @ProfileValueSourceConfiguration
				* @Timed
				* @Repeat
			* 11.4.4 Meta-Annotation Support for Testing
		* 11.5 Spring TestContext Framework
			* 11.5.1 Key abstractions
				* TestContext
				* TestContextManager
				* TestExecutionListener
				* Context Loaders
			* 11.5.2 Bootstrapping the TestContext framework
			* 11.5.3 TestExecutionListener configuration
				* Registering custom TestExecutionListeners
				* Automatic discovery of default TestExecutionListeners
				* Ordering TestExecutionListeners
				* Merging TestExecutionListeners
			* 11.5.4 Context management
				* Context configuration with XML resources
				* Context configuration with Groovy scripts
				* Context configuration with annotated classes
				* Mixing XML, Groovy scripts, and annotated classes
				* Context configuration with context initializers
				* Context configuration inheritance
				* Context configuration with environment profiles
				* Context configuration with test property sources
				* Loading a WebApplicationContext
				* Context caching
				* Context hierarchies
			* 11.5.5 Dependency injection of test fixtures
			* 11.5.6 Testing request and session scoped beans
			* 11.5.7 Transaction management
				* Test-managed transactions
				* Enabling and disabling transactions
				* Transaction rollback and commit behavior
				* Programmatic transaction management
				* Executing code outside of a transaction
				* Configuring a transaction manager
				* Demonstration of all transaction-related annotations
			* 11.5.8 Executing SQL scripts
				* Executing SQL scripts programmatically
				* Executing SQL scripts declaratively with @Sql
			* 11.5.9 Parallel test execution
			* 11.5.10 TestContext Framework support classes
				* Spring JUnit 4 Runner
				* Spring JUnit 4 Rules
				* JUnit 4 support classes
				* TestNG support classes
		* 11.6 Spring MVC Test Framework
			* 11.6.1 Server-Side Tests
				* Static Imports
				* Setup Options
				* Performing Requests
				* Defining Expectations
				* Filter Registrations
				* Differences between Out-of-Container and End-to-End Integration Tests
				* Further Server-Side Test Examples
			* 11.6.2 HtmlUnit Integration
				* Why HtmlUnit Integration?
				* MockMvc and HtmlUnit
				* MockMvc and WebDriver
				* MockMvc and Geb
			* 11.6.3 Client-Side REST Tests
				* Static Imports
				* Further Examples of Client-side REST Tests
		* 11.7 PetClinic Example
	* 12 Further Resources
* IV Data Access
	* 13 Transaction Management
		* 13.1 Introduction to Spring Framework transaction management
		* 13.2 Advantages of the Spring Framework’s transaction support model
			* 13.2.1 Global transactions
			* 13.2.2 Local transactions
			* 13.2.3 Spring Framework’s consistent programming model
		* 13.3 Understanding the Spring Framework transaction abstraction
		* 13.4 Synchronizing resources with transactions
			* 13.4.1 High-level synchronization approach
			* 13.4.2 Low-level synchronization approach
			* 13.4.3 TransactionAwareDataSourceProxy
		* 13.5 Declarative transaction management
			* 13.5.1 Understanding the Spring Framework’s declarative transaction implementation
			* 13.5.2 Example of declarative transaction implementation
			* 13.5.3 Rolling back a declarative transaction
			* 13.5.4 Configuring different transactional semantics for different beans
			* 13.5.5 &lt;tx:advice/&gt; settings
			* 13.5.6 Using @Transactional
				* @Transactional settings
				* Multiple Transaction Managers with @Transactional
				* Custom shortcut annotations
			* 13.5.7 Transaction propagation
				* Required
				* RequiresNew
				* Nested
			* 13.5.8 Advising transactional operations
			* 13.5.9 Using @Transactional with AspectJ
		* 13.6 Programmatic transaction management
			* 13.6.1 Using the TransactionTemplate
				* Specifying transaction settings
			* 13.6.2 Using the PlatformTransactionManager
		* 13.7 Choosing between programmatic and declarative transaction management
		* 13.8 Transaction bound event
		* 13.9 Application server-specific integration
			* 13.9.1 IBM WebSphere
			* 13.9.2 Oracle WebLogic Server
		* 13.10 Solutions to common problems
			* 13.10.1 Use of the wrong transaction manager for a specific DataSource
		* 13.11 Further Resources
	* 14 DAO support
		* 14.1 Introduction
		* 14.2 Consistent exception hierarchy
		* 14.3 Annotations used for configuring DAO or Repository classes
	* 15 Data access with JDBC
		* 15.1 Introduction to Spring Framework JDBC
			* 15.1.1 Choosing an approach for JDBC database access
			* 15.1.2 Package hierarchy
		* 15.2 Using the JDBC core classes to control basic JDBC processing and error handling
			* 15.2.1 JdbcTemplate
				* Examples of JdbcTemplate class usage
				* JdbcTemplate best practices
			* 15.2.2 NamedParameterJdbcTemplate
			* 15.2.3 SQLExceptionTranslator
			* 15.2.4 Executing statements
			* 15.2.5 Running queries
			* 15.2.6 Updating the database
			* 15.2.7 Retrieving auto-generated keys
		* 15.3 Controlling database connections
			* 15.3.1 DataSource
			* 15.3.2 DataSourceUtils
			* 15.3.3 SmartDataSource
			* 15.3.4 AbstractDataSource
			* 15.3.5 SingleConnectionDataSource
			* 15.3.6 DriverManagerDataSource
			* 15.3.7 TransactionAwareDataSourceProxy
			* 15.3.8 DataSourceTransactionManager
			* 15.3.9 NativeJdbcExtractor
		* 15.4 JDBC batch operations
			* 15.4.1 Basic batch operations with the JdbcTemplate
			* 15.4.2 Batch operations with a List of objects
			* 15.4.3 Batch operations with multiple batches
		* 15.5 Simplifying JDBC operations with the SimpleJdbc classes
			* 15.5.1 Inserting data using SimpleJdbcInsert
			* 15.5.2 Retrieving auto-generated keys using SimpleJdbcInsert
			* 15.5.3 Specifying columns for a SimpleJdbcInsert
			* 15.5.4 Using SqlParameterSource to provide parameter values
			* 15.5.5 Calling a stored procedure with SimpleJdbcCall
			* 15.5.6 Explicitly declaring parameters to use for a SimpleJdbcCall
			* 15.5.7 How to define SqlParameters
			* 15.5.8 Calling a stored function using SimpleJdbcCall
			* 15.5.9 Returning ResultSet/REF Cursor from a SimpleJdbcCall
		* 15.6 Modeling JDBC operations as Java objects
			* 15.6.1 SqlQuery
			* 15.6.2 MappingSqlQuery
			* 15.6.3 SqlUpdate
			* 15.6.4 StoredProcedure
		* 15.7 Common problems with parameter and data value handling
			* 15.7.1 Providing SQL type information for parameters
			* 15.7.2 Handling BLOB and CLOB objects
			* 15.7.3 Passing in lists of values for IN clause
			* 15.7.4 Handling complex types for stored procedure calls
		* 15.8 Embedded database support
			* 15.8.1 Why use an embedded database?
			* 15.8.2 Creating an embedded database using Spring XML
			* 15.8.3 Creating an embedded database programmatically
			* 15.8.4 Selecting the embedded database type
				* Using HSQL
				* Using H2
				* Using Derby
			* 15.8.5 Testing data access logic with an embedded database
			* 15.8.6 Generating unique names for embedded databases
			* 15.8.7 Extending the embedded database support
		* 15.9 Initializing a DataSource
			* 15.9.1 Initializing a database using Spring XML
				* Initialization of other components that depend on the database
	* 16 Object Relational Mapping (ORM) Data Access
		* 16.1 Introduction to ORM with Spring
		* 16.2 General ORM integration considerations
			* 16.2.1 Resource and transaction management
			* 16.2.2 Exception translation
		* 16.3 Hibernate
			* 16.3.1 SessionFactory setup in a Spring container
			* 16.3.2 Implementing DAOs based on plain Hibernate API
			* 16.3.3 Declarative transaction demarcation
			* 16.3.4 Programmatic transaction demarcation
			* 16.3.5 Transaction management strategies
			* 16.3.6 Comparing container-managed and locally defined resources
			* 16.3.7 Spurious application server warnings with Hibernate
		* 16.4 JPA
			* 16.4.1 Three options for JPA setup in a Spring environment
				* LocalEntityManagerFactoryBean
				* Obtaining an EntityManagerFactory from JNDI
				* LocalContainerEntityManagerFactoryBean
				* Dealing with multiple persistence units
			* 16.4.2 Implementing DAOs based on JPA: EntityManagerFactory and EntityManager
			* 16.4.3 Spring-driven JPA transactions
			* 16.4.4 JpaDialect and JpaVendorAdapter
			* 16.4.5 Setting up JPA with JTA transaction management
	* 17 Marshalling XML using O/X Mappers
		* 17.1 Introduction
			* 17.1.1 Ease of configuration
			* 17.1.2 Consistent Interfaces
			* 17.1.3 Consistent Exception Hierarchy
		* 17.2 Marshaller and Unmarshaller
			* 17.2.1 Marshaller
			* 17.2.2 Unmarshaller
			* 17.2.3 XmlMappingException
		* 17.3 Using Marshaller and Unmarshaller
		* 17.4 XML Schema-based Configuration
		* 17.5 JAXB
			* 17.5.1 Jaxb2Marshaller
				* XML Schema-based Configuration
		* 17.6 Castor
			* 17.6.1 CastorMarshaller
			* 17.6.2 Mapping
				* XML Schema-based Configuration
		* 17.7 JiBX
			* 17.7.1 JibxMarshaller
				* XML Schema-based Configuration
		* 17.8 XStream
			* 17.8.1 XStreamMarshaller
* V The Web
	* 18 Web MVC framework
		* 18.1 Introduction to Spring Web MVC framework
			* 18.1.1 Features of Spring Web MVC
			* 18.1.2 Pluggability of other MVC implementations
		* 18.2 The DispatcherServlet
			* 18.2.1 Special Bean Types In the WebApplicationContext
			* 18.2.2 Default DispatcherServlet Configuration
			* 18.2.3 DispatcherServlet Processing Sequence
		* 18.3 Implementing Controllers
			* 18.3.1 Defining a controller with @Controller
			* 18.3.2 Mapping Requests With @RequestMapping
				* Composed @RequestMapping Variants
				* @Controller and AOP Proxying
				* New Support Classes for @RequestMapping methods in Spring MVC 3.1
				* URI Template Patterns
				* URI Template Patterns with Regular Expressions
				* Path Patterns
				* Path Pattern Comparison
				* Path Patterns with Placeholders
				* Suffix Pattern Matching
				* Suffix Pattern Matching and RFD
				* Matrix Variables
				* Consumable Media Types
				* Producible Media Types
				* Request Parameters and Header Values
				* HTTP HEAD and HTTP OPTIONS
			* 18.3.3 Defining @RequestMapping handler methods
				* Supported method argument types
				* Supported method return types
				* Binding request parameters to method parameters with @RequestParam
				* Mapping the request body with the @RequestBody annotation
				* Mapping the response body with the @ResponseBody annotation
				* Creating REST Controllers with the @RestController annotation
				* Using HttpEntity
				* Using @ModelAttribute on a method
				* Using @ModelAttribute on a method argument
				* Using @SessionAttributes to store model attributes in the HTTP session between requests
				* Using @SessionAttribute to access pre-existing global session attributes
				* Using @RequestAttribute to access request attributes
				* Working with "application/x-www-form-urlencoded" data
				* Mapping cookie values with the @CookieValue annotation
				* Mapping request header attributes with the @RequestHeader annotation
				* Method Parameters And Type Conversion
				* Customizing WebDataBinder initialization
				* Advising controllers with @ControllerAdvice and @RestControllerAdvice
				* Jackson Serialization View Support
				* Jackson JSONP Support
			* 18.3.4 Asynchronous Request Processing
				* Exception Handling for Async Requests
				* Intercepting Async Requests
				* HTTP Streaming
				* HTTP Streaming With Server-Sent Events
				* HTTP Streaming Directly To The OutputStream
				* Configuring Asynchronous Request Processing
			* 18.3.5 Testing Controllers
		* 18.4 Handler mappings
			* 18.4.1 Intercepting requests with a HandlerInterceptor
		* 18.5 Resolving views
			* 18.5.1 Resolving views with the ViewResolver interface
			* 18.5.2 Chaining ViewResolvers
			* 18.5.3 Redirecting to Views
				* RedirectView
				* The redirect: prefix
				* The forward: prefix
			* 18.5.4 ContentNegotiatingViewResolver
		* 18.6 Using flash attributes
		* 18.7 Building URIs
			* 18.7.1 Building URIs to Controllers and methods
			* 18.7.2 Building URIs to Controllers and methods from views
		* 18.8 Using locales
			* 18.8.1 Obtaining Time Zone Information
			* 18.8.2 AcceptHeaderLocaleResolver
			* 18.8.3 CookieLocaleResolver
			* 18.8.4 SessionLocaleResolver
			* 18.8.5 LocaleChangeInterceptor
		* 18.9 Using themes
			* 18.9.1 Overview of themes
			* 18.9.2 Defining themes
			* 18.9.3 Theme resolvers
		* 18.10 Spring’s multipart (file upload) support
			* 18.10.1 Introduction
			* 18.10.2 Using a MultipartResolver with Commons FileUpload
			* 18.10.3 Using a MultipartResolver with Servlet 3.0
			* 18.10.4 Handling a file upload in a form
			* 18.10.5 Handling a file upload request from programmatic clients
		* 18.11 Handling exceptions
			* 18.11.1 HandlerExceptionResolver
			* 18.11.2 @ExceptionHandler
			* 18.11.3 Handling Standard Spring MVC Exceptions
			* 18.11.4 REST Controller Exception Handling
			* 18.11.5 Annotating Business Exceptions With @ResponseStatus
			* 18.11.6 Customizing the Default Servlet Container Error Page
		* 18.12 Web Security
		* 18.13 Convention over configuration support
			* 18.13.1 The Controller ControllerClassNameHandlerMapping
			* 18.13.2 The Model ModelMap (ModelAndView)
			* 18.13.3 The View - RequestToViewNameTranslator
		* 18.14 HTTP caching support
			* 18.14.1 Cache-Control HTTP header
			* 18.14.2 HTTP caching support for static resources
			* 18.14.3 Support for the Cache-Control, ETag and Last-Modified response headers in Controllers
			* 18.14.4 Shallow ETag support
		* 18.15 Code-based Servlet container initialization
		* 18.16 Configuring Spring MVC
			* 18.16.1 Enabling the MVC Java Config or the MVC XML Namespace
			* 18.16.2 Customizing the Provided Configuration
			* 18.16.3 Conversion and Formatting
			* 18.16.4 Validation
			* 18.16.5 Interceptors
			* 18.16.6 Content Negotiation
			* 18.16.7 View Controllers
			* 18.16.8 View Resolvers
			* 18.16.9 Serving of Resources
			* 18.16.10 Falling Back On the "Default" Servlet To Serve Resources
			* 18.16.11 Path Matching
			* 18.16.12 Message Converters
			* 18.16.13 Advanced Customizations with MVC Java Config
			* 18.16.14 Advanced Customizations with the MVC Namespace
	* 19 View technologies
		* 19.1 Introduction
		* 19.2 Thymeleaf
		* 19.3 Groovy Markup Templates
			* 19.3.1 Configuration
			* 19.3.2 Example
		* 19.4 FreeMarker
			* 19.4.1 Dependencies
			* 19.4.2 Context configuration
			* 19.4.3 Creating templates
			* 19.4.4 Advanced FreeMarker configuration
			* 19.4.5 Bind support and form handling
				* The bind macros
				* Simple binding
				* Form input generation macros
				* HTML escaping and XHTML compliance
		* 19.5 JSP & JSTL
			* 19.5.1 View resolvers
			* 19.5.2 'Plain-old' JSPs versus JSTL
			* 19.5.3 Additional tags facilitating development
			* 19.5.4 Using Spring’s form tag library
				* Configuration
				* The form tag
				* The input tag
				* The checkbox tag
				* The checkboxes tag
				* The radiobutton tag
				* The radiobuttons tag
				* The password tag
				* The select tag
				* The option tag
				* The options tag
				* The textarea tag
				* The hidden tag
				* The errors tag
				* HTTP Method Conversion
				* HTML5 Tags
		* 19.6 Script templates
			* 19.6.1 Dependencies
			* 19.6.2 How to integrate script based templating
		* 19.7 XML Marshalling View
		* 19.8 Tiles
			* 19.8.1 Dependencies
			* 19.8.2 How to integrate Tiles
				* UrlBasedViewResolver
				* ResourceBundleViewResolver
				* SimpleSpringPreparerFactory and SpringBeanPreparerFactory
		* 19.9 XSLT
			* 19.9.1 My First Words
				* Bean definitions
				* Standard MVC controller code
				* Document transformation
		* 19.10 Document views (PDF/Excel)
			* 19.10.1 Introduction
			* 19.10.2 Configuration and setup
				* Document view definitions
				* Controller code
				* Subclassing for Excel views
				* Subclassing for PDF views
		* 19.11 Feed Views
		* 19.12 JSON Mapping View
		* 19.13 XML Mapping View
	* 20 CORS Support
		* 20.1 Introduction
		* 20.2 Controller method CORS configuration
		* 20.3 Global CORS configuration
			* 20.3.1 JavaConfig
			* 20.3.2 XML namespace
		* 20.4 Advanced Customization
		* 20.5 Filter based CORS support
	* 21 Integrating with other web frameworks
		* 21.1 Introduction
		* 21.2 Common configuration
		* 21.3 JavaServer Faces 1.2
			* 21.3.1 SpringBeanFacesELResolver (JSF 1.2+)
			* 21.3.2 FacesContextUtils
		* 21.4 Apache Struts 2.x
		* 21.5 Tapestry 5.x
		* 21.6 Further Resources
	* 22 WebSocket Support
		* 22.1 Introduction
			* 22.1.1 WebSocket Fallback Options
			* 22.1.2 A Messaging Architecture
			* 22.1.3 Sub-Protocol Support in WebSocket
			* 22.1.4 Should I Use WebSocket?
		* 22.2 WebSocket API
			* 22.2.1 Create and Configure a WebSocketHandler
			* 22.2.2 Customizing the WebSocket Handshake
			* 22.2.3 WebSocketHandler Decoration
			* 22.2.4 Deployment Considerations
			* 22.2.5 Configuring the WebSocket Engine
			* 22.2.6 Configuring allowed origins
		* 22.3 SockJS Fallback Options
			* 22.3.1 Overview of SockJS
			* 22.3.2 Enable SockJS
			* 22.3.3 HTTP Streaming in IE 8, 9: Ajax/XHR vs IFrame
			* 22.3.4 Heartbeat Messages
			* 22.3.5 Servlet 3 Async Requests
			* 22.3.6 CORS Headers for SockJS
			* 22.3.7 SockJS Client
		* 22.4 STOMP Over WebSocket Messaging Architecture
			* 22.4.1 Overview of STOMP
			* 22.4.2 Enable STOMP over WebSocket
			* 22.4.3 Flow of Messages
			* 22.4.4 Annotation Message Handling
			* 22.4.5 Sending Messages
			* 22.4.6 Simple Broker
			* 22.4.7 Full-Featured Broker
			* 22.4.8 Connections To Full-Featured Broker
			* 22.4.9 Using Dot as Separator in @MessageMapping Destinations
			* 22.4.10 Authentication
			* 22.4.11 Token-based Authentication
			* 22.4.12 User Destinations
			* 22.4.13 Listening To ApplicationContext Events and Intercepting Messages
			* 22.4.14 STOMP Client
			* 22.4.15 WebSocket Scope
			* 22.4.16 Configuration and Performance
			* 22.4.17 Runtime Monitoring
			* 22.4.18 Testing Annotated Controller Methods
	* 23 Reactive Web Applications
		* 23.1 Introduction
			* 23.1.1 What is Reactive Programming?
			* 23.1.2 Reactive API and Building Blocks
		* 23.2 Spring Web Reactive Module
			* 23.2.1 Server Side
				* Annotation-based Programming Model
				* Functional Programming Model
			* 23.2.2 Client Side
			* 23.2.3 Request and Response Body Conversion
			* 23.2.4 Reactive WebSocket Support
		* 23.3 Getting Started
			* 23.3.1 Spring Boot Starter
			* 23.3.2 Manual Bootstrapping
			* 23.3.3 Examples
* VI Integration
	* 24 Remoting and web services using Spring
		* 24.1 Introduction
		* 24.2 Exposing services using RMI
			* 24.2.1 Exporting the service using the RmiServiceExporter
			* 24.2.2 Linking in the service at the client
		* 24.3 Using Hessian to remotely call services via HTTP
			* 24.3.1 Wiring up the DispatcherServlet for Hessian and co.
			* 24.3.2 Exposing your beans by using the HessianServiceExporter
			* 24.3.3 Linking in the service on the client
			* 24.3.4 Applying HTTP basic authentication to a service exposed through Hessian
		* 24.4 Exposing services using HTTP invokers
			* 24.4.1 Exposing the service object
			* 24.4.2 Linking in the service at the client
		* 24.5 Web services
			* 24.5.1 Exposing servlet-based web services using JAX-WS
			* 24.5.2 Exporting standalone web services using JAX-WS
			* 24.5.3 Exporting web services using the JAX-WS RI’s Spring support
			* 24.5.4 Accessing web services using JAX-WS
		* 24.6 JMS
			* 24.6.1 Server-side configuration
			* 24.6.2 Client-side configuration
		* 24.7 AMQP
		* 24.8 Auto-detection is not implemented for remote interfaces
		* 24.9 Considerations when choosing a technology
		* 24.10 Accessing RESTful services on the Client
			* 24.10.1 RestTemplate
				* Working with the URI
				* Dealing with request and response headers
				* Jackson JSON Views support
			* 24.10.2 HTTP Message Conversion
				* StringHttpMessageConverter
				* FormHttpMessageConverter
				* ByteArrayHttpMessageConverter
				* MarshallingHttpMessageConverter
				* MappingJackson2HttpMessageConverter
				* MappingJackson2XmlHttpMessageConverter
				* SourceHttpMessageConverter
				* BufferedImageHttpMessageConverter
			* 24.10.3 Async RestTemplate
	* 25 Enterprise JavaBeans (EJB) integration
		* 25.1 Introduction
		* 25.2 Accessing EJBs
			* 25.2.1 Concepts
			* 25.2.2 Accessing local SLSBs
			* 25.2.3 Accessing remote SLSBs
			* 25.2.4 Accessing EJB 2.x SLSBs versus EJB 3 SLSBs
		* 25.3 Using Spring’s EJB implementation support classes
			* 25.3.1 EJB 3 injection interceptor
	* 26 JMS (Java Message Service)
		* 26.1 Introduction
		* 26.2 Using Spring JMS
			* 26.2.1 JmsTemplate
			* 26.2.2 Connections
				* Caching Messaging Resources
				* SingleConnectionFactory
				* CachingConnectionFactory
			* 26.2.3 Destination Management
			* 26.2.4 Message Listener Containers
				* SimpleMessageListenerContainer
				* DefaultMessageListenerContainer
			* 26.2.5 Transaction management
		* 26.3 Sending a Message
			* 26.3.1 Using Message Converters
			* 26.3.2 SessionCallback and ProducerCallback
		* 26.4 Receiving a message
			* 26.4.1 Synchronous Reception
			* 26.4.2 Asynchronous Reception - Message-Driven POJOs
			* 26.4.3 the SessionAwareMessageListener interface
			* 26.4.4 the MessageListenerAdapter
			* 26.4.5 Processing messages within transactions
		* 26.5 Support for JCA Message Endpoints
		* 26.6 Annotation-driven listener endpoints
			* 26.6.1 Enable listener endpoint annotations
			* 26.6.2 Programmatic endpoints registration
			* 26.6.3 Annotated endpoint method signature
			* 26.6.4 Response management
		* 26.7 JMS namespace support
	* 27 JMX
		* 27.1 Introduction
		* 27.2 Exporting your beans to JMX
			* 27.2.1 Creating an MBeanServer
			* 27.2.2 Reusing an existing MBeanServer
			* 27.2.3 Lazy-initialized MBeans
			* 27.2.4 Automatic registration of MBeans
			* 27.2.5 Controlling the registration behavior
		* 27.3 Controlling the management interface of your beans
			* 27.3.1 the MBeanInfoAssembler Interface
			* 27.3.2 Using Source-Level Metadata (Java annotations)
			* 27.3.3 Source-Level Metadata Types
			* 27.3.4 the AutodetectCapableMBeanInfoAssembler interface
			* 27.3.5 Defining management interfaces using Java interfaces
			* 27.3.6 Using MethodNameBasedMBeanInfoAssembler
		* 27.4 Controlling the ObjectNames for your beans
			* 27.4.1 Reading ObjectNames from Properties
			* 27.4.2 Using the MetadataNamingStrategy
			* 27.4.3 Configuring annotation based MBean export
		* 27.5 JSR-160 Connectors
			* 27.5.1 Server-side Connectors
			* 27.5.2 Client-side Connectors
			* 27.5.3 JMX over Hessian or SOAP
		* 27.6 Accessing MBeans via Proxies
		* 27.7 Notifications
			* 27.7.1 Registering Listeners for Notifications
			* 27.7.2 Publishing Notifications
		* 27.8 Further Resources
	* 28 JCA CCI
		* 28.1 Introduction
		* 28.2 Configuring CCI
			* 28.2.1 Connector configuration
			* 28.2.2 ConnectionFactory configuration in Spring
			* 28.2.3 Configuring CCI connections
			* 28.2.4 Using a single CCI connection
		* 28.3 Using Spring’s CCI access support
			* 28.3.1 Record conversion
			* 28.3.2 the CciTemplate
			* 28.3.3 DAO support
			* 28.3.4 Automatic output record generation
			* 28.3.5 Summary
			* 28.3.6 Using a CCI Connection and Interaction directly
			* 28.3.7 Example for CciTemplate usage
		* 28.4 Modeling CCI access as operation objects
			* 28.4.1 MappingRecordOperation
			* 28.4.2 MappingCommAreaOperation
			* 28.4.3 Automatic output record generation
			* 28.4.4 Summary
			* 28.4.5 Example for MappingRecordOperation usage
			* 28.4.6 Example for MappingCommAreaOperation usage
		* 28.5 Transactions
	* 29 Email
		* 29.1 Introduction
		* 29.2 Usage
			* 29.2.1 Basic MailSender and SimpleMailMessage usage
			* 29.2.2 Using the JavaMailSender and the MimeMessagePreparator
		* 29.3 Using the JavaMail MimeMessageHelper
			* 29.3.1 Sending attachments and inline resources
				* Attachments
				* Inline resources
			* 29.3.2 Creating email content using a templating library
	* 30 Task Execution and Scheduling
		* 30.1 Introduction
		* 30.2 The Spring TaskExecutor abstraction
			* 30.2.1 TaskExecutor types
			* 30.2.2 Using a TaskExecutor
		* 30.3 The Spring TaskScheduler abstraction
			* 30.3.1 the Trigger interface
			* 30.3.2 Trigger implementations
			* 30.3.3 TaskScheduler implementations
		* 30.4 Annotation Support for Scheduling and Asynchronous Execution
			* 30.4.1 Enable scheduling annotations
			* 30.4.2 The @Scheduled annotation
			* 30.4.3 The @Async annotation
			* 30.4.4 Executor qualification with @Async
			* 30.4.5 Exception management with @Async
		* 30.5 The task namespace
			* 30.5.1 The 'scheduler' element
			* 30.5.2 The 'executor' element
			* 30.5.3 The 'scheduled-tasks' element
		* 30.6 Using the Quartz Scheduler
			* 30.6.1 Using the JobDetailFactoryBean
			* 30.6.2 Using the MethodInvokingJobDetailFactoryBean
			* 30.6.3 Wiring up jobs using triggers and the SchedulerFactoryBean
	* 31 Dynamic language support
		* 31.1 Introduction
		* 31.2 A first example
		* 31.3 Defining beans that are backed by dynamic languages
			* 31.3.1 Common concepts
				* The &lt;lang:language/&gt; element
				* Refreshable beans
				* Inline dynamic language source files
				* Understanding Constructor Injection in the context of dynamic-language-backed beans
			* 31.3.2 JRuby beans
			* 31.3.3 Groovy beans
				* Customizing Groovy objects via a callback
			* 31.3.4 BeanShell beans
		* 31.4 Scenarios
			* 31.4.1 Scripted Spring MVC Controllers
			* 31.4.2 Scripted Validators
		* 31.5 Bits and bobs
			* 31.5.1 AOP - advising scripted beans
			* 31.5.2 Scoping
		* 31.6 Further Resources
	* 32 Cache Abstraction
		* 32.1 Introduction
		* 32.2 Understanding the cache abstraction
		* 32.3 Declarative annotation-based caching
			* 32.3.1 @Cacheable annotation
				* Default Key Generation
				* Custom Key Generation Declaration
				* Default Cache Resolution
				* Custom cache resolution
				* Synchronized caching
				* Conditional caching
				* Available caching SpEL evaluation context
			* 32.3.2 @CachePut annotation
			* 32.3.3 @CacheEvict annotation
			* 32.3.4 @Caching annotation
			* 32.3.5 @CacheConfig annotation
			* 32.3.6 Enable caching annotations
			* 32.3.7 Using custom annotations
		* 32.4 JCache (JSR-107) annotations
			* 32.4.1 Features summary
			* 32.4.2 Enabling JSR-107 support
		* 32.5 Declarative XML-based caching
		* 32.6 Configuring the cache storage
			* 32.6.1 JDK ConcurrentMap-based Cache
			* 32.6.2 Ehcache-based Cache
			* 32.6.3 Caffeine Cache
			* 32.6.4 GemFire-based Cache
			* 32.6.5 JSR-107 Cache
			* 32.6.6 Dealing with caches without a backing store
		* 32.7 Plugging-in different back-end caches
		* 32.8 How can I set the TTL/TTI/Eviction policy/XXX feature?
* VII Appendices
	* 33 What’s New in the Spring Framework
	* 34 Migrating to Spring Framework 4.x
	* 35 Spring Annotation Programming Model
	* 36 Classic Spring Usage
		* 36.1 Classic ORM usage
			* 36.1.1 Hibernate
				* The HibernateTemplate
				* Implementing Spring-based DAOs without callbacks
		* 36.2 JMS Usage
			* 36.2.1 JmsTemplate
			* 36.2.2 Asynchronous Message Reception
			* 36.2.3 Connections
			* 36.2.4 Transaction Management
	* 37 Classic Spring AOP Usage
		* 37.1 Pointcut API in Spring
			* 37.1.1 Concepts
			* 37.1.2 Operations on pointcuts
			* 37.1.3 AspectJ expression pointcuts
			* 37.1.4 Convenience pointcut implementations
				* Static pointcuts
				* Dynamic pointcuts
			* 37.1.5 Pointcut superclasses
			* 37.1.6 Custom pointcuts
		* 37.2 Advice API in Spring
			* 37.2.1 Advice lifecycles
			* 37.2.2 Advice types in Spring
				* Interception around advice
				* Before advice
				* Throws advice
				* After Returning advice
				* Introduction advice
		* 37.3 Advisor API in Spring
		* 37.4 Using the ProxyFactoryBean to create AOP proxies
			* 37.4.1 Basics
			* 37.4.2 JavaBean properties
			* 37.4.3 JDK- and CGLIB-based proxies
			* 37.4.4 Proxying interfaces
			* 37.4.5 Proxying classes
			* 37.4.6 Using 'global' advisors
		* 37.5 Concise proxy definitions
		* 37.6 Creating AOP proxies programmatically with the ProxyFactory
		* 37.7 Manipulating advised objects
		* 37.8 Using the "autoproxy" facility
			* 37.8.1 Autoproxy bean definitions
				* BeanNameAutoProxyCreator
				* DefaultAdvisorAutoProxyCreator
				* AbstractAdvisorAutoProxyCreator
			* 37.8.2 Using metadata-driven auto-proxying
		* 37.9 Using TargetSources
			* 37.9.1 Hot swappable target sources
			* 37.9.2 Pooling target sources
			* 37.9.3 Prototype target sources
			* 37.9.4 ThreadLocal target sources
		* 37.10 Defining new Advice types
		* 37.11 Further resources
	* 38 XML Schema-based configuration
		* 38.1 Introduction
		* 38.2 XML Schema-based configuration
			* 38.2.1 Referencing the schemas
			* 38.2.2 the util schema
				* &lt;util:constant/&gt;
				* &lt;util:property-path/&gt;
				* &lt;util:properties/&gt;
				* &lt;util:list/&gt;
				* &lt;util:map/&gt;
				* &lt;util:set/&gt;
			* 38.2.3 the jee schema
				* &lt;jee:jndi-lookup/&gt; (simple)
				* &lt;jee:jndi-lookup/&gt; (with single JNDI environment setting)
				* &lt;jee:jndi-lookup/&gt; (with multiple JNDI environment settings)
				* &lt;jee:jndi-lookup/&gt; (complex)
				* &lt;jee:local-slsb/&gt; (simple)
				* &lt;jee:local-slsb/&gt; (complex)
				* &lt;jee:remote-slsb/&gt;
			* 38.2.4 the lang schema
			* 38.2.5 the jms schema
			* 38.2.6 the tx (transaction) schema
			* 38.2.7 the aop schema
			* 38.2.8 the context schema
				* &lt;property-placeholder/&gt;
				* &lt;annotation-config/&gt;
				* &lt;component-scan/&gt;
				* &lt;load-time-weaver/&gt;
				* &lt;spring-configured/&gt;
				* &lt;mbean-export/&gt;
			* 38.2.9 the tool schema
			* 38.2.10 the jdbc schema
			* 38.2.11 the cache schema
			* 38.2.12 the beans schema
	* 39 Extensible XML authoring
		* 39.1 Introduction
		* 39.2 Authoring the schema
		* 39.3 Coding a NamespaceHandler
		* 39.4 BeanDefinitionParser
		* 39.5 Registering the handler and the schema
			* 39.5.1 'META-INF/spring.handlers'
			* 39.5.2 'META-INF/spring.schemas'
		* 39.6 Using a custom extension in your Spring XML configuration
		* 39.7 Meatier examples
			* 39.7.1 Nesting custom tags within custom tags
			* 39.7.2 Custom attributes on 'normal' elements
		* 39.8 Further Resources
	* 40 spring JSP Tag Library
		* 40.1 Introduction
		* 40.2 The argument tag
		* 40.3 The bind tag
		* 40.4 The escapeBody tag
		* 40.5 The eval tag
		* 40.6 The hasBindErrors tag
		* 40.7 The htmlEscape tag
		* 40.8 The message tag
		* 40.9 The nestedPath tag
		* 40.10 The param tag
		* 40.11 The theme tag
		* 40.12 The transform tag
		* 40.13 The url tag
	* 41 spring-form JSP Tag Library
		* 41.1 Introduction
		* 41.2 The button tag
		* 41.3 The checkbox tag
		* 41.4 The checkboxes tag
		* 41.5 The errors tag
		* 41.6 The form tag
		* 41.7 The hidden tag
		* 41.8 The input tag
		* 41.9 The label tag
		* 41.10 The option tag
		* 41.11 The options tag
		* 41.12 The password tag
		* 41.13 The radiobutton tag
		* 41.14 The radiobuttons tag
		* 41.15 The select tag
		* 41.16 The textarea tag
