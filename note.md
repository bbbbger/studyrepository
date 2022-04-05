# git 笔记



~~~
git config --global <key> <value>     // --global 表示本机上所有仓库都会使用这个配置

git config --global user.name "bbbbger"
git config --global user.email "<myemail>@email.com"
~~~

### 创建仓库

~~~git
1、选择一个空文件夹，在此路径下打开 git bash
2、git init   //初始化仓库，此时空文件夹下会生成一个.git文件夹，为仓库的管理文件

~~~

### 本地仓库提交文件

~~~
1、在仓库中存在更改或添加的文件
2、git status   可显示工作目录和暂存区的状态，untracked files（红色名）即添加到工作目录下，但为提交到本地仓库中的文件
3、git add <file name>   将文件添加到暂存区changes to be committed（绿色名）  使用git add . 将所有untracked file 添加到暂存区
4、git commmit -m"message"       message为本次提交的备注信息，最好写。此命令将暂存区文件提交到本地仓库
~~~

### 修改文件

~~~
修改已提交的文件
1、git status 可以查看被修改的文件
2、git diff 可以查看修改前后具体不同的部分，减号后为删去部分，加号后为新加部分。可选参数 HEAD --<文件名>  查看工作区文件与当前版本内文件差别
3、git checkout --<文件名>  撤销文件在工作区的所有修改，回到最近一次add或commit时的状态。

4、git reset HEAD <文件名>  将暂存区文件打回工作区，git reset的另一个功能
~~~

### 同步远程仓库

~~~
1、git remote add origin <仓库链接>      //github改规则了，估计要用令牌，格式<https://token@github.com/username/repo.git>
2、git push -u origin master   //第一次提交远程仓库，之后再提交直接git push就可以

3、git remote -v 查看远程库信息
4、git remote rm origin  删除远程库

~~~



### 克隆仓库

~~~
1、git clone <仓库链接>
~~~

### 协同开发

~~~
1、git pull   远程仓库同步到本地仓库，用于协同开发的场景，保证一致
~~~







### 版本信息

~~~ 
git log  显示提交日志信息，后面可跟参数控制显示信息
git reset --hard HEAD^  命令回退到上个历史版本，暂时别用。HEAD表示当前版本，HEAD^表示上个版本，HEAD^^表示上上个等等。n个版本就是HEAD~n。 也可以直接指定commit id，即--hard <commit id> 只需要写前几位，git会自动补齐。

git reflog 记录所有执行的命令，可以找到历史commit id，然后再指定回当前版本。
~~~

### 工作区和暂存区

~~~

~~~

![](D:\from github\studyrepository\工作区与暂存区.jpg)



### 删除文件

~~~
1、rm <文件名>
2、git status查看被删除文件
3、git rm <文件名>
4、git commit -m"delete a file" 仓库中文件就被删除了
5、git remote
6、git push
~~~



## 分支管理

### 创建与合并分支

~~~
1、git checkout -b <new branch name>    创建并切换到新分支等价与下面两条命令
1.1、git branch <new branch neme>       创建新分支
1.2、git checkout <new branch name>     切换到新分支

2、git checkout master
3、git merge <branch name>      把分支合并到当前分支中

4、git branch -d <branch name>  删除分支

\*
1、在新分支上修改的文件如果不add和commit，切换到master分支后通过git status命令仍旧能查看到修改，即工作区和暂存区是所有分支共享的。

*\
~~~





