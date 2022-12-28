# 版本控制软件

### 优点:

###### 1.操作简便，

###### 2.易于对比，

###### 3.易于回溯，

###### 4.不易丢失,

###### 5,协作方便

# 版本控制系统分类

1. ### 本地版本控制系统：单机运行，使维护文件版本的操作工具化

   ![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\1.png)

2. ### 集中化的版本控制系统：支持联网运行，支持多人协作开发；性能差，用户体验不好

   ![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\2.png)

3. ### 分布式版本控制系统：联网运行，支持多人协作开发；性能优秀，用户体验好

   ![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\3.png)

# Git基础概念

### Git特点

项目越大越复杂，协同开发者越多，越能体现出Git的高性能和高可用性

### Git特性 

1. 直接记录快照，而非差异比较
2. 近乎所有操作都是本地执行

### 与svn差异比较

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\4.png)



### Git的记录快照

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\5.png)

### 近乎所有操作都在本地执行

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\6.png)

### Git中的三个区域

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\7.png)

### Git中的三种状态

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\8.png)

### 基本的Git工作流程

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\9.png)

# Git安装并配置

### 安装Git 

直接搜索如下地址选择对应安装包next知道安装即可：

[git下载]: https://git-scm.com/downloads

### 配置用户信息

#### 首次安装需配置git用户名和邮件地址

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\10.png)

```
git config --global user.name "设置git使用者的用户名"
git config --global user.email "设置git使用者的邮箱"
```

#### Git的全局配置文件

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\12.png)

#### 检查Git配置信息

除了使用记事本查看全局的配置信息之外，还可以运行如下的终端命令，快速的查看Git的全局配置信息:

##### 1.查看所有的全局配置项

```
git config --list --global
```

##### 2.查看指定的全局配置项

```
git config user.name
git config user.email
```

### 获取帮助信息

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\13.png)

# Git 的基本操作

## 1.获取 Git 仓库的两种方式

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\14.png)

## 2.在现有目录中初始化仓库

```
# 在需要初始化git仓库的目录中使用git bash命令执行
git init
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\15.png)

## 3.工作区中文件的4种状态

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\16.png)

## 4.检查文件的状态

```
# 检查文件状态
git status
# 以精简的方式显示文件状态
git status -s
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\17.png)

## 5.跟踪新文件

```
git add 文件名称
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\18.png)

## 6.更新

```
git commit -m "对本次提交内容的进一步描述"
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\19.png)

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\20.png)

## 7.对已提交的文件进行修改

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\21.png)

## 8.暂存已修改的文件

```
git add 需暂存的文件名称
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\22.png)

## 9.提交已暂存的文件

```
git commit -m "提交消息"
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\23.png)

## 10.撤销对文件的修改

```
git checkout -- 撤销修改的文件名称
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\24.png)

## 11.向暂存区中一次性添加多个文件

```
git add .
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\25.png)

## 12.取消暂存的文件

```
git reset HEAD 要移除的文件名称
```

## 13.跳过使用暂存区域

```
git commit -a -m "描述消息"
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\26.png)

## 14.移除文件

```
# 从 Git 仓库和工作区同时移除文件
git rm -f 要移除的文件名称
# 只从 Git 仓库中移除文件，但保留工作区中的文件
git rm --cached 要移除的文件名称
```

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\27.png)

## 15.忽略文件

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\28.png)

## 16.glob模式

![](C:\Users\uu\Desktop\每天学一点\git高级\gitimage\29.png)

## 17. .gitignore 文件的例子

```
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

