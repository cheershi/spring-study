# spring学习笔记(一)

## Spring Ioc 容器

Spring 容器是Spring框架的核心。Spring容器将创建Bean对象实例,把它们联系在一起，配置它们，并管理它们整个生命周期从创建到销毁。Spring 容器通过依赖注入(DI)将它们组成一个应用程序组件。这些bean对象我们称为Spring beans。

 1.BeanFactory容器

官网API：The BeanFactory interface provides an advanced configuration mechanism capable of managing any type of object。

   翻译：BeanFactory接口提供一个高效配置机制可以管理任何类型的对象

2.ApplicationContext容器

   官网API: ApplicationContext is a sub-interface of BeanFactory. It adds easier integration with Spring’s AOP features; message resource handling (for    use in internationalization), event publication; and application-layer specific contexts such as the WebApplicationContext for use in web applications。

   翻译：ApplicationContext接口是BeanFactory接口的子接口，增加更容易集成Spring的AOP功能；信息资源处理(用于国际化),事件发布;和应用程序层特定上下文如WebApplicationContext用于web应用程序。
   
 基于xml元数据配置Spring Ioc容器实现代码示例：
 
    //创建一个ApplicationContext容器
        applicationContext = new ClassPathXmlApplicationContext(new String[]{"test1-service.xml"});
