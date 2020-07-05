## 1. 为什么要使用 Git & GitHub

## 2. 什么是版本控制？

## 3. 安装 Git、初始化仓库并做最简单的配置

```
git --version
```

```
mkdir learn_git
```

```
cd learn_git
```

```
ls -al
```

```
git init
```

```
ls -al
```

```
git config --global user.name "wuyong"
```

```
git config --global user.email wuyong@fastmail.com
```

```
git config --global --list
```

## 4. 在 Windows 系统上安装 Git

## 5. 完成一个最简单的 Git 操作流程：工作区、暂存区和仓库

```
git status
```

```
pwd
```

```
git status
```

```
git add learn_git.html
```

```
git status
```

```
git commit -m "create learn_git.html"
```

```
git status
```

```
git add .
```

```
git status
```

```
git commit -m "web1.0"
```

```
git add learn_git.html
```

```
git commit -m "web2.0"
```

```
git log
```

## 6. 将本地仓库同步到远程 GitHub 仓库

HTTPS

```
https://github.com/wuyong/learn_git.git
```

SSH

```
git@github.com:wuyong/learn_git.git
```

…or create a new repository on the command line

```
echo "# learn_git" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

…or push an existing repository from the command line

```
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

### Checking for existing SSH keys

```
ls -al ~/.ssh
```

### Generating a new SSH key and adding it to the ssh-agent

```
ssh-keygen -t rsa -b 4096 -C "wuyong@fastmail.com"
```

```
eval "$(ssh-agent -s)"
```

```
open ~/.ssh/config
```

```
touch ~/.ssh/config
```

```
open ~/.ssh/config
```

```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

```
ssh-add -K ~/.ssh/id_rsa
```

### Adding a new SSH key to your GitHub account

```
pbcopy < ~/.ssh/id_rsa.pub
```

### Testing your SSH connection

```
ssh -T git@github.com
```

### push an existing repository from the command line

```
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

```
git add learn_git.html
```

```
git commit -m "web3.0"
```

```
git push -u origin master
```

```
git log
```
