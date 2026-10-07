一个流程例子
```
# 初始化仓库
git clone https://github.com/user/repo.git
cd repo

# 创建并切换到新分支
git checkout -b feature/new-feature

# 添加并提交修改
touch new_file.txt
git add new_file.txt
git commit -m "添加新文件"

# 推送分支到远程
git push -u origin feature/new-feature

# 拉取最新更新
git pull origin main

# 合并分支
git checkout main
git merge feature/new-feature
```

问题
1. 如何拿到前n个版本。
2. 其实完全可以本地尝试几乎所有功能，远程仓库只是一个复制品。



操作
首先我们要知道，git先是为自己的代码版本服务，再是和别人共享。
1. git commit--提交一个更改
2. git branch xxx, git checkout -b xxx--创建一个分支
3. git checkout xxx--将HEAD指向一个commit，或一个分支
4. git merge xxx--将HEAD所在分支与另一个分支xxx合并（可能产生冲突），生成一个新的commit，由HEAD所在分支指向，另一个分支不动。
5. git rebase xxx--将HEAD指向的分支与xxx分支串起来，在xxx分支后生成一个新的commit，原HEAD指向的分支消失。HEAD和其原分支指向新的commit，xxx分支不动。最后git rebase <HEAD指向的分支>，将xxx分支后移。
6. `git HEAD~<n>`和`git HEAD^`移动HEAD指向分支或commit
7. git reset HEAD~1--返回前1个版本，此版本删除，用于本地
8. git revert HEAD~1--返回前1个版本，区别在于是新的commit，用于远程
9. git cheryy-pick xx xxx--从xx到xxx复制到HEAD所在分支，和rebase相同，但是不删除原分支
10. git branch -f main HEAD~3--改变分支位置


远程问题
1. 我在本地commit了更新，别人在远程push了新的版本和其他东西，我再push会发生什么，或者此时我如何只pull（或fetch）我想要的东西
2. 我想撤销某一个指令，比如pull

远程操作
1. git clone
2. git fetch--下载日志和最新分支图，但不会影响本地
3. git pull--相当于fetch和merge/rebase/cherry-pick的结合