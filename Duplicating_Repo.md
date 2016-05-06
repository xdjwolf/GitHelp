### 复制版本库

如果你不想派生项目，而只是想复制一份相同的源代码，或者想从别的 Git 托管服务那里复制一份源代码到 GitCafe 上的话，可以通过以下步骤来操作。

1). 从原地址克隆一份裸版本库，当然你也可以把托管于其它 git 服务器上的版本库克隆下来。

`git clone --bare git://gitcafe.com/username/project.git`

2). 然后到 GitCafe 服务器上[创建一个新项目][newproject]。

3). 以镜像推送的方式上传代码到 GitCafe 服务器上。

`cd project.git`

`git push --mirror git@gitcafe.com/username/newproject.git`

4). 删除本地代码

`cd ..`

`rm -rf project.git`

[newproject]:https://gitcafe.com/projects/new
