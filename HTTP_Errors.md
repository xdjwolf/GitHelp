# HTTP Errors

如果你在使用 HTTP 协议进行 Git 操作的时候出现错误提示：

* 401 错误：

    $ git push origin master
    error: RPC failed; result=22, HTTP code = 401
    fatal: The remote end hung up unexpectedly
    fatal: The remote end hung up unexpectedly
    Everything up-to-date

* 403 错误：

    $ git push origin master
    error: RPC failed; result=22, HTTP code = 401
    fatal: The remote end hung up unexpectedly
    fatal: The remote end hung up unexpectedly
    Everything up-to-date

有以下几个可能性：

1. Git 版本过低。GitCafe 推荐使用的 Git 版本是 >= 1.7，请参考[这里](http://git.gitcafe.com/downloads)获取最新版本。

    $ git --version
    git version 1.8.2.1

2. 远程仓库路径设置错误。注意，GitCafe 对于路径的识别是大小写敏感的。

    查看已有的远程仓库：

        $ git remote -v
        origin  https://gitcafe.com/GitCafe/help.git (fetch)
        origin  https://gitcafe.com/GitCafe/help.git (push)

    设置新的远程仓库路径：

        $ git remote set-url origin https://gitcafe.com/GitCafe/Help.git

    查看新的远程仓库路径：
    
        $ git remote -v
        origin  https://gitcafe.com/GitCafe/Help.git (fetch)
        origin  https://gitcafe.com/GitCafe/Help.git (push)

3. 对该仓库没有访问权限。检查你是否对目标仓库有相应的读写权限。

4. 输入了错误的用户名和密码。检查你是否使用了对该仓库有写权限的正确的账户名称和密码，检查是否对所有你名下的仓库均不能访问。

如果以上检查都没能帮到您，请到[这里给我们反馈][feedback]，或直接发送邮件到 [support@gitcafe.com](support@gitcafe.com) ，我们会及时做出响应。
