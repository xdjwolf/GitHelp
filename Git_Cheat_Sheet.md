# Git 常用命令速查表

\\\ Git Cheat Sheet < CN > (#Version 0.1)

> [PDF 版本下载](https://gitcafe.com/GitCafe/Help/raw/master/Git/PDF_Docs/Git_Cheat_Sheet.pdf) / [PNG图片下载](https://gitcafe.com/GitCafe/Help/raw/master/Git/PDF_Docs/Git_Cheat_Sheet.png)

---

### 创建版本库

* `$ git clone <url>` #克隆远程版本库
* `$ git init` #初始化本地版本库

### 修改和提交

* `$ git status` #查看状态
* `$ git diff` #查看变更内容
* `$ git add .` #跟踪所有改动过的文件
* `$ git add <file>` #跟踪指定的文件
* `$ git mv <old> <new>` #文件改名
* `$ git rm <file>` #删除文件
* `$ git rm --cached <file>` #停止跟踪文件但不删除
* `$ git commit -m “commit message”` #提交所有更新过的文件
* `$ git commit --amend` #修改最后一次提交

### 查看提交历史

* `$ git log` #查看提交历史

* `$ git log -p <file>` #查看指定文件的提交历史

* `$ git blame <file>` #以列表方式查看指定文件的提交历史

### 撤消

* `$ git reset --hard HEAD` #撤消工作目录中所有未提交文件的修改内容
* `$ git checkout HEAD <file>` #撤消指定的未提交文件的修改内容
* `$ git revert <commit>` #撤消指定的提交

### 分支与标签

* `$ git branch` #显示所有本地分支
* `$ git checkout <branch/tag>` #切换到指定分支或标签
* `$ git branch <new-branch>` #创建新分支
* `$ git branch -d <branch>` #删除本地分支
* `$ git tag` #列出所有本地标签
* `$ git tag <tagname>` #基于最新提交创建标签
* `$ git tag -d <tagname>` #删除标签

### 合并与衍合

* `$ git merge <branch>` #合并指定分支到当前分支
* `$ git rebase <branch>` #衍合指定分支到当前分支

### 远程操作

* `$ git remote -v` #查看远程版本库信息
* `$ git remote show <remote>` #查看指定远程版本库信息
* `$ git remote add <remote> <url>` #添加远程版本库
* `$ git fetch <remote>` #从远程库获取代码
* `$ git pull <remote> <branch>` #下载代码及快速合并
* `$ git push <remote> <branch>` #上传代码及快速合并
* `$ git push <remote> :<branch/tag-name>` #删除远程分支或标签
* `$ git push --tags` #上传所有标签
