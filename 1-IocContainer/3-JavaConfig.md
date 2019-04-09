Java Config 的写法类似于这样

``` java
@Configuration
public class AppConfig {
    @Bean
    public Panda getPanda(){
        Panda panda =  new Panda();
        panda.setName("LeLe");
        return panda;
    }
}
```

- @Configuration:

  表明这是一个配置类

- @Bean

  标注在方法上，表明这个方法的返回值是一个bean，交给IOC容器来管理。

上面的写法类似于

```xml
<beans>
    <bean id="panda" class="zoo.animal.Panda" >
        <property name="name" value="LeLe" />
    </bean>
</beans>
```

