# 在使用git将本地现有的项目和远程的仓库关联的时候的相关步骤：
首先打开AndroidStudio上的Terminal。
1.没有进行过任何git初始化操作的时候，输入命令：git init
生成.git文件初始化git。
2.输入命令：git clone 你的仓库地址例如：git clone https://github.com/**/**.git
3.本地项目不能是空文件夹，所以需要执行git add .命令将所有添加和修改的文件添加到暂存区，
4.使用git status查看是否将所有添加和修改的文件添加到暂存区，
出现Changes not staged for commit:提示时，说明还有文件没有添加到暂存区（见红色的输出文字），
如果没有出现Changes not staged for commit:提示时，只有Changes to be committed:和下面的绿色输出文字，
那么证明已经将所有添加和修改的文件添加到暂存区。
5.输入命令：git commit -m 后面空格加上你的更新日志信息，否则会有问题
6.输入命令：git push origin **/**  将本地的分支代码push到远程分支

如果你想创建新的本地分支和切换本地分支
按如下操作：
前提是你本地有master分支
1.查看本地分支：输入命令：git branch -l
带星号的是当前使用分支
2.创建新的分支dev：git branch dev
3.查看本地分支是否有dev: 输入命令：git branch -l
4.切换本地分支到分支dev: 输入命令：git checkout dev
切换完成后再查看下当前分支是否是dev分支。


如果你想将本地分支提交到远程仓库添加（给远程仓库添加新的分支）
git 本地给远程仓库创建分支 三步法
命令如下:
1.本地创建分支dev
    命令：git branch dev
2.下面是把本地分支提交到远程仓库
    命令：git push origin dev
3. 查看一下远程仓库有几个分支
    git branch -a
    输出：
    dev
    * master *号代表你现在所在的分支

      remotes/origin/dev  远程仓库dev分支
      remotes/origin/master  远程仓库master分支

