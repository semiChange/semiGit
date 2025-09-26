### git diff <file>
* 通常都是跟 工作区(最新)+ 进行比较
* 总结: 
*   老的默认是 暂存区, HEAD或commitID 就表示老的是 版本库
*   git diff HEAD 
*   新的默认是 工作区, --cached 表示为新的是 暂存区    

    比较 -老<暂存区> 和 +新<工作区> 的差异 
如果修改了工作区, 还没有添加到暂存区

--- 暂存区
+++ 工作区

@@ -起始行,结尾行 +起始行,结尾行 @@

### git diff --cached/staged 文件名
* 添加了 -- 选项则表示跟指定的 位置(最新)进行 比较
* 老的只有 版本库了
比较 -版本库 和 +暂存区 差异


### git diff <commitID> <commitID>
比较 2个版本库 差异


### git diff <branch1> <branch2>
比较2个分支之间的差异


### git diff <commit>
* 还是跟 工作区(最新)+ 进行比较, 但是是拿版本库- 作为老的


### git diff --stat
只查看差异的数量 ,增加和减少的行数









