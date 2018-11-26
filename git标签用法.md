### Git tag(标签) 用法
> 1. 切换到某一分支下，如master,针对该分支，进行tag操作；
> 2. 为最近一次commit打标签；
> > 2.1 方式一: 当本地commit之后，执行以下命令：

> > >     git tag tag_name

> > 2.2 方式二:为特定的commit打标签,执行以下命令: 

> > >     git tag test_tag c809ddbf83939a89659e51dc2a5fe183af384233　　　　//在某个commit 上打tag

> > 2.3 方式三: 运行tag 命令时指定-a选项创建附注标签:

> > >     git tag -a tag_name -m " create one tag,it's name is tag_name "

> 3. 删除本地标签:

>     git tag -d tag_name

> 4. 删除远程标签:

>     git push origin :refs/tags/tag_name

>5. 将本地tag推送到远程:

> > >    git push origin tag_name    //推送单一tag

> > >    git push origin --tags    //一次推送多个tag

> 详情查看:https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE
>
>  ### 拉取tag分支

> >  先 git clone 整个仓库，然后 git checkout tag_name 就可以取得 tag 对应的代码:

> > >      git checkout tag_name

> > 但是这时候 git 可能会提示你当前处于一个“detached HEAD” 状态，因为 tag 相当于是一个快照，是不能更改它的代码的，如果要在 tag 代码的基础上做修改，你需要一个分支： 

> > >      git checkout -b branch_name tag_name 

> > 这样会从 tag 创建一个分支，然后就和普通的 git 操作一样了。其实要取得不同的branch的tag，只需要在相应的分支上打tag就行了。这样的tag就唯一对应了不同的分支。例如，你在master上打了tag为v1，在某个branch上打了tag为v2，则你取出v2代码的时候，自然就是对应的branch分支了。
