## git branch
查看所有分支

$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master


## 移动指定分支
// 把main分支,基于当前HEAD位置往前移动3个  
git branch -f main HEAD~3  
// 当然也能直接指定 commitID去移动指定分支
git branch -f dev C3






