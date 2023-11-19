## git 命令

当使用 Git 进行版本控制时，通常会涉及一些基本的命令和操作。以下是使用 Git 的基本步骤：

### 1. 安装 Git

首先，确保你已经在计算机上安装了 Git。你可以从[Git官网](https://git-scm.com/)下载并按照安装说明进行安装。

### 2. 创建一个新的仓库

#### 在现有项目中初始化仓库：

```bash
cd /path/to/your/project
git init
```

#### 或者克隆现有仓库：

```bash
git clone <repository_url>
```

### 3. 添加和提交更改

#### 添加所有更改到暂存区：

```bash
git add .
```

#### 添加指定文件到暂存区：

```bash
git add filename
```

#### 提交更改到本地仓库：

```bash
git commit -m "你的提交信息"
```

### 4. 查看状态和历史

#### 查看文件状态：

```bash
git status
```

#### 查看文件修改的具体内容：

```bash
git diff
```

#### 查看提交历史：

```bash
git log
```

### 5. 分支操作

#### 创建新分支：

```bash
git branch branch_name
```

#### 切换分支：

```bash
git checkout branch_name
```

#### 创建并切换到新分支：

```bash
git checkout -b new_branch_name
```

#### 合并分支：

```bash
git merge branch_name
```

### 6. 远程仓库操作

#### 添加远程仓库：

```bash
git remote add origin <repository_url>
```

#### 推送到远程仓库：

```bash
git push -u origin master
```

#### 从远程仓库拉取：

```bash
git pull origin master
```

### 7. 其他常用操作

#### 撤销工作区的修改：

```bash
git checkout -- filename
```

#### 撤销暂存区的修改：

```bash
git reset filename
```

#### 撤销最后一次提交：

```bash
git reset HEAD~1
```

这只是 Git 的基础使用方法，还有很多高级功能和选项。使用 `git --help` 可以查看 Git 的帮助文档，或者查阅[Pro Git书籍](https://git-scm.com/book/zh/v2)以获取更深入的理解。
