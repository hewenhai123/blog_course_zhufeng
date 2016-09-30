### 安装 Express
express 是 Node.js 上最流行的 Web 开发框架，正如他的名字一样，使用它我们可以快速的开发一个 Web 应用。我们用 express 来搭建我们的博客，打开命令行，输入:
```
$ npm install -g express-generator
```
安装 express 命令行工具，使用它我们可以初始化一个 express 项目

![image](/express.png)

----

### 生成一个项目
在命令行中输入：
```
$ express -e zhufengpeixunblog
$ cd zhufengpeixunblog && npm install
```
执行结果中会显示生成的文件并提示后续的命令

```
E:\>express -e zhufengpeixunblog

   create : zhufengpeixunblog
   create : zhufengpeixunblog/package.json
   create : zhufengpeixunblog/app.js
   create : zhufengpeixunblog/public
   create : zhufengpeixunblog/routes
   create : zhufengpeixunblog/routes/index.js
   create : zhufengpeixunblog/routes/users.js
   create : zhufengpeixunblog/public/images
   create : zhufengpeixunblog/public/javascripts
   create : zhufengpeixunblog/views
   create : zhufengpeixunblog/views/index.ejs
   create : zhufengpeixunblog/views/error.ejs
   create : zhufengpeixunblog/public/stylesheets
   create : zhufengpeixunblog/public/stylesheets/style.css
   create : zhufengpeixunblog/bin
   create : zhufengpeixunblog/bin/www

   install dependencies:
     > cd zhufengpeixunblog && npm install

   run the app:
     > SET DEBUG=zhufengpeixunblog:* & npm start

```
进入生成的目录并安装依赖
```
E:\>cd zhufengpeixunblog && npm install

debug@2.2.0 node_modules\debug
└── ms@0.7.1

morgan@1.6.1 node_modules\morgan
├── on-headers@1.0.1
├── basic-auth@1.0.3
├── depd@1.0.1
└── on-finished@2.3.0 (ee-first@1.1.1)

cookie-parser@1.3.5 node_modules\cookie-parser
├── cookie@0.1.3
└── cookie-signature@1.0.6

serve-favicon@2.3.0 node_modules\serve-favicon
├── ms@0.7.1
├── etag@1.7.0
├── fresh@0.3.0
└── parseurl@1.3.0

body-parser@1.13.3 node_modules\body-parser
├── bytes@2.1.0
├── content-type@1.0.1
├── depd@1.0.1
├── on-finished@2.3.0 (ee-first@1.1.1)
├── qs@4.0.0
├── iconv-lite@0.4.11
├── http-errors@1.3.1 (statuses@1.2.1, inherits@2.0.1)
├── type-is@1.6.9 (media-typer@0.3.0, mime-types@2.1.7)
└── raw-body@2.1.4 (unpipe@1.0.0, iconv-lite@0.4.12)

express@4.13.3 node_modules\express
├── escape-html@1.0.2
├── array-flatten@1.1.1
├── path-to-regexp@0.1.7
├── merge-descriptors@1.0.0
├── content-type@1.0.1
├── methods@1.1.1
├── utils-merge@1.0.0
├── content-disposition@0.5.0
├── range-parser@1.0.3
├── serve-static@1.10.0
├── vary@1.0.1
├── depd@1.0.1
├── cookie@0.1.3
├── cookie-signature@1.0.6
├── fresh@0.3.0
├── etag@1.7.0
├── on-finished@2.3.0 (ee-first@1.1.1)
├── parseurl@1.3.0
├── qs@4.0.0
├── finalhandler@0.4.0 (unpipe@1.0.0)
├── accepts@1.2.13 (negotiator@0.5.3, mime-types@2.1.7)
├── type-is@1.6.9 (media-typer@0.3.0, mime-types@2.1.7)
├── proxy-addr@1.0.8 (forwarded@0.1.0, ipaddr.js@1.0.1)
└── send@0.13.0 (destroy@1.0.3, ms@0.7.1, statuses@1.2.1, mime@1.3.4, http-errors@1.3.1)

E:\zhufengpeixunblog>

```
设置环境变量并启动服务器,在命令行中执行下列命令
```
SET DEBUG=zhufengpeixunblog:* & npm start
```
执行完成后会显示
```
zhufengpeixunblog:server Listening on port 3000 +0ms
```
在浏览器里访问 http://localhost:3000 就可以显示欢迎页面
```
Express
Welcome to Express
```
刚才我们就用express生成器生成了一个使用ejs模板的示例工程。

---
### 推送至github
创建.gitignore文件。里面内容
```
node_modules
.idea
```
### 提交到本地仓库
- git init 初始化仓库
- git add -A 把所有的文件添加到暂存区
- git commit -m"初始化珠峰博客" 把所有的修改添加到历史区

### 创建远程仓库
- 在github上登陆
- 创建一个新的项目，请特别注意
- 一定不要勾选Initialize this repository with a README 前面的复选框
- 也不要去下拉框里选择 .gitignore 或license
- 要保持默认，直接点击 Create repository

### 推送到远程仓库
- git remote add origin https://github.com/zhufengnodejs/zhufengblog.git 添加远程仓库的关联
- git push -u origin master 把本地的仓库推送到远程服务器上去












