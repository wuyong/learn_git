## 1. 为什么要使用 Git & GitHub

## 2. 什么是版本控制？

## 3. 安装 Git、初始化仓库并做最简单的配置

```bash
git --version
```

```bash
mkdir learn_git
```

```bash
cd learn_git
```

```bash
ls -al
```

```bash
git init
```

```bash
ls -al
```

```bash
git config --global user.name "wuyong"
```

```bash
git config --global user.email wuyong@fastmail.com
```

```bash
git config --global --list
```

## 4. 在 Windows 系统上安装 Git

## 5. 完成一个最简单的 Git 操作流程：工作区、暂存区和仓库

```bash
git status
```

```bash
pwd
```

```bash
git status
```

```bash
git add learn_git.html
```

```bash
git status
```

```bash
git commit -m "create learn_git.html"
```

```bash
git status
```

```bash
git add .
```

```bash
git status
```

```bash
git commit -m "web1.0"
```

```bash
git add learn_git.html
```

```bash
git commit -m "web2.0"
```

```bash
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

```bash
echo "# learn_git" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

…or push an existing repository from the command line

```bash
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

### Checking for existing SSH keys

```bash
ls -al ~/.ssh
```

### Generating a new SSH key and adding it to the ssh-agent

```bash
ssh-keygen -t rsa -b 4096 -C "wuyong@fastmail.com"
```

```bash
eval "$(ssh-agent -s)"
```

```bash
open ~/.ssh/config
```

```bash
touch ~/.ssh/config
```

```bash
open ~/.ssh/config
```

```bash
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

```bash
ssh-add -K ~/.ssh/id_rsa
```

### Adding a new SSH key to your GitHub account

```bash
pbcopy < ~/.ssh/id_rsa.pub
```

### Testing your SSH connection

```bash
ssh -T git@github.com
```

### push an existing repository from the command line

```bash
git remote add origin git@github.com:wuyong/learn_git.git
git push -u origin master
```

```bash
git add learn_git.html
```

```bash
git commit -m "web3.0"
```

```bash
git push -u origin master
```

```bash
git log
```
