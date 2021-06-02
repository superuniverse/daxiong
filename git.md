配置邮箱和用户名

git config --global user.name 'nowLetsgo'
git config --global user.email 'lipeihua0922@163.com'

git config --global -l  查看全局配置

git config --global  user.name  查看全局的用户名配置

git config --global  user.email ：查看全局的邮箱配置



git init ：初始化仓库

git status:版本状态查看

git add fileName/./*:把某次工作区改动的文件 或者工作区全部改动文件  提交到暂存区

	- 红色：目前只存在在工作区
	- 绿色：目前存在在暂存区
	- 没有：目前三个区域内容一直 

git commit -m '提交注释信息'

git commit -am '注释'：跳过暂存 提交已经跟踪的文件修改



git restore ./filename : 撤销工作区的改动到最近的提交（未跟踪的文件不能撤销，自行删除）

git restore --staged ./filename :撤销暂存区的修改到工作区



git rm fileName : 删除工作区和暂存区的某个文件

git rm --cached filename:删除暂存区的某个文件

git rm -f filename:强制删除工作区和暂存区的文件



git mv oldname newname:给文件重命名  直接修改了工作区和暂存区的

git mv  filename dirname/ :把文件移动到某个路径

git mv dirname/filename  filename:移动文件并改名



git log:查看提交日志 如果日志过多 使用上下键控制  使用q退出

git log --oneline:查看提交日志 简化版





git diff：比较暂存区和工作区的差异

git diff --cached:比较暂存区和仓库区当前版本的差异

git diff a b:比较两个版本之间的差异



git reflog：查看仓库区所有的操作

git reset --hard commitID:回退到某一个版本 并重置工作区和暂存区

git reset --mixed commitID：回退到某一个版本 并重置暂存区

git reset --soft commitID：回退到某一个版本 只重置仓库区

git reset --hard HEAD~1： 回退到上一个版本





.gitignore:配置忽略文件

如果某个文件已经被提交了，那么此时直接忽略无效，需要先手动删除暂存区的这个文件，然后再配置忽略，提交



git branch 查看所有的分支

git branch branchName:创建一个分支（相当于把某个分支包含提交信息完全拷贝了一份）

git checkout branchname：切换到某个分支

git checkout -b branchname：创建并切换分支

git checkout -B branchname：创建并切换分支（如果已经存在该分支，则直接强制覆盖）

git checkout -b branchname commitID:从指定提交节点创建分支

git checkout --orphan branchname: 创建一个裸分支。裸分支和其他分支没有什么不同，就是裸分支开始的时候，没有父分支的commit提交记录



git branch -d branchname:删除某个分支

git branch -D branchname：当两个分支提交记录不同的时候 强制删除某个分支



git merge branchName:合并分支

如果有冲突，则需要解决冲突 并重新提交



