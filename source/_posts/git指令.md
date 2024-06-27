---
title: git
date: 2024-06-27
tages:
---

# git

## gitconfig设置

```
~/.gitconfig
[user]
	email = 
	name =
[color]
	ui = auto
```

## ssh配置

```
ssh-keygen -t rsa -C "xxx@xxx.com"  // 生成ssh
// 执行后一直回车即可
cd ~/.ssh
cat id_rsa.pub                      // 获取ssh key公钥内容
// Github账号上添加公钥
ssh -T git@github.com               // 验证是否设置成功
```

## 本地仓库初始化

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin 远程仓库地址
git push -u origin main
```

## git指令

### 检查改动

```
// 检查工作目录中的改动
git diff <file1> [<file2>...]
// 检查提交历史
git log --graph --decorate [--oneline]
// 回顾历史中的一次改动
git show <commit_hash>
```

### 撤销改动

```
// 回退某一版本，并保留staging index中的内容
git reset --soft <commit_hash>
// 把staging index的改动撤回working tree
git reset HEAD <file1> [<file2>...]
```

### 分支操作

```
// 查看分支
git branch
// 创建分支
git branch <name>
// 切换分支
git checkout <name>
// 删除分支
git branch -d <name>
// 分支合并
git merge <合并分支名>
// 解决合并冲突
git status
```

### 远端操作

```
git remote add origin 远程仓库地址
// 显示链接的所有远端
git remote -v
// 删除其中一个远端
git remote remove <name>
// 首次上传
git push -u origin <branch_name>
// 删除远端branch
git branch -r -d <branch_name>
```

### 其他

```
// 给一个提交打上标签
git tag -a <tagname> <commit_hash>
// 暂存本地未提交改动
git stash
git stash pop
// 抵消前面某次提交commit
git revert <commit>
// 二分法找错
git bisect
```



