@[TOC](Git 的安装和使用)
# Git 的安装
ArchLinux通过pacman -S git
Debian系通过apt-get install git
# Git 的使用
## 个人日常使用操作流程

```git
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Milkshake-lyf/test.git
git push -u origin master
/* 摘自Github新建仓库流程 */
/* 项目为临时创建，名称为test*/
```

## Git 的仓库
### 本地仓库
版本库或者是仓库，英文名Repository，其实啊说白了就是一个目录而且，这个目录中的所以文件都被git管理而且，不管你做什么操作都会被记录，包括：增加、删除、修改文件等，都会被记录下来，以便后来跟踪与修改相关记录，甚至被还原。
#### 本地仓库的创建

```git
mkdir test
cd test
git init
```
![git init 初始化本地仓库](https://img-blog.csdnimg.cn/2019093011030514.png)
### 远程仓库
Github上存放东西的仓库
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190930113527404.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)

## Git 基本命令的使用[^1]
[^1]:除去文件/文件夹的撤销删除操作

（按照一个文件/文件夹上传到Github远程仓库的顺序）
### git init

```git
git init //初始化本地仓库
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190930110910710.png)
### git status
```git
git status //查看工作区的状态
```
![git status时没有文件改动状态](https://img-blog.csdnimg.cn/20190930111049897.png)
![有文件改动时git status状态](https://img-blog.csdnimg.cn/20190930111231347.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)
### git add

```git
git add 文件名/文件夹名
git add . //提交全部文件/文件夹
// 如果文件很少建议使用第二种
// 此时文件/文件夹被添加到暂存区
// 等待被提交到本地仓库
```
![使用git add添加进暂存区](https://img-blog.csdnimg.cn/2019093011162024.png)
### git commit

```git
git commit //用来提交暂存区的文件/文件夹到本地仓库
git commit -m "提交时的说明"
// 此处说明建议有意义以方便日后查看
// 此时文件被提交到本地仓库
// 等待被push到远程仓库
```
![git commit提交到本地仓库](https://img-blog.csdnimg.cn/20190930112113571.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)
### git push

```git
git push
// 按照初始创建Github远程仓库提示
// 这里分为两步
// 先添加远程仓库地址，然后添加push到的分支
// 这里直接复制即可
git remote add origin https://github.com/Milkshake-lyf/test.git
git push -u origin master
```
![git push到远程仓库](https://img-blog.csdnimg.cn/20190930112952645.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)
### 远程仓库截图
![新建远程仓库截图](https://img-blog.csdnimg.cn/20190930113548715.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)
![远程仓库截图](https://img-blog.csdnimg.cn/20190930113136166.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NTQ5NjcxOA==,size_16,color_FFFFFF,t_70)
# Git 的三个区域

 - 工作区
 - 暂存区/提交区 (index/stage)
 - 仓库/版本库

