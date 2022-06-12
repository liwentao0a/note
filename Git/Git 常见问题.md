# Git 常见问题

## OpenSSL SSL_read: Connection was reset, errno 10054

Git Bash 中，push 时，出现错误

```shell
git push -u origin main
OpenSSL SSL_read: Connection was reset, errno 10054 ...
```

### 解决方案

1. 邮箱问题

    查看用户名，邮箱

    ```shell
    git config user.name
    git config user.email
    ```

    修改，用户名，邮箱

    ```shell
    git config --global user.name "xxx"
    git config --global user.email "xxx"
    ```

    移除仓库，重新添加

    ```shell
    git remote rm origin
    git remote add origin https://github.com/XXX
    ```

2. 解除SSL认证

    在 Git Bash 中输入以下命令：

    ```shell
    git config --global http.sslVerify "false"
    ```

3. 更新 DNS 缓存

    cmd 窗口输入

    ```shell
    ipconfig /flushdns
    ```

4. 文件过大，超过上限

    修改为 500MB，在 Git Bash 中输入以下命令：

    ```shell
    git config http.postBuffer 5242880003
    ```

### 小结

多数情况下国内访问 Github 会被…，或因网络波动问题推送失败。推荐使用 SSH 方式拉去代码或者参考开源项目修改本机 hosts 文件解决访问问题