## npm简介
    NPM是随同NodeJS一起安装的包管理工具，安装NodeJs即可安装NPM。
## 查看版本号
    npm -v
## 使用淘宝 NPM 镜像
    npm install -g cnpm --registry=https://registry.npm.taobao.org
## 升级
    sudo npm install npm -g
## 本地安装模块
    * 将安装包放在 ./node_modules 下（运行 npm 命令时所在的目录）
    * 可以通过 require() 来引入本地安装的包
    npm install <Module Name>
### 开发 OR 生产
    把模块信息保存到package.json文件中；
    devDependencies是只会在开发环境下依赖的模块；
    dependencies依赖的包不仅开发环境能使用，生产环境也能使用；
    --save
    --save-dev
>> 例如：webpack，gulp等打包工具，这些都是我们开发阶段使用的，代码提交线上时，不需要这些工具，所以我们将它放入devDependencies即可，但是像jquery这类插件库，如果我们不把他打入线上代码中，那么项目就可能报错，无法运行，所以类似这种项目必须依赖的插件库，我们则必须打入dependencies中.
## 全局安装模块
    * 将安装包放在 /usr/local 下或者你 node 的安装目录。
    * 可以直接在命令行里使用。
    npm install express -g

> 如果你希望具备两者功能，则需要在两个地方安装它或使用 npm link。

## 查看所有全局安装的模块
    npm list -g
## 查看某个模块的版本号
    npm list grunt
## 卸载模块
    npm uninstall express
## 更新模块
    npm update express
## 搜索模块
    npm search express
## 清空NPM本地缓存
    npm cache clear
## **创建模块**
    `npm init`

## 注册用户 && 发布
    npm adduser
    npm publish
## 版本号
版本号分为X.Y.Z三位，分别代表主版本号、次版本号和补丁版本号。
    如果只是修复bug，需要更新Z位。
    如果是新增了功能，但是向下兼容，需要更新Y位。
    如果有大变动，向下不兼容，需要更新X位。