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