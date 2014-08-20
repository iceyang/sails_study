###Models And ORM
sails是一个MVC的框架，这里的Model就是对应MVC中的M -> 实体对象。  
它使用了一个ORM/ODM框架：Waterline，提供数据库的抽象层，用户只需使用sails已经提供的适配器即可。

####总体介绍
1.  model存放位置: api/models，connections存放位置：config/connections  
2.  适配器Adapter  
跟其他MVC框架一样，sails支持多种数据库，不管我们使用哪种数据库：mongodb，mysql，或其他数据库，只要我们安装指定好Adapter，在model层的操作是一样的。
sails提供了许多数据库adapter，比如sails-mongo，提供mongodb的适配器，可以通过下面指令安装

        npm install sails-mongo

3.  数据库连接配置Connections  
Adapter解决了如何操作数据库的问题，Connection则提供了数据库配置，这个配置对象提供了数据库连接时需要的信息，下面是mongodbServer的例子：  

        mongodbServer: {
          adapter: 'sails-mongo',
          host: 'localhost',
          port: 27017,
          user: 'your_username',
          password: 'your_password',
          database: 'your_database'
        }
        其中的adapter属性指定了使用哪个适配器，
当设置好之后，可以通过该对象来引用（这里是mongodbServer），比如在config/env里；在model里面。

#####具体内容请参见model_and_orm里对应的文档。