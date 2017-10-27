first git
??
添加远程仓库：
1、ssh-keygen -t rsa -C "youremail@example.com" 使用git-bash生成公钥
2、github配置公钥
3、github创建仓库
4、本地仓库执行git remote add study git@github.com:xiaoming3/study.git
5、本地代码push到远程仓库 git push -u origin master
6、git push origin master推送最新修改
注意：最新修改也是需要先commit到本地库然后再push

git checkout -- filename 将会把文件回复更改到最近一次add或者commit的版本
git reset HEAD filename 可以把add到暂存区的版本回退，HEAD可以为其他版本号
	然后使用git checkout -- filename则可撤销修改
	
【git reset 版本号】 和 【git reset --hard 版本号】的区别：
	git reset version 时会获取到目标版本的文件，回到的状态是未add状态，
		使用git checkout -- filename可以将目标版本的文件覆盖到本地
		而在该状态下使用get add添加的是本地版本
	git reset --hard version会直接回退目标版本
	
克隆远程仓库到本地
	git clone git@github.com:xiaoming3/SmartPortables.git
该命令默认会在当前目录下建立仓库
也可以指定目录git clone xxx.git "指定目录"
clone时创建新的分支替代默认Origin HEAD（master）
	git clone -b [new_branch_name]  xxx.git
clone 远程分支
	git clone 命令默认的只会建立master分支，如果你想clone指定的某一远程分支(如：dev)的话，可以如下：
		A. 查看所有分支(包括隐藏的)  git branch -a 显示所有分支
		B.  在本地新建同名的("dev")分支，并切换到该分支
			git checkout -t origin/dev 该命令等同于：
			git checkout -b dev origin/dev		
			
拉取远程代码，运行不同库合并			
git pull SmartPortables master --allow-unrelated-histories
