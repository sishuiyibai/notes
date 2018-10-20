### 忽略workspace.xml等文件
> 1. 在项目还没有git add .之前，在.gitignore 文件中加入 .idea
> 2. 如果已经git add .了，再在.gitignore中加入.idea ，就已经没有用了。
> 3. 最好把.idea/workspace.xml写入.gitignore文件中
>> 此时，需要运行命令 git rm --cached -r .idea
