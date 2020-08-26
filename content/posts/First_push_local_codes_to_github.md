---
title: "首次将本地代码库推送到github方法"
date: 2020-08-26T16:51:28+08:00
draft: true
---
# 场景
即从本地开发了一个项目，因项目合规需要，需要保存在github进行版本管理。

# 步骤
1. 本地代码有进行git格式化（有则跳过）
```
git init 
```

2. 远端新建一个仓库。

3. 在本地主目录，进行远程仓库关联。
```
git remote add origin https://github.com/arthaszyb/myHUGO.git
```
在这条命令中，git会自动将远程仓库的名字设置为origin，方便我们的后续操作。

4. 更新提交本地文件
```
git add .
git commit -m "xxx"
```

5. 推送到远程仓库
推送到master分支
假设我想将本地master分支上的内容推送到远程master分支上，方式如下：
```
git push -u origin master
```
-u参数可以在推送的同时，将origin 仓库的master 分支设置为本地仓库当前分支的upstream（上游）。添加了这个参数，将来运行git pull命令从远程仓库获取内容时，本地仓库的这个分支就可以直接从origin 的master 分支获取内容，省去了另外添加参数的麻烦。这个参数也只用在第一次push时加上，以后直接运行git push命令即可。

至此，本地代码应该同步到了远端了。
