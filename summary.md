## git配置
命令：git config
作用：配置、读取 环境变量
说明：变量存放位置，
1. /etc/gitconfig  使用 git config --system 操作此文件,针对系统中所有用户
2. ~/.gitconfig 使用 git config --global 操作此文件,针对当前用户
3. .git/config 只针对当前工作目录, 内层配置会覆盖外层

### 配置用户信息
git config --global user.name "runoob"
git config --global user.email test@runoob.com

### 查看配置信息
git config --list

## 工作流程
(本地库) (缓存区) (工作区)
1. 克隆仓库
(远程仓库) -> (本地仓库)
参与一个已有的项目,需要克隆到本地,变成本地仓库
git clone https://github.com/xxx/test.git
cd test

2. 创建新分支
通常不建议在master分支上开发, 创建一个新的分支
git checkout -b slave

3. 修改文件后缓存文件
 (缓存区) < 工作区
git add 1.txt

4. 提交更改
 (本地仓库) < 缓存区
git commit -m "修改的概括"

5. 拉取最新
推送本地仓库之前,最好拉取远程,避免冲突
(远程仓库)->(本地仓库)
git pull origin main
或者拉取成新分支名
git pull origin new-branch

6. 推送更改
(本地仓库)->(远程仓库)
git push origin new-branch

### 如何删除分支
git branch -d old-branch
git push origin --delete old-branch

## git 工作区/缓存区/版本库 概念
工作区: 就是电脑上看到的目录
缓存区a2: stage/index 也叫索引区, 在.git/index文件中
版本库a3: 在 .git目录, 版本库中包含了缓存区

### 一些说明
(工作区) <--> {(缓存区)<-->(版本库)}
HEAD 指向 master  所以命令中的HEAD都可以用分支名替代

git add :                   缓存区index索引目录被更新
git reset HEAD :            缓存区index索引目录被重写,工作区不变
git rm --cached <file>      缓存区文件被删除,工作区不变
git checkout ./<file>       会用缓存区文件替换工作区,会清除工作区未添加到缓存区的内容
git checkout HEAD ./<file>  既清除工作区未提交改动,也清除缓存区未提交改动
a1

a2
