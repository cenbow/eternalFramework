eternalFramework
----
一个基于spring mvc的应用框架，实现基本用户注册及权限控制，可在此框架基础上进行二次开发

# 框架说明
整个框架基于`Spring mvc` + `spring data jpa with hibernate` + `mysql database`。
包结构分的尽量细是为了扩展其他功能，如后期扩展`eternal-api`供移动端调用，可以很简单的依赖`eternal-service`而不用去跟`eternal-web` 耦合，解耦合并提高模块的复用性。

# 关于前端
1. bootstrap 3
2. 引入pjax实现pustState + ajax技术，局部刷新提高访问速度

# 模块简单说明
1. eternal-commons: 公共的jar
2. eternal-springcore: spring核心jar
3. eternal-utils: 自定义的工具类
4. eternal-model: model 实现
5. eternal-dao: dao 实现
6. eternal-service: service实现
7. eternal-mvc: 对mvc framework配置的封装
8. eternal-api: api数据接口实现
9. eternal-web: 前端页面访问实现

# 如何运行
1. maven、jdk1.7+
2. 建立mysql数据库

    ```sql
    create database quickstart default charset utf8
    ```
3. 修改数据库配置

   打开 `eternal-mvc` -> `src` -> `main` -> `resources` -> `db.properties` 修改相关配置
   
4. 进入 `eternalFramework` 根目录

5. 运行命令

    ```bash
    mvn clean compile install
    ```
6. 进入 `eternal-web` 

7. 运行项目
    
    ```bash
    mvn jetty:run
    ```
8. 访问：[http://localhost:8888](http://localhost:8888)

# See
* myblog: [http://wincn.net](http://wincn.net)
* task list: [worktile](https://new.worktile.com/project/07a3eaa6a0ed42e7ab652781e89a0f97/task)