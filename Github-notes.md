>##什么是版本控制（VCS）？
>版本控制是一种记录若干文件内容变化，以便将来查阅特定版本修订情况的系统。
>然而Git只关心文件数据的整体是否发生变化,而大多数其他系统则只关心文件内容的具体差异，这类系统(Cvs,Subversion,Perforce,Bazaar 等等)每次记录有哪些文件>作了更新,以及都更新了哪些行的什么内容。

>##版本控制类型：
<p>本地版本控制、集中化的版本控制、分布式版本控制</p>
>##Git和其他版本控制系统的主要差别是什么？
>1、Git 只关心文件数据的整体是否发生变化，而大多数其他系统则只关心文件内容的具体差异。这类系统（CVS，Subversion，Perforce，Bazaar 等等）每次记录有哪些文件作了更新，以及都更新了哪些行的什么内容(直接快照而非比较差异)。<br/>
>2、近乎所有操作都可本地执行：在Git 中的绝大多数操作都只需要访问本地文件和资源，不用连网。但如果用CVCS 的话，差不多所有操作都需要连接网络。因为Git在本>地磁盘上就保存着所有有关当前项目的历史更新，所以处理起来速度飞快。<br/>
>3、时刻保持数据完整性：在保存到Git 之前，所有数据都要进行内容的校验和（checksum）计算，并将此结果作为数据的唯一标识和索引。<br/>
>##三种状态：
<p>已提交（committed），已修改（modified）和已暂存（staged）。</p>

>##Linux命令：
1.git --help：查看帮助
2.pwd：用于显示当前目录
3.cd：修改路径
4.mkdir：新建文件
5.ls -ah：查看隐藏文件
6.cd ..：回到上一级目录
7.vim：进入编辑状态
8.ZZ：退出vim进入的编辑状态
9.git add ：（这是个多功能命令，根据目标文件的状态不同，此命令的效果也不同：可以用它开始跟踪新文件，或者把已跟踪的文件放到暂存区，还能用于合并时把有冲突的文件标记为已解决状态等）
10.rm 文件名 -rf：删除文件及其里面的内容
11.cat主要有三大功能：(1)一次显示整个文件。$ cat filename(2)从键盘创建一个文件。$ cat > filename只能创建新文件,不能编辑已有文件.(3)将几个文件合并为一个文件： $cat file1 file2 > file。更多链接：[Cat命令](http://blog.csdn.net/tanga842428/article/details/52628357)<br/>
详见书《Pro Git》或[Git-help](https://git-scm.com/book/en/v2)
>##Git使用规范流程
[Git使用规范流程](http://mp.weixin.qq.com/s?__biz=MzAxODI5ODMwOA==&mid=2666540296&idx=1&sn=bcaa54a27bc521f39c88b8072fd7073b&chksm=80dce9a3b7ab60b5cbb6246874ff0c61a94971e6144dc691e29d0492379de8776d0c29ec03b6&mpshare=1&scene=23&srcid=0117cMMmmZFYfOiFV95XVQTz#rd)
>##从远程仓库克隆到提交本地内容到远程仓库过程及一些简单操作:
>-克隆：git clone 地址
>-本地新建文件：touch README.md
>-本地新建文件：mkdir 文件名
>-跟踪新文件：git add 文件名（git status查看最近更新情况及哪些待提交）
>-提交：git commit -m '说明内容'
>-初次需要执行：git remote add origin 地址
>-提交到远程仓库：git push origin master
>-中途遇到个问题：在远程仓库删除了个文件结果更新下来有问题，解决方法： git pull --rebase origin master。[更多:](http://www.tuicool.com/articles/3aIvQfU)
>-[查看未提交到远程仓库的一些命令：](http://blog.csdn.net/kakaxi2222/article/details/46011717)
>-[更多详情：](http://blog.csdn.net/steven6977/article/details/10567719)
>##删除文件并更新
>-把远程仓库更新到本地：git pull 
>-删除本地的文件：git rm 文件名（README.md）
>-提交到远程仓库：git commit -m '说明'
>-git push 即可git pulL命令更多：](http://www.yiibai.com/git/git_pull.html)
>-[更多详情：](http://jingyan.baidu.com/article/2a1383288e2ba5074a134fb5.html)
