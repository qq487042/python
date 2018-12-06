# python

#### 项目介绍
学习Python的笔记，收录的一些代码段

#### 描述
学习python,第一个使用git的东西，刚开始使用的是GITHUB,国内吧，就使用码云。

#### 使用码云操作流程:
1. 先在码云上创建一个库，比如：`python`

2. 本地新建一个文件夹用来存放代码，比如：`python`

3. 初始化本地库，先`cd`到`python`：`git init`

4. 本地生成ssh-key,查看是否有：`$ cd ~/.ssh`，如果没有这个文件夹，则生成：`$ ssh-keygen`

5. 复制KEY到码云个的设置-安全设置-SSH公钥：`$ cat ~/.ssh/id_rsa.pub`

6. 设置远程仓库地址：`git remote add origin https://gitee.com/用户个性地址/python.git`

7. 拉取远程仓库文件：`git pull origin master`

8. 上传文件到远程仓库：`git push origin master`

9. 以下一些git常用操作命令：

```
1. 查看文件状态：git status
2. 查看远程仓库有哪些：git remote -v
3. 删除不要的远程仓库：git remote rm 远程仓库名
4. 回退版本：git reset --hard 版本号
```

[爱css](https://icss.me)

> 每多学一点知识，就少写一行代码
