 1. 创建数据库app_excel，数据库编码为UTF-8
 
 2. 执行db文件下sql，初始化数据
 
 3. 修改application.yml文件的spring.profiles.active为pro,启用环境为正式环境
 ![image](/uploads/575abfd7bd6474712b21f04fa47a6387/image.png)
 4.  修改application-pro.yml，更新MySQL连接和账号以及密码
 ![image](/uploads/b681cb2dc4ec9775554491fe8fad556e/image.png)
 
 5. 启动redis,修改application-pro.yml，更新redis连接配置
 ![image](/uploads/f8874ac4fe597026017d7a32d07d656e/image.png)
 
 6.  修改application-pro.yml，更新eim.excel下的前四个配置信息
![image](/uploads/56b454b2edb062f452c7fa5f5e2b2522/image.png)

 7.  修改resources/static/js/commond.js 文件中baseURL,StrategyInfoURL,developerUrl的值
![image](/uploads/8671b1ea8f1245297ebdd3b9275ab39e/image.png)

