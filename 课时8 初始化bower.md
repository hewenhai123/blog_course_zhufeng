### 初始化bower
先执行此命令，然后会执行一系列交互问答 bower init
```
E:\zhufengpeixunblog>bower init
? name: zhufengpeixunblog
? version: 0.0.0
? description:
? main file:
? what types of modules does this package expose?
? keywords:
? authors: zhangrenyang-t510 <zhang_renyang@>
? license: MIT
? homepage:
? set currently installed components as dependencies? Yes
? add commonly ignored files to ignore list? Yes
? would you like to mark this package as private which prevents it from being accidentally published to the regis
? would you like to mark this package as private which prevents it from being accidentally published to the regis

{
  name: 'zhufengpeixunblog',
  version: '0.0.0',
  authors: [
    'zhangrenyang-t510 <zhang_renyang@>'
  ],
  license: 'MIT',
  ignore: [
    '**/.*',
    'node_modules',
    'bower_components',
    'test',
    'tests'
  ]
}

? Looks good? Yes
```
执行完此命令后会生成一个 bower.json 文件。

### 创建配置文件 .bowerrc
里面内容如下
```
{"directory":"./public/lib"}
```

这表示以后bower安装的模块都安装在./public/lib下面。

### 安装bootstrap
```
bower install bootstrap --save
```
大家可以看到，不但安装了bootstrap,也安装了依赖的jquery
```
E:\zhufengpeixunblog>bower install bootstrap --save
bower bootstrap#*               cached git://github.com/twbs/bootstrap.git#3.3.5
bower bootstrap#*             validate 3.3.5 against git://github.com/twbs/bootstrap.git#*
bower jquery#>= 1.9.1           cached git://github.com/jquery/jquery.git#2.1.4
bower jquery#>= 1.9.1         validate 2.1.4 against git://github.com/jquery/jquery.git#>= 1.9.1
bower bootstrap#~3.3.5         install bootstrap#3.3.5
bower jquery#>= 1.9.1          install jquery#2.1.4

bootstrap#3.3.5 public\lib\bootstrap
└── jquery#2.1.4

jquery#2.1.4 public\lib\jquery

```












