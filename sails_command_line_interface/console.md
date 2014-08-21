###sails console
通过sails console可以启动sails项目并且进入node REPL模式，意味着可以使用我们自己的models, services, configuration等内容，对于查询项目的配置、通过Waterline查看数据内容很有帮助。

####例子

    cd sails_demo
    sails console
    进入REPL之后，可以通过已有的User模型操作用户对象:
    sails> User.find(console.log)
    null [ { username: 'user',
    password: 'pass',
    createdAt: Thu Aug 21 2014 16:46:41 GMT+0800 (中国标准时间),
    updatedAt: Thu Aug 21 2014 16:46:41 GMT+0800 (中国标准时间),
    id: 1 } ]