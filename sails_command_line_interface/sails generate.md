###sails generate
sails generate可以帮助我们自动生成项目相关内容

    1. sails generate new <appName>  
       生成名为appName的项目，其实"sails new <appName>" 使用的就是这个

    2. sails generate api <foo>
       生成api/models/Foo.js、api/controller/FooController.js

    3. sails generate model <foo> [attribute1:type1, attribute2:type2 ... ]
       生成api/models/Foo.js，attribute是可选参数

    4. sails generate controller <foo> [action1, action2, ...]
       生成api/controller/FooController.js，action是可选参数

    5. sails generate adapter <foo>
       创建api/adapter/foo文件夹，包含创建一个adapter需要的资源，用于自定义adapter

    6. sails generate generator <foo>
       创建foo文件夹，包含一个generator需要的资源，用于自定义生成器


####例子
生成默认UserController和User

    sails generate api user
成功运行后，会生成api/models/User.js和api/controller/UserController.js两个文件