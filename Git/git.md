## 设置签名

### 全局

git config --global user.name shi

git config --global user.email shi

## 版本记录

git log

git log --pretty=oneline 以一行显示

git log --oneline 更简洁版

gti reflog 

## 版本前进后退

- 基于索引

  git reset --hard hash

- 用^

  git reset --hard HEAD^^^

- 用~

  git reset --hard HEAD~3

## 文件比较

git diff [file name]

不带文件名可以比较多个文件

# 版本分支

## 查看分支

git branch -v

## 创建分支

git branch name

## 切换分支

git checkout branchName

## 分支合并

1. 切换到master分支
2. git merge branchName

# 本地远程交互

## 远程仓库别名

1. 查看远程仓库别名

   git remote -v

2. 设置远程仓库别名

   git remote add [alis] https/ssh.git

## 推送

git push [alis] [branch]

## SSH免密登陆

1. ssh-keygen -t rsa -C gitAccount
2. cd ~/.ssh 文件里面会生成两个密钥
3. 复制公钥到github账户















