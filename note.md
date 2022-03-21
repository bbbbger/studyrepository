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

### 同步远程仓库

~~~

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



