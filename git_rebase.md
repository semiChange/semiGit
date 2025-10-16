## 变基操作






## 修改提交信息
1. 查看提交信息
git log
b2c4743 test1
664d5e1 init  (第一次提交)

2. 操作想要修改init信息 (rebase 注意顺序是反的)
git rebase -i HEAD~2
pick 664d5e1 init (第一次提交)
pick b2c4743 test1 

3. 把pick 改为e或edit, 然后保存退出
e664d5e1 init (第一次提交)
pick b2c4743 test1 

4. 提示 使用 git commit --amend 然后 git rebase --continue
git commit --amend
把init 改为 init modify
git rebase --continue