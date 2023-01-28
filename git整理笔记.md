# 版本控制软件

### 优点:

###### 1.操作简便，

###### 2.易于对比，

###### 3.易于回溯，

###### 4.不易丢失,

###### 5,协作方便

# 版本控制系统分类

1. ### 本地版本控制系统：单机运行，使维护文件版本的操作工具化

   ![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\1.png)

2. ### 集中化的版本控制系统：支持联网运行，支持多人协作开发；性能差，用户体验不好

   ![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\2.png)

3. ### 分布式版本控制系统：联网运行，支持多人协作开发；性能优秀，用户体验好

   ![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\3.png)

# Git基础概念

### Git特点

项目越大越复杂，协同开发者越多，越能体现出Git的高性能和高可用性

### Git特性 

1. 直接记录快照，而非差异比较
2. 近乎所有操作都是本地执行

### 与svn差异比较

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\4.png)



### Git的记录快照

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\5.png)

### 近乎所有操作都在本地执行

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\6.png)

### Git中的三个区域

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\7.png)

### Git中的三种状态

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\8.png)

### 基本的Git工作流程

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\9.png)

# Git安装并配置

### 安装Git 

直接搜索如下地址选择对应安装包next知道安装即可：

[git下载]: https://git-scm.com/downloads

### 配置用户信息

#### 首次安装需配置git用户名和邮件地址

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\10.png)

```git
git config --global user.name "设置git使用者的用户名"
git config --global user.email "设置git使用者的邮箱"
```

#### Git的全局配置文件

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\12.png)

#### 检查Git配置信息

除了使用记事本查看全局的配置信息之外，还可以运行如下的终端命令，快速的查看Git的全局配置信息:

##### 1.查看所有的全局配置项

```git
git config --list --global
```

##### 2.查看指定的全局配置项

```git
git config user.name
git config user.email
```

### 获取帮助信息

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\13.png)

# Git 的基本操作

## 1.获取 Git 仓库的两种方式

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\14.png)

## 2.在现有目录中初始化仓库

```git
# 在需要初始化git仓库的目录中使用git bash命令执行
git init
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\15.png)

## 3.工作区中文件的4种状态

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\16.png)

## 4.检查文件的状态

```git
# 检查文件状态
git status
# 以精简的方式显示文件状态
git status -s
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\17.png)

## 5.跟踪新文件

```git
git add 文件名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\18.png)

## 6.更新

```git
git commit -m "对本次提交内容的进一步描述"
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\19.png)

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\20.png)

## 7.对已提交的文件进行修改

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\21.png)

## 8.暂存已修改的文件

```git
git add 需暂存的文件名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\22.png)

## 9.提交已暂存的文件

```git
git commit -m "提交消息"
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\23.png)

## 10.撤销对文件的修改

```git
git checkout -- 撤销修改的文件名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\24.png)

## 11.向暂存区中一次性添加多个文件

```git
git add .
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\25.png)

## 12.取消暂存的文件

```git
git reset HEAD 要移除的文件名称
```

## 13.跳过使用暂存区域

```git
git commit -a -m "描述消息"
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\26.png)

## 14.移除文件

```git
# 从 Git 仓库和工作区同时移除文件
git rm -f 要移除的文件名称
# 只从 Git 仓库中移除文件，但保留工作区中的文件
git rm --cached 要移除的文件名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\27.png)

## 15.忽略文件

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\28.png)

## 16.glob模式

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\29.png)

## 17. .gitignore 文件的例子

```git
# 忽略所有的 .a 文件
*.a

# 跟踪所有的 lib.a，即使在前面忽略了 .a 文件
!lib.a

# 只忽略当前目录下的 TODO 文件，而不忽略 subdir/TODO
/TODO

# 忽略任何目录下名为 build 的文件夹
build/

# 忽略 doc/notes.txt，但不忽略 doc/server/arch.txt
doc/*.txt

# 忽略 doc/ 目录以及所有子目录下的 .pdf 文件
doc/**/*.pdf
```

## 18.查看提交历史

如果希望回顾项目的提交历史，可以使用 git log 这个简单且有效的命令

```git
# 按时间先后顺序列出所有的提交历史，最近的提交排在最上面
git log

# 只展示最新的两条提交历史，数字可以按需进行填写
git log -2

# 在一行上展示最近两条提交历史的信息
git log -2 --pretty=oneline

# 在一行上展示最近两条提交历史的信息，并自定义输出的格式
# %h 提交的简写哈希值 %an 作者名字 %ar 作者修订日期,按多久以前的方式显示 %s提交说明
git log -2 --pretty=format:"%h | %an | %ar | %s"
```

## 19.回退到指定的版本

```git
# 在一行上展示所有的提交历史
git log --pretty=oneline

# 使用 git reset --hard 命令，根据指定的提交 ID 回退到指定版本
git reset --hard <CommitID>

# 在旧版本中使用 git reflog --pretty=oneline 命令，查看命令操作的历史
git reflog --pretty=oneline

# 再次根据最新的提交 ID，跳转到最新的版本
git reset --hard <CommitID>
```

# 开源相关概念

## 开源托管平台

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\30.png)

# Github介绍

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\31.png)

## Github远程仓库的使用

### 远程仓库的两种访问方式

 ![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\32.png)

### 基于HTTPS将本地仓库上传到Github

```git
# 第一次关联远程仓库必须执行完整的 git push -u origin master 命令
git push -u origin master
# 连接后只需要执行 git push 就能推送到远程仓库
git push
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\33.png)

### 基于SSH将本地仓库上传到Github

#### SSH key

###  ![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\34.png)

#### 生成 SSH key

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\35.png)

#### 配置 SSH key

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\36.png)

#### 检测 Github 的 SSH key 是否配置成功

```git
ssh -T git@github.com
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\37.png)

#### 上传

```git
# 第一次关联远程仓库必须执行完整的 git push -u origin master 命令
git push -u origin master
# 连接后只需要执行 git push 就能推送到远程仓库
git push
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\38.png)

### 将远程仓库克隆到本地

```git
# 打开 Git Bash，输入以下命令
git clone 远程仓库的地址
```

# Git分支-本地分支操作

## 分支概念

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\39.png)

## 分支在实际开发中的作用

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\40.png)

## master 主分支

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\41.png)

## 功能分支

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\42.png)

# 分支操作

## 查看分支列表

```git
# 查看当前Git仓库中所有分支列表
git branch
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\43.png)

## 创建新分支

使用如下的命令，可以基于当前分支，创建一个新的分支，此时，新分支中的代码和当前分支完全一样

```git
git branch 新分支名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\44.png)

## 切换分支

使用如下命令，可以切换到指定的分支上进行开发

```git
git checkout 要切换的分支名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\45.png)

## 分支的快速创建和切换

使用如下的命令，可以创建指定名称的新分支，并立即切换到新分支上：

```git
# -b 表示创建一个新分支
# checkout 表示切换到刚才新建的分支上
git checkout -b 新分支名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\46.png)

## 合并分支

功能分支的代码开发测试完毕之后，可以使用如下的命令，将完成后的代码合并到 master 主分支上：

```git
# 1.切换到 master 分支
git checkout master
# 2.在 master 主分支上运行 git merge 命令，将 login 分支的代码合并到 master 主分支
git merge 需要合并到主分支的分支名称
```

## 删除分支

当把功能分支的代码合并到 master 主分支上以后，就可以使用如下命令，删除对应的功能分支:

```git
git branch -d 要删除的分支名称
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\47.png)

## 遇到冲突时的分支合并

```git
# 假设：在把reg分支合并到master分支期间，代码发生了冲突
git checkout master
git merge reg

# 打开包含冲突的文件，手动解决冲突之后，再执行如下命令
git add .
git commit -m "解决了分支合并冲突的问题"
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\48.png)

# 远程分支操作

## 将本地分支推送到远程仓库

如果时 第一次 将本地分支推送到远程仓库，需要运行如下的命令:

```git
# -u 表示把本地分支和远程分支进行关联，只在第一次推送的时候需要带 -u 参数
git push -u 远程仓库的别名 本地分支名称:远程分支名称

# 实际案例：
git push -u origin payment:pay

# 如果希望远程分支的名称和本地分支名称保持一致，可以对命令进行简化：
git push -u origin payment
```

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\49.png)

## 查看远程仓库中所有的分支列表

通过如下命令，可以查看远程仓库中，所有的分支列表的信息：

```git
git remote show 远程仓库名称
```

## 跟踪分支

跟踪分支指的是：从远程仓库中，把远程分支下载到本地仓库中。需要运行的命令如下：

```git
# 从远程仓库中，把对应的远程分支下载到本地仓库，保持本地分支和远程分支名称相同
git checkout 远程分支的名称

#示例:
git checkout pay

# 从远程仓库中，把对应的远程分支下载到本地仓库，并把下载的本地分支进行重命名
git checkout -b 本地分支名称 远程仓库名称/远程分支名称
#示例：
git checkout -b payment origin/pay
```

## 拉取远程分支的最新代码

可以使用如下命令，把远程分支最新的代码下载到本地对应的分支中：

```git
# 从远程仓库，拉取当前分支最新的代码及，保持当前分支的代码和远程分支代码一致
git pull
```

## 删除远程分支

可以使用如下命令，删除远程仓库中指定的分支：

```git
# 删除远程仓库中，指定名称的远程分支
git push 远程仓库名称 --delete 远程分支名称
#示例：
git push origin --delete pay
```

# 总结

![](C:\Users\uu\Desktop\技术文档\技术知识照片截图\git\gitimage\50.png)