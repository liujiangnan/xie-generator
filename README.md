# xie-generator

楔框架生成器

# 1 概要说明

大者以为舟航柱梁，小者以为楫楔<br>

# 2 使用 
    * 依赖环境：>=nodejs 8.0.0 
    * npm install -g xie-generator
    * x create myXproject
    * cd myXproject && npm start
    * 打开浏览器，输入http://localhost:1337
    
# 3 第一次

1、在 /engine 下新建一个模块(文件夹) example，然后在example里新建 src 和 web 两个文件夹

2、在新建的src文件夹下新建service.js文件，编写内容如下：

```javascript

function service(net){ 
    net.data.message = "hello world!!";
}
module.exports = service;

```

3、在新建的web文件夹下新建index.ejs,编写内容如下：

```

<div id="realData">
    <h1>{{message}}</h1>
</div>

```
 
```

<script> 
    var vue = net.datachange("realData");
</script>

```

4、在根目录打开CMD，输入 node app.js 命令来启动微服务

5、打开浏览器，输入http://localhost:1337/example 查看效果

# 4 更多命令

## x init 

此命令为快速初始化开发框架，用于在某个文件夹内快速添加框架的目录结构与npm包安装

* 新建一个空文件夹
* cmd进入这个文件夹
* 运行命令 x init 
* 生成目录结构

## x add $engine

此命令为快速建立一个模块的目录结构，通过此命令可以快速建立一个模块

* cmd进入项目的engine目录
* 运行命令 x add example
* 重启服务
* 打开浏览器，输入http://localhost:1337/example 查看效果

## x install $engine

此命令为安装npm开源社区提供的开源的楔子模块，它会自动的安装依赖到node_modules，并且把模块拷贝到engine目录下

注意：

1、此命令必须在项目的根目录运行才能正确安装
     
2、楔子模块官网


# 5 更多功能与方法