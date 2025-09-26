```c
// 初始化本地库
PS D:\semiGit> git init
Initialized empty Git repository in D:/semiGit/.git/

// 添加远程库
PS D:\semiGit> git remote add origin https://github.com/semi/testGit.git

// 查看远程库
PS D:\semiGit> git remote -v
origin  https://github.com/semi/testGit.git (fetch)
origin  https://github.com/semi/testGit.git (push)

// 拉取远程
PS D:\semiGit> git fetch origin
remote: Enumerating objects: 32, done.
remote: Total 32 (delta 0), reused 0 (delta 0), pack-reused 32 (from 1)
Unpacking objects: 100% (32/32), done.
From https://github.com/semi/testGit
 * [new branch]      master     -> origin/master

// 查看分支情况
PS D:\semiGit> git branch -a
  remotes/origin/master

// 合并分支
PS D:\semiGit> git merge origin/master

// 查看分支情况
PS D:\semiGit> git branch -a
* master
  remotes/origin/maste

  ```