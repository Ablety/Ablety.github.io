# SpringCloud-zuul

## 相关依赖
```groovy
implementation 'org.springframework.cloud:spring-cloud-starter-config'
implementation 'org.springframework.cloud:spring-cloud-starter-netflix-eureka-client'
implementation 'org.springframework.cloud:spring-cloud-starter-netflix-zuul'
```

## yml配置
```yaml
eureka:
  client:
    service-url:
      defaultZone: http://cloud1.com:16001/eureka, http://cloud2.com:16002/eureka, http://cloud3.com:16003/eureka,  #服务中心注册地址
  instance:
    instance-id: gateway.com #服务别名
    prefer-ip-address: true #显示ip
```
## 启动类配置
@EnableZuulProxy