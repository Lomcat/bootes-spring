## Part I. Spring 框架概述

Spring 是一个开源框架，为创建企业级应用程序提供了一个轻量级的解决方案。Spring 的主要优势之一是分层架构，虽然 Spring 包含的功能很多，但这些功能被设计为多个可独立存在的模块，你可以只使用需要的模块而忽略其余模块。同时 Spring 还可以很好的和当下主流开发框架进行集成，如 Struts2、 Hibernate、 Mybatis、 JTA等。

Spring 提供了一个 AOP（面向切面编程）框架，许多 OOP 不易实现的功能可以通过 AOP 轻松实现。另外，利用 Spring 提供的 IoC 容器，可以将对象之间的依赖关系交由 Spring 控制，从而避免硬编码造成的紧耦合。

Spring 支持声明式事务管理，通过声明的方式灵活的进行事务管理，使开发者从单调繁琐的事务管理代码中解脱出来。Spring 是低侵入式的，领域逻辑代码不需要依赖 Spring 框架本身，代码污染极低。

本文档是 Spring 框架的参考指南，如果你对本文档有任何要求、意见或者问题，均可发送到 [用户邮件列表](https://groups.google.com/forum/#!forum/spring-framework-contrib)。对于 Spring 框架本身的问题可在 StackOverflow 上提问 (see https://spring.io/questions)。