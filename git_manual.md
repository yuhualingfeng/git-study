## Git命令
### git config
此命令用于查看或修改配置信息

```git
git congfig --global user.name "puhuasheng"

```
1 配置用户参数
	git config --global user.name "John Doe"
	git config --global user.email "1135317965.qq.com"
	git config --global core.editor emacs
	git config --global merge.tool vimdiff
	git config --global credential.helper store   // 保存用户名和密码
2 查看配置参数
	git config --list
	git config user.name

3查看某条命令的帮助信息
	git help <verb>
	git <verb> --help
	example:git help config

4将README文件添加到版本控制	
	git add README
5将所有
git add .


git commit -m "initial project version"

git clone git://github.com/schacon/grit.git

git diff
git diff --cached

git commit -a -m 'initial project version'


git rm readme.md
git rm --cached readme.md

#文件移动(重命名)
git mv README.md README

#更新远程代码(method 1)
git remote -v
git fetch origin master
git log -p master.. origin/master
git merge origin/master

#更新远程代码(method 1)
git fetch origin master:temp
git diff temp
git merge temp
git branch -d temp


#查看提交历史
git log
git log -p -2
git log --pretty=oneline
git log --pretty=format:"%h - %an, %ar : %s"
git log --since=2.weeks

#修改最后一次提交
git commit -m 'initial commit'
git add forgotten_file
git commit -amend

#取消已暂存的文件
git reset HEAD benchmarks.rb

#取消对文件的修改
git checkout -- benchmarks.rb

git remote
git remote -v

git push origin master
git remote show origin
git pull 
git remote rename pb paul
git remote rm paul

#标签
git tag
git tag -l 'v1.4.2.*'
git tag -a v1.4 -m 'my version 1.4'
git show v1.4
git push origin v1.0.0
git push origin --tags

git config --global alias.st status
git config --global alias.ci commit
git config --global alias.last 'log -1 HEAD'

#使用HTTPS协议clone的情况下保存用户名和密码
git config --global credential.helper wincred


#远程分支
git fetch origin
git remote add teamone
git fetch teamone
git push origin serverfix
git push origin serverfix:serverfix
git push origin serverfix:awesomebranch

git merge origin/serverfix
git checkout -b serverfix origin/serverfix
git push origin :serverdix



#分支
git fetch origin 同步远程服务器上的数据到本地
git push origin serverfix  推送到远程仓库
git push origin :serverfix 删除远程分支（非常无厘头）

git checkout -b iss53 origin/master 从远程分支直接分化一个本地分支
git push 
git pull 

git fetch origin master  同步远程仓库
git fetch origin master:temp 同步远程的master分支到新建的temp分支
git merge origin/master 合并master分支

#存储用户名和密码
git config --global credential.helper store

















