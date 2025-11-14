## 日志示例
$ git log --oneline
ea9ac9a (HEAD -> master) zj:v7  // 本地HEAD头位置 (表示本地提交提早远程提交)
5f324e7 zj: v6
f35faf0 zj: v5
dfd2f01 (origin/master, origin/HEAD) zj:v4  // 远程HEAD头位置
745e267 zj: v3
edff7ea zj: v2
e76f460 zj: v1

注: 如果git pull 提示 already up to date 表示本地库的最新远程数据已经和远程库数据相同
只是本地库的提交比远程库更新




## 查看commit记录
* git log --graph --oneline
--pretty 格式化输出  
默认是单行显示 %n 可以换行



--date 自定义日期格式


--oneline 单行显示






## git log 查看区间
$ git log --oneline
55431b7 v2
01e3cb3 v2
625b947 v1

$ git log 625b..5543   (旧..新)  注意625b不会展示  
commit 55431b7c1b5f77b9e3561a1c8506c470095bc016
Author: zj <zj@example.com>
Date:   Sun Jun 3 18:38:56 2018 +0800

    v2

commit 01e3cb3a2470e7853ce0998313f46005187ed348
Author: zj <zj@example.com>
Date:   Sun Jun 3 17:42:27 2018 +0800

    v2


## git log 自定义格式
$ git log --oneline --pretty=format:"%h %ai %s"
eb76382 2025-10-16 13:24:00 +0800 cc
413e9b9 2025-10-11 14:36:10 +0800 bb
f2c9d00 2025-10-11 10:35:44 +0800 aa
查看commit记录
git log --graph --oneline
