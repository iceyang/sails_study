###new
通过  

    sails new <appName>
可以创建一个名为appName的sails项目，该命令有下面几种参数：

    1) --no-linker
       关闭view、静态html与asset之间的自动链接（相关的grunt任务不会创建）
    2) --no-frontend
       关闭生成assets文件夹和对应文件
    3) --template=[template language]
       指定使用的模版语言，比如ejs、jade，sails默认为ejs

####例子
创建名为sails_demo的项目，同时指定模版语言为jade。

    sails new sails_demo --template=jade
执行成功后就会得到一个新的sails项目。
当使用jade为模版引擎时，需要通过"npm install jade --save"安装jade，否则将找不到jade module
