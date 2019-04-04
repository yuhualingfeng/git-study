## 配置用户参数
```sh
	git config --global user.name "John Doe"
	git config --global user.email "1135317965.qq.com"
	git config --global core.editor emacs
	git config --global merge.tool vimdiff
	git config --global credential.helper store   // 保存用户名和密码
```

## 查看配置参数
```sh
	git config --list
	git config user.name
```

## 查看某条命令的帮助信息
```sh
	git help <verb>
	git <verb> --help
	example:git help config
```

## 将README文件添加到版本控制	
```sh
	git add README
```

# 文件移动(重命名)
```sh
git mv README.md README
```

# 更新远程代码(method 1)
```sh
git remote -v
git fetch origin master
git log -p master.. origin/master
git merge origin/master
```

## 更新远程代码(method 1)
```sh
git fetch origin master:temp
git diff temp
git merge temp
git branch -d temp
```


## 查看提交历史
```sh
git log
git log -p -2
git log --pretty=oneline
git log --pretty=format:"%h - %an, %ar : %s"
git log --since=2.weeks
```

## 查看单个文件提交历史
```sh
gitk --follow filename
```

## 修改最后一次提交
```
git commit -m 'initial commit'
git add forgotten_file
git commit -amend
```

## 取消已暂存的文件
```sh
git reset HEAD benchmarks.rb
```

## 取消对文件的修改
```sh
git checkout -- benchmarks.rb

git remote
git remote -v

git push origin master
git remote show origin
git pull 
git remote rename pb paul
git remote rm paul
```

## 标签
```sh
git tag
git tag -l 'v1.4.2.*'
git tag -a v1.4 -m 'my version 1.4'
git show v1.4
git push origin v1.0.0
git push origin --tags

git config --global alias.st status
git config --global alias.ci commit
git config --global alias.last 'log -1 HEAD'
```

## 使用HTTPS协议clone的情况下保存用户名和密码
```sh
git config --global credential.helper wincred
```


## 远程分支
```sh
git fetch origin
git remote add teamone
git fetch teamone
git push origin serverfix
git push origin serverfix:serverfix
git push origin serverfix:awesomebranch

git merge origin/serverfix
git checkout -b serverfix origin/serverfix
git push origin :serverdix
```



## 分支
```sh
git fetch origin 同步远程服务器上的数据到本地
git push origin serverfix  推送到远程仓库
git push origin :serverfix 删除远程分支（非常无厘头）
git branch -d serverfix 删除本地分支

git checkout -b iss53 origin/master 从远程分支直接分化一个本地分支
git push origin iss53
git pull 

git fetch origin master  同步远程仓库
git fetch origin master:temp 同步远程的master分支到新建的temp分支
git merge origin/master 合并master分支
```

## 存储用户名和密码
```sh
git config --global credential.helper store
```
## 回滚到指定版本
```sh
git reset --hard 'commit_id'
git push origin master --force
```
















