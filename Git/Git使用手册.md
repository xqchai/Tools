# Git使用手册

下载--安装--初始配置略

```
$ git help git	//打开本地帮助文档
```

### Commit提交

在目标文件夹右键-显示更多选项-open git bush here

```
$ git init	//在该文件夹创建仓库，文件夹中多了一个.git文件（可能是隐藏文件）
```

```
$ git status	//查看仓库状态，绿色为已上传
```

```
$ git add 文件名	//把文件夹中的该文件上传暂存区
```

```
$ git add .		//把该目录下所有文件上传暂存区
```

```
$ git commit -m message	
//提交此次变更到本地仓库，message为文字描述，只提交绿色的已上传的文件, 会生成唯一的commitID
```

```
$ git log		//查看日志
```

```
$ git reset <filename>	//commit之前将绿色的文件重新变成红色的
```

即必要的操作为 add -> commit

### 文件状态

1.没有被add过的文件叫untracked
2.add之后文件处于staged状态等待commit
3.commit之后文件处于unmodified这里之所以是modified是因为文件会跟仓库中的文件对比
4.当unmodified的文件被修改则会变为modified状态
5.modified之后的文件add之后将继续变为staged状态
6.unmodifed的文件还有一种可能是已经不再需要了，那么可以remove它不再追踪变为untracked状态

### Alias别名

打开git安装目录C:\Program Files\Git\etc 找到gitconfig文件，编辑即可

![image-20230920113249883](C:\Users\xqchai\AppData\Roaming\Typora\typora-user-images\image-20230920113249883.png)

设置自己喜欢的别名来代替原生命令，比较好记



### 常用命令

```
$ clear		//清屏
```

```
$ git reset commitID	//将现有文件恢复至commitID对应的提交版本
//后缀加--hard: 不保留所有变更
//后缀加--soft: 保留变更且变更内容处于Staged
//后缀加--mixed: 保留变更且变更内容处于Modified
```

```
$ git reflog	//查看所有的操作记录，commitID前7位和全部是一样的
```



### Branch分支

生成仓库时默认生成master主分支

```
$ git checkout -b name template	
//创建新分支，name为新分支名字，template为以哪个分支为模板，不写默认为当前分支
```

```
$ git branch	//查看所有分支
```

```
$ git checkout branchName	//直接切换分支
```

```
$ git fetch		//从服务器上拉取数据
```



### Merge合并

```
$ git merge branchName	//合并分支变更
```



### Clone克隆

```
$ git clone 仓库地址
```

```
$ git push --setup-stream	//新切的分支，设置上流分支
```

```
$ git push	//提交到云端仓库
```



### Rebase变基

待补充