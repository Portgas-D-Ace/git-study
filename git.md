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
	git add  'filename'	or .----- 将已修改的指定(所有)文件提交到暂存区 
	git commit -m			----- 将暂存区的文件提交的版本库
	git commit -am			----- 将已修改的文件直接提交到版本库
	git commit --amend 		----- 撤销上一次提交的版本并将暂存区文件提交到版本库
