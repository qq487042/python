# python

#### 项目介绍
学习web的笔记，收录的一些代码段

#### 描述
学习web,第一个使用git的东西，刚开始使用的是GITHUB,国内吧，就使用码云，现在使用阿里云。

#### 使用码云操作流程:
1. 先在码云上创建一个库，比如：`python`

2. 本地新建一个文件夹用来存放代码，比如：`python`

3. 初始化本地库，先`cd`到`python`：`git init`

4. 本地生成ssh-key,查看是否有：`$ cd ~/.ssh`，如果没有这个文件夹，则生成：`$ ssh-keygen -t rsa -C "xxx@xxx.com"`，在终端添加SSH信任：`ssh -T git@gitee.com`

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
5. 查看配置：git config --list
6. 配置user.name ：git config --global user.name "阿乞云计算"
7. 配置user.email: git config --global user.email "xxx@xxx.com"
```
# 关于SSH keys

SSH key 可以让你在你的电脑和Code服务器之间建立安全的加密连接。 先执行以下语句来判断是否已经存在本地公钥：

``` 
cat ~/.ssh/id_rsa.pub 
```

如果你看到一长串以 ssh-rsa或 ssh-dsa开头的字符串, 你可以跳过 ssh-keygen的步骤。

提示: 最好的情况是一个密码对应一个ssh key，但是那不是必须的。你完全可以跳过创建密码这个步骤。请记住设置的密码并不能被修改或获取。

你可以按如下命令来生成ssh key：

```
ssh-keygen -t rsa -C "487042@qq.com"
```

这个指令会要求你提供一个位置和文件名去存放键值对和密码，你可以点击Enter键去使用默认值。

用以下命令获取你生成的公钥：

```
cat ~/.ssh/id_rsa.pub
```
# 一个本地库关联多个github库

使用多个远程库时，我们要注意，git给远程库起的默认名称是`origin`，如果有多个远程库，我们需要用不同的名称来标识不同的远程库。

仍然以`python`本地库为例，我们先删除已关联的名为`origin`的远程库：

```
git remote rm origin
```

然后，先关联`GitHub`的远程库：

```
git remote add github git@github.com:michaelliao/python.git
```

注意，远程库的名称叫`github`，不叫`origin`了。

接着，再关联码云的远程库：

```
git remote add gitee git@gitee.com:liaoxuefeng/python.git
```

同样注意，远程库的名称叫`gitee`，不叫`origin`。

现在，我们用`git remote -v`查看远程库信息，可以看到两个远程库：

```
git remote -v
gitee    git@gitee.com:liaoxuefeng/python.git (fetch)
gitee    git@gitee.com:liaoxuefeng/python.git (push)
github    git@github.com:michaelliao/python.git (fetch)
github    git@github.com:michaelliao/python.git (push)
```

如果要推送到GitHub，使用命令：

```
git push github master
```

如果要推送到码云，使用命令：

```
git push gitee master
```

这样一来，我们的本地库就可以同时与多个远程库互相同步


[爱css](https://icss.me)

> 每多学一点知识，就少写一行代码
