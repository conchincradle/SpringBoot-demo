# Client 
## application.yml
```yml
server:
  port: 8080
  servlet:
    context-path: /demo
spring:
  application:
    # Spring Boot Admin展示的客户端项目名，不设置，会使用自动生成的随机id
    name: spring-boot-demo-admin-client
  boot:
    admin:
      client:
        # Spring Boot Admin 服务端地址
        url: "http://localhost:8000/"
        instance:
          metadata:
            # 客户端端点信息的安全认证信息
            user.name: ${spring.security.user.name}
            user.password: ${spring.security.user.password}
  security:
    user:
      name: zhu
      password: 123456
management:
  endpoint:
    health:
      # 端点健康情况，默认值"never"，设置为"always"可以显示硬盘使用情况和线程情况
      show-details: always
  endpoints:
    web:
      exposure:
        # 设置端点暴露的哪些内容，默认["health","info"]，设置"*"代表暴露所有可访问的端点
        include: "*"
```
### 登录然后显示client的Index页面

# server

<img src="https://user-images.githubusercontent.com/33627638/209654813-97804b18-d3b1-455e-a741-7b20c3f2d0a8.png" width="600">

<img src="https://user-images.githubusercontent.com/33627638/209655496-43c218a5-2613-4df1-84c9-e558392d70c6.png" width="600">

