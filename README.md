* 安装node.js
* 安装淘宝的cnpm

    npm install -g cnpm --registry=https://registry.npm.taobao.org
* 安装electron && electron-packager

    cnpm install -g electron
    cnpm install -g electron-packager
* 写完代码先install
    npm install
* 启动程序
    npm start
* 打包命令
    npm run-script packageWin
    npm run-script packageDarwin
    npm run-script packageLinux
    npm run-script package
    打包命令中一定要有`--ignore=node_modules`,否则打包不能成功；
    **命令行打包参数**：
        electron-packager <location of project> <name of project> <platform> <architecture> <electron version> <optional options>
        参数说明： 
            * location of project：项目所在路径 
            * name of project：打包的项目名字 
            * platform：确定了你要构建哪个平台的应用（Windows、Mac 还是 Linux） 
            * architecture：决定了使用 x86 还是 x64 还是两个架构都用 
            * electron version：electron 的版本 
            * optional options：可选选项


git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/qlong8807/electron-firstapp.git
git push -u origin master
