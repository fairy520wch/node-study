# node-study
node study record
Node.js是什么？
这里我们可以简单理解Node.js是一个内置有chrome V8引擎的JavaScript运行环境，他可以使原本在浏览器中运行的JavaScript有能力跑后端，从而操作我们数据库，进行文件读写等。

目前市面上高密集的I/O模型，比如 Web 开发，微服务，前端构建等都有做Node.js的身影。不少大型网站都是使用 Node.js 作为后台开发语言的，比如 淘宝 双十一、去哪儿网 的 PC 端核心业务等。另外我们一些前端工具譬如VSCode,webpack等也是有Node.js开发。

Node.js的包管理工具，npm已经成为世界开源包管理中最大的生态，功能强大，目前单月使用者接近1000万。

Node.js特点（记住三句话）
事件驱动
非阻塞IO模型（异步）
轻量和高效

Node.js使得JavaScript可以脱离浏览器的窗口，独立运行在Node.js提供的环境中，所以Node.js中没有BOM，DOM这些概念。Node.js中根本没有页面，主要是进行一些服务器上的操作（比如：读写文件，网络通信...）。我们只需要基本的JavaScript语法基础（ES6）即可学习。

Node.js采用的是CommonJs规范，在NodeJS中，一般将代码合理拆分到不同的JS文件中，每一个文件就是一个模块，而文件路径就是模块名。 在编写每个模块时，都有require、exports、module三个预先定义好的变量可供使用。

Node.js中模块的分类：

核心模块（已经封装好的内置模块）；
自己定义的模块；
第三方的模块（npm下载下来的）；

Node.js中module.exports和exports的区别
Node中每个模块都有一个module对象，module对象中的有一个exports属性为一个接口对象，我们需要把模块之间公共的方法或属性挂载在这个接口对象中，方便其他的模块使用这些公共的方法或属性。

Node中每个模块的最后，都会return: module.exports。

Node中每个模块都会把module.exports指向的对象赋值给一个变量exports，也就是说：exports = module.exports。

module.exports = XXX，表示当前模块导出一个单一成员，结果就是XXX。

如果需要导出多个成员时必须使用exports.add = XXX; exports.foo = XXX;或者使用module.exports.add = XXX; module.export.foo = XXX;。

npm常见命令
npm -v ：查看npm版本。

npm init：初始化后会出现一个package.json配置文件。可以在后面加上-y ，快速跳过问答式界面。

npm install ：会根据项目中的package.json文件自动下载项目所需的全部依赖。

npm install 包名 --save-dev(npm install 包名 -D)：安装的包只用于开发环境，不用于生产环境，会出现在package.json文件中的devDependencies属性中。

npm install 包名 --save(npm install 包名 -S)：安装的包需要发布到生产环境的，会出现在package.json文件中的dependencies属性中。

npm list：查看当前目录下已安装的node包。

npm list -g：查看全局已经安装过的node包。

npm --help：查看npm帮助命令。

npm update 包名：更新指定包。

npm uninstall 包名：卸载指定包。

npm config list ：查看配置信息。

npm 指定命令 --help ：查看指定命令的帮助。

npm info 指定包名：查看远程npm上指定包的所有版本信息。

npm config set registry https://registry.npm.taobao.org： 修改包下载源，此例修改为了淘宝镜像。

npm root：查看当前包的安装路径。

npm root -g：查看全局的包的安装路径。

npm ls 包名：查看本地安装的指定包及版本信息，没有显示empty。

npm ls 包名 -g：查看全局安装的指定包及版本信息，没有显示empty。
