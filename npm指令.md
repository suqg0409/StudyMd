#npm,vue各种指令介绍  
---
#### npm install -g gulp
全局安装模块
#### npm install gulp
安装模块
#### npm install gulp --save 或 npm install gulp -S
-S, --save 安装模块信息将加入到dependencies（生产阶段的依赖）
#### npm install gulp --save-dev 或 npm install gulp -D
-D, --save-dev 安装模块信息将加入到devDependencies（开发阶段的依赖），所以开发阶段一般使用它  
#### npm install gulp --save-optional 或 npm install gulp -O
-O, --save-optional 安装模块信息将加入到optionalDependencies（可选阶段的依赖）
#### npm install gulp --save-exact 或 npm install gulp -E
-E, --save-exact 精确安装指定模块版本
#### npm uninstall gulp
卸载模块，后缀语法与安装后缀语法一样
#### npm update gulp
更新模块
#### npm outdated
检查过时模块
#### npm ls
查看安装的模块
#### npm ls -g
查看全局安装的模块
#### npm init
在项目中引导创建一个package.json文件
#### npm help
查看某条命令的详细帮助 
#### npm root
查看包的安装路径  
#### npm config
管理npm的配置路径
#### npm cache
管理模块的缓存  
#### npm cache clean
清除npm本地缓存  
#### npm run 命令名
启动模块，在package.json文件scripts中执行相应的命令名
#### npm start
启动模块，该命令写在package.json文件scripts的start字段中，npm start会执行scripts里的start字段。 如果没有start字段则执行node server.js
#### npm stop
停止模块
#### npm restart
重新启动模块
#### npm test
测试模块，该命令写在package.json文件scripts的test字段中，可以自定义该命令来执行一些操作
#### npm version
查看模块版本  
#### npm view
查看模块的注册信息
#### npm view gulp dependencies
查看模块的依赖关系
#### npm view gulp repository.url
查看模块的源文件地址
#### npm view npm contributors
查看模块的贡献者，包含邮箱地址
#### npm adduser
登录npm
#### npm publish
发布npm模块
#### npm access
在发布的包上设置访问级别
#### npm root
查看包的安装路径
#### npm root
查看包的安装路径

---
> #### package.json 配置文件  
> 1. script: 配置npm run启动项的指令
> 2. dependencies: 生产环境依赖（如jquery）
> 3. devDependencies: 开发环境依赖（如vue-cli，webpack等不需要在生产环境中的模块）
> 4. engines: 引擎（npm node）
> 5. browserslist: 市场份额，与支持浏览器  
> 6. name与version: npm的标识符，代表模块的名字版本
> 7. description: 放简介，字符串，方便在npm search中搜索
> 8. keywords: 关键字，数组、字符串，方便在npm search中搜索
> 9. bugs: 你项目的提交问题的url和（或）邮件地址  
> 10. repository: 指定你的代码存放的地方。这个对希望贡献的人有帮助。如果git仓库在github上，那么npm docs命令能找到你。
> 11. scripts: “scripts”是一个由脚本命令组成的hash对象，他们在包不同的生命周期中被执行。key是生命周期事件，value是要运行的命令。
> 12. config: "config" hash可以用来配置用于包脚本中的跨版本参数