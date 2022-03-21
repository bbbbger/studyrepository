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
2、git status   可显示工作目录和暂存区的状态，untracked files即添加到工作目录下，但为提交到本地仓库中的文件
3、git add <file name>  
~~~

