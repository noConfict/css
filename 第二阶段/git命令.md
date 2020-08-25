GIT:是目前最先进的分布式版本控制系统（没有之一）

作用：团队协作时，合并代码

如果git是未知的命令   添加环境变量
我的电脑鼠标单击右键属性>高级系统设置单击>环境变量>系统变量（s）>path单击>添加路径

```
设置你的用户名
git  --version	

	查看版本
git config --global user.name "你的姓名"
设置邮箱
git config --global user.email "你的邮箱地址"
git config --list 	显示
git init	初始化仓库
git add 文件名	提交单个
git status	查看当前git状态
git add .		提交所有
git commit -m 第一次提交		第几次版本
git log 	查看当前版本，以及之前所有版本！！！
git reflog   	查看所有版本
git reset --hard "版本ID"		代码回滚到之前某一个版本
git checkout -- 文件名称	从暂存区恢复记录
git remote add origin "远程仓库路径"
git push -u origin master		推送到远程仓库
git clone "远程仓库地址"		克隆远程仓库到本地

更改凭据
我的电脑右键属性>右上角搜索控制输入"凭据"回车>管理Windows凭据>普通凭据


```




