###Getting-started

sails目前稳定版本：0.10.2

1.  安装  

        npm install -g sails@0.10.2

2.  使用sails命令行创建新项目  

        sails new testProject  
成功创建完新项目后，项目结构如下：  

        project
        |---api
        |    |---controllers  //MVC -> C
        |    |---models       //MVC -> M
        |    |---policies     //权限控制
        |    |---responses    //api/responses里面存放的东西可以作为res的方法调用。badRequest的话就是res.badRequest()
        |    |---services     //业务逻辑
        |---assets            //资源文件，比如images, css, js
        |---config            //存放配置文件
        |    |---env          //环境配置，production/development
        |    |---locales      //存放国际化资源文件
        |    |---blueprints   //url类型设置如：restful;一些Model限制的配置，比如limit30配置模型find只能查询30条
        |    |---bootstrap
        |    |---connection   //adpter配置
        |    |---cors         //配置允许使用的HTTP方法
        |    |---csrf         //csrf防御配置
        |    |---globals      //全局对象，比如async,在代码中可以直接使用，而无需重新声明
        |    |---http         //HTTP请求的配置, 配置中间件，中间件顺序，自定义中间件
        |    |---i18n         //国际化配置
        |    |---local        //本地配置文件,它将覆盖config/env里面的配置,使用git作为版本控制工具时，这个文件不会被提交
        |    |---log          //配置log级别
        |    |---models       //配置Model默认的connection, migrate(Model的数据迁移策略), schema等等
        |    |---policies     //policies在controllers之前执行，这里可以配置对那些Controller，具体那些方法进行拦截
        |    |---routes       //配置路由，map URLS to views and controllers
        |    |---session      //配置session，cookie保存时间，缓存adapter
        |    |---views        //配置视图相关内容，比如模版引擎
        |---tasks             //自动任务
        |---views             //MVC -> V

3.  运行刚创建的项目  

        cd testProject
        sails lift
运行成功后，访问http://localhost:1337/，就能看到默认首页。  