# Git远程操作详解

### 作者： 阮一峰
### 日期： 2014年6月12日

Git是目前最流行的版本管理系统，学会Git几乎成了开发者的必备技能。
Git有很多优势，其中之一就是远程操作非常简便。本文详细介绍5个Git命令，它们的概念和用法，理解了这些内容，你就会完全掌握Git远程操作。
* git clone
* git remote
* git fetch
* git pull
* git push
本文针对初级用户，从最简单的讲起，但是需要读者对Git的基本用法有所了解。同时，本文覆盖了上面5个命令的几乎所有的常用用法，所以对于熟练用户也有参考价值。

#### 流程图
![流程](https://github.com/rockgs/myblog/blob/master/20170802/bg2014061202%5B1%5D.jpg)

### 一、git clone
远程操作的第一步，通常是从远程主机克隆一个版本库，这时就要用到git clone命令。
```
$ git clone <版本库的网址>
```
比如，克隆jQuery的版本库。
```
git clone https://github.com/jquery/jquery.git
```
该命令会在本地主机生成一个目录，与远程主机的版本库同名。如果要指定不同的目录名，可以将目录名作为git clone命令的第二个参数。
```
git clone <版本库的网址> <本地目录名>
```

git clone支持多种协议，除了HTTP(s)以外，还支持SSH、Git、本地文件协议等，下面是一些例子。
```
git clone http[s]://example.com/path/to/repo.git/
git clone ssh://example.com/path/to/repo.git/ 
git clone git://example.com/path/to/repo.git/
git clone /opt/git/project.git
git clone file:///opt/git/project.git
git clone ftp[s]://example.com/path/to/repo.git/
git clone rsync://example.com/path/to/repo.git/
```
SSH协议还有另一种写法。
```
git clone [user@]example.com:path/to/repo.git/
```
通常来说，Git协议下载速度最快，SSH协议用于需要用户认证的场合。各种协议优劣的详细讨论请参考官方文档。





