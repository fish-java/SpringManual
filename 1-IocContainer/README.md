## 如何理解Spring beans容器

Spring最核心的思想就是实现了 控制反转（高层模块不依赖于底层模块）的设计原则。

说白了，就是一个对象A依赖的其他对象不应该在A的方法调用中创建，而是应该在其他地方创建。然后通过

- 构造函数
- Setter方法
- 或者工厂方法

的传参来传递给对象A。



 `org.springframework.beans` 和 `org.springframework.context` 这两个包是Spring实现IOC容器的基础。



![container-magic](assets/container-magic.png)

对于被依赖的底层对象，统统交由Ioc容器来管理。然后我们通过配置文件而不是硬编码的方式来创建我们需要的对象。使得我们的高层模块直接获取自己需要的bean，达到低耦合的效果。



Configuration Metadata 有三种写法

- XML配置文件
- 注解
- Java-based configuration
