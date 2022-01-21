## 一、软件架构

> 1、`SpringBoot 2.2.8` + `JPA（暂定）` 核心框架
>
> 2、前后端分离模式：`Shrio` + `JWT`无状态鉴权认证机制

 ## 二、工程结构说明

### 		1、`pom`继承关系

```
adhere
    |--------adhere-core
                |--------adhere-system
                            |--------adhere-api
                           
```

### 	2、`module`说明

> 1、`adhere` 父工程`pom`，主要用于工程jar包版本统一管理
>
> 2、`adhere-core` 核心工程，主要包含`Base`类、工具类、平台`banner`
>
> 3、`adhere-system` 平台后台管理代码（前后端未分离），包含工程配置类
>
> 4、`adhere-api` 平台后台管理代码（前后端分离），新项目可以直接继承`ecpp-api` 开发

## 三、工程配置文件说明

> 1、`application-*.yml` 工程配置文件，数据源、日志在此文件进行配置
>
> 2、`application.yml` 工程配置文件注册入口，`spring.profiles.action` 用于选择使用哪个工程配置文件
>
> 3、`application.properties` 工程环境变量文件
后期加入
## 四、Swagger配置说明

> 1、开启和关闭`Swagger`配置：`application-*.yml`中的`swagger.enable`属性`true-开启`，`false-关闭`
>
> 2、`Swagger`访问路径：`http://ip+port/docs.html`
>
> 3、`Swagger`最佳实践：实体：`Dict` ；controller：`DictController`

