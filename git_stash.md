## 不想提交时,暂时保存工作进度
## 切换分支时,先处理当前分支的工作进度

1. git stash [save "一些信息"]
暂存当前工作进度,让工作区恢复到,最新的一次提交

2. git stash list
查看所有暂存

3. git stash pop
取出最近一次暂存,并删除该记录xxxxxx

4. git stash apply stash@{X}
取出暂存记录x

5. git stash drop stash@{x}
删除暂存记录

6. git stash clear
清除所有暂存


