# 装机必备工具



## Github

每次`git push`都需要输入账号密码？不妨使用下面的方法:

下面命令会将下次弹框的账号和密码保存起来，永久使用。

``` git
git config --global credential.helper store
```

如果想要清除该账号和密码，使用如下命令：

```
git config --global credential.helper reset
```

想要临时存储（默认15min），使用如下命令

``` git
git config --global credential.helper cache
```

windows下的临时存储命令不是上面的，应该使用下面的命令:  

``` git
git config --global credential.helper wincred
```

