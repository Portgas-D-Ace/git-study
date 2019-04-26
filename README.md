git 的三层结构

	working directory	----- 工作区
	staging index		----- 暂存区
	git directory		----- 版本库
	

git 文件的四种状态

	untracked   ----- 未被管理追踪的
	modified	----- 已修改、未提交到暂存区的
	staged		----- 已提交到暂存区、未提交到版本库的
	committed 	----- 已提交到版本库的


git 常用命令

	git status  			----- 打印当前文件状态
	git log					----- 打印提交版本日志
	git add  'fileName'	or .----- 将已修改的指定(所有)文件提交到暂存区 
	git commit -m			----- 将暂存区的文件提交的版本库
	git commit -am			----- 将已修改的文件直接提交到版本库
	git commit --amend 		----- 撤销上一次提交的版本并将暂存区文件提交到版本库，亦可以用来修改提交说明
	git checkout -- fileName----- 拉取暂存区指定(所有)文件替换工作区的文件 (还原当前工作区已修改文件)
	git reset HEAD --fileName---- 拉取版本库的指定(所有)文件到暂存区(不影响工作区) head 可以指定任意的版本id 默认head 指定最近一次
	git rm fileName			----- 删除工作区和暂存区中的文件 相当于删除文件后执行了git add
	git rm --cached fileName----- 删除暂存区的文件保留工作区的文件，在不小心将不需要被管理的文件添加到暂存区时可以用
	git rm -f fileName		----- 强制删除暂存区和工作区的文件
	git mv oldName newName	----- 重命名工作区文件并提交到暂存区 相当于 git rm oldName  git add newName