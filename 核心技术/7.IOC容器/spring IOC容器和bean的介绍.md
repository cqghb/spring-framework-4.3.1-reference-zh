本章讲述了spring框架IOC容器的实现原理，IOC也被称为依赖注入。这是一个使用对象来定义依赖关系的过程，它们与其他对象一起工作，但是只有通过构造函数参数、工厂方法的参数，或者是在方法构造或返回对象实例上设置的属性。容器在创建bean时注入这些依赖项。这个过程是逆向的，因此它的名字叫控制反转(IOC).bean本身通过直接构造类或一种机制来控制其依赖关系的实例化或位置。
    org.springfeamework.beans 和 org.springframework.context两个包是spring框架的IOC容器的基础包。BeanFactory接口提供了一个可以管理任何类型的对象的高级配置机制。ApplicationContext是BeanFactory的子接口。它更容易与spring的AOP功能集成；消息资源处理(用于国际化)、事件发布；应用层的具体语言环境，如用于web应用的WebApplicationContext。
    总之，BeanFactory提供配置框架和基本功能，并增加了更多的企业应用的特定功能。ApplicationContext完整的扩展了BeanFactory，是专门用于在本章描述的spring的IOC容器。关于使用BeanFactory而不使用ApplicationContext的更多信息，请参考7.16节的BeanFactory。
    在spring中，构成应用程序主干并有spring IOC容器管理的对象称为bean。bean时一个被spring IOC容器实例化、集成和管理的对象。另外bean只是应用程序中许多对象中的一个。bean之间的依赖关系通过容器中使用的配置元数据反映出来。
