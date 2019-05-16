```xml
<!-- 导包-->
<dependency>
          　　<groupId>com.fasterxml.jackson.core</groupId>
          　　<artifactId>jackson-core</artifactId>
          　　<version>2.7.3</version>
      </dependency>

      <dependency>
          <groupId>com.fasterxml.jackson.core</groupId>
          <artifactId>jackson-databind</artifactId>
          <version>2.7.3</version>
      </dependency>
      <dependency>
          <groupId>com.fasterxml.jackson.core</groupId>
          <artifactId>jackson-annotations</artifactId>
          <version>2.7.3</version>
      </dependency>
```

在springmvc.xml中配置

```xml
 <!--映射器 解决ResponseBody报错问题-->
    <bean class="org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping"/>
    <bean class="org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter">
        <property name="messageConverters">
            <list>
                <bean class="org.springframework.http.converter.json.MappingJackson2HttpMessageConverter"/>
            </list>
        </property>
    </bean>
```

