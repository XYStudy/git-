** 
* 同时push代码到git出现冲突问题
** 
git log 查看第二次的log，然后复制字符串
git reset --soft 复制的字符串（回退到某个版本，只回退了commit的信息,并且保存了本地修改）
git stash 将本地代码缓存到stash
git pull 拉取远程代码
git stash pop 将本地缓存的代码和远程拉取的代码 整合

git stash pop可以用 git stash apply stash@{0} 代替
git stash list 查看本地stash的版本，想要哪个就stash apply stash@{*}

** 
* 本地已有代码初始化提交到git
** 
git init 初始化git
git remote add origin + 项目地址  与远程仓库连接
git add .
git commit -m '***'
git push -u origin master 

** 
* 分支创建并切换
** 
git checkout -b newBranchName
git add .
git commit -m 'init newBranch'
git push origin newBranchName

** 
* 仓库地址操作
** 
git remote -v 查看当前仓库的地址
git remote set-url origin + 地址  与远程仓库连接

** 
* 更新远程分支到本地
git remote update origin --prune
