first git
??
添加远程仓库：
1、ssh-keygen -t rsa -C "youremail@example.com" 使用git-bash生成公钥
2、github配置公钥
3、github创建仓库
4、本地仓库执行git remote add origin git@github.com:xiaoming12/learngit.git
5、本地代码push到远程仓库 git push -u origin master
6、git push origin master推送最新修改