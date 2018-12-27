# Git学习心得
## Git简介
Git是分布式版本控制系统


## Git的安装
* 安装就不多说了
* 配置用户名和邮箱
```
git config —global user.name <username>
git config —global user.email <email@xx.com>
```



## 创建版本库
* 新建仓库(repository)
```
mkdir <reponame>
cd <reponame>
git init
```
当前文件夹就是一个工作区
文件夹中的.git文件就是当前仓库的版本库
版本库又分为暂存区(stage or index)和分支(master)

* 文件的基本操作
工作区文件的状态：
	1. Tracked files  即那些纳入了版本控制的文件
	2. Untracked files  即除tracked files以外的所有其他文件


![](Git%E5%AD%A6%E4%B9%A0%E5%BF%83%E5%BE%97/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202018-12-27%20%E4%B8%8B%E5%8D%881.21.45.png)

```
git add <file>				//添加内容到下一次提交中
git rm <file>					//从暂存区和工作目录中删除文件
git rm -f <file>				//删除之前修改过并放入缓存区-force
git mv <file_from> <file_to>	//移动文件
git commit -m <message>		//提交
git commit -a -m <message>	//跳过使用暂存区直接提交

//谨慎使用以下3条命令
git checkout -- <file>		//丢弃工作区的修改
git reset HEAD <file>			//丢弃暂存区的修改
git reset --hard <commit id>	//回退版本
```

* Git的其他功能
```
git status
git status -s
git diff <file>				//工作区和暂存区文件的区别
git diff --cached <file>		//暂存区和分支文件的区别
git diff --staged <file>		//同上
git diff HEAD <file>			//工作区和分支文件的区别
git log						//当前commit的历史操作
git reflog					//所有commit历史操作的记录
```


## 远程仓库Github
* 基本命令
```
git remote add origin git@github.com:xxxxxx/repo-name.git
//添加后远程库的名字就是origin
git push -u origin master
git push origin master
git clone git@github.com:xxxxxx/repo-name.git
```


## Git分支管理
```
git checkout -b <branch>			//创建并切换分支
git branch						//产看分支
git checkout <branch>				//切换分支
git merge <branch>				//合并分支(Fast-forward)
git branch -d <branch>			//删除分支

```









