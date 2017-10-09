## 简介
- 在企业内部，Excel为常用的办公工具，记录各种各种各样数据，其中以员工相关数据颇多， 以本公司为例，员工年假、参加的培训、成绩、入职时间、等级等信息记录。 对员工来说不透明，员工无法快速查询，一对一的咨询效率低下； 希望通过员工自助查询，通过企信为载体进行交互，输入特定关键字，返回对应信息， 例如输入“CXSYNJ”及返回员工的剩余年假
- 不限定Excel模板下，通过添加项指定读取Excel及读取规则，确定后加装到缓存，用户通过关键字定位到项，返回规则指定的内容。
<br> 
 
## 项目特点
- 友好的代码结构及注释，便于阅读及二次开发
- 实现前后端分离，通过token进行数据交互，前端再也不用关注后端技术
- 灵活的权限控制，可控制到页面或按钮，满足绝大部分的权限需求
- 页面交互使用Vue2.x，极大的提高了开发效率
- 引入quartz定时任务，可动态完成任务的添加、修改、删除、暂停、恢复及日志查看等功能
- 引入API模板，根据token作为登录令牌，极大的方便了APP接口开发
- 引入Hibernate Validator校验框架，轻松实现后端校验
- 引入swagger文档支持，方便编写API接口文档
- 引入路由机制，刷新页面会停留在当前页
<br> 

## 项目结构
```
app_excel
├─db  项目SQL语句
├─war  war包
├─common 公共模块
│  ├─aspect 系统日志
│  ├─exception 异常处理
│  ├─validator 后台校验
│  └─xss XSS过滤
│  
├─config 配置信息
│ 
├─modules 功能模块
│  ├─api API接口模块(APP调用)
│  ├─job 定时任务模块
│  ├─oss 文件服务模块
│  ├─excel 查询助手模块
│  └─sys 权限模块
│ 
├─poi excel导入封装
│ 
├─AppExcelApplication 项目启动类
│  
├──resources 
│  ├─mapper SQL对应的XML文件
│  ├─static 第三方库、插件等静态资源
│  └─views  项目静态页面

```
<br> 



## 技术选型
- 核心框架：Spring Boot 1.5
- 安全框架：Apache Shiro 1.3
- 视图框架：Spring MVC 4.3
- 持久层框架：MyBatis 3.3
- 定时器：Quartz 2.3
- 数据库连接池：Druid 1.0
- 日志管理：SLF4J 1.7、Log4j
- 页面交互：Vue2.x 
<br> 


## 本地部署 
 
- 安装依赖包
- 创建数据库app_excel，数据库编码为UTF-8
- 执行db文件下sql，初始化数据
- 启动redis 
- 修改application-dev.yml，更新MySQL账号和密码
- 修改application-dev.yml，更新redis连接配置
- 修改application-dev.yml，更新eim.excel 下 的 的配置 
- Eclipse、IDEA运行AppExcelApplication.java，则可启动项目
- 项目访问路径：http://localhost
- 账号密码：admin/admin
- Swagger路径：http://localhost/swagger/index.html


## 代码托管

> **[Github](http://10.10.15.98/wangjiafang/app_excel_v2)**

## 参与贡献

欢迎各路好汉一起来参与完善`app_excel`，我们期待你的PR！

- 贡献代码：代码地址 [app_excel](http://10.10.15.98/wangjiafang/app_excel_v2) ，欢迎提交 Issue 或者 Pull Requests
- 维护文档：文档地址 [app_excel-Doc](https://github.com/wangjiafang/docsify) ，欢迎参与翻译和修订
