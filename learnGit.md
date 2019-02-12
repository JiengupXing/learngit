#什么是Git
Git是一个分布式版本控制系统，由Linux的创始人Linus为Linux开源社区创建，是一个开源免费的分布式版本控制系统。

#创建Git版本库

	git init
	
把目录变成本地仓库(repository)

#添加和文件到本地git仓库
##查看本地库状态
	git status
##添加文件到变更区
	git add <filename>
	
##提交变更申请
	git commit -m "notes"
	
#管理本地文件变更

##查看变更记录信息
	git log
	//--pretty=oneline to slim the imformation
##查看历史操作记录
	git relog 
	//可以用来返回到任意历史版本
##回退到历史版本
	git reset --hard HEAD^
	//HEAD^ to last HEAD^^ to last'last HEAD~NUM to the former NUMth 
##回退到指定版本
	git reset --hard "commit key"

#撤销修改或删除文件

##撤销修改
	git checkout -- <flie>
	//回到最近一次commit 或者 add 时的状态

##撤销缓存区中的修改
	git reset HEAD <file>
	//回退到该文件到add步骤

##确认删除文件
	git rm
	git commit
##恢复删除文件
	git checkout <file>
#创建与合并分支
##创建分支
	git checkout -b "branchname"
	//-b表示创建并切换
#查看分支
	git branch
#切换分支
	git checkout “branchname”
#合并分支
	git merge “branchname”
#删除分支 
	git branch -d “branchname“
#强制删除分支
	git branch -D “branchname”
#查看分支合并的情况
	git log、
#禁用fast forward以保存分支信息
	git merge --no-ff -m "massage"
#临时保存工作现场
	git stash
#查看保存的工作现场
	git stash list
#恢复stash内容
	git stash apply
#删除stash内容
	git stash drop
	//git stash apply + git stash drop = git stash pop
#查看远程库的信息
	git remote
