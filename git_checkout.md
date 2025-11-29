## git checkout 分支名/CommitID


默认HEAD指向分支名  

如果指向 CommitID 就表示HEAD头分离  

eg.  

** main分支 **   
// 这里移动的是HEAD头 , 当然分支默认就是指向HEAD的 
git checkout C1  
那么 HEAD -> main -> C1  


HEAD^ 表示HEAD的父一级  
HEAD~n  表示多级  


### 可以指定分支操作
// 这里移动的是分支  
git branch -f 分支名 HEAD~n  





