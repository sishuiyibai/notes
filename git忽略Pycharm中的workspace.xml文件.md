### 忽略workspace.xml等文件
> 1. 在项目还没有git add .之前，在.gitignore 文件中加入 .idea
> 2. 如果已经git add .了，再在.gitignore中加入.idea ，就已经没有用了。
> 3. 最好把.idea/workspace.xml写入.gitignore文件中
> 4. 确保远程分支上不存在.idea文件，如果存在该文件，请用本地git 将删除该文件后的项目push上去，当用pycharm重新pull时，会在本地自动创建新的.idea文件，此时.gitignore已配置忽略该文件夹，后续提交时不会再提示commit 该文件夹下文件的相关信息。
>> 此时，需要运行命令 git rm --cached -r .idea
