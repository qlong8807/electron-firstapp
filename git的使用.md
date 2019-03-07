# git 命令
## 配置用户和邮箱
git config --global user.name "newname"

git config --global user.email "newemail"
## 初始化
git init
## 查看状态
git status
## 添加文件，可多次执行
git add .
## 提交到本地
git commit -m 'a comments'
## 查看提交日志
git log
## 撤销/回滚
git reset --hard af9d9g9ess //只需输入log中看到的版本号前8位即可
## 查看每一次操作git的记录（回滚后查看曾经的最新）
git reflog
## 关联到服务器
git remote add origin https://github.com/*
## 推送
git push -u origin master
## 拉取
git pull
## 对比工作区和版本库最新版本
git diff -- HEAD src/com/breakyizhan/git/HelloGIT.java
## 撤销修改
git checkout -- src/com/breakyizhan/git/HelloGIT.java //撤销对HelloGIT.java的修改

git checkout . //撤销所有文件的修改

## 分支
### 创建分支
git branch dev
### 切换分支
git checkout dev
### 删除分支
git branch -d dev
### 合并分支
git checkout master

git merge dev//在master保留dev分支信息

git merge --no-ff -m "dev merge master with no-ff" dev//在master会生成一个新的commit，在dev保留分支信息

## 暂存区
### 暂存代码
git add .

git stash
### 查看暂存区
git stash list
### 恢复并删除暂存
git stash pop

##查看提交次数
git log --oneline| wc -l
