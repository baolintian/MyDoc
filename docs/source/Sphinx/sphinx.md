# 说明文档管理工具Sphinx

`Sphinx`类似于`Mkdocs`工具，是一个生成说明文档的管理工具。

使用的过程：

1. 在本地用Sphinx生成相应的工程文件结构，并且可以进行构建预览
2. 用github建立相关的repo，将工程文档上传
3. 注册[ReadtheDoc](<https://readthedocs.org/>)，关联相关的仓库，建立webhook，等待自动的构建

## 安装

1. 生成目录文件的时候，可以参考[使用readthedoc建立说明文档](<https://www.xncoding.com/2017/01/22/fullstack/readthedoc.html>)

假设目前在/repo目录下，先安装好python

```
pip install sphinx sphinx-autobuild sphinx_rtd_theme
```

2. 在本地搭建好相关的环境之后，建议直接使用下面的[模板](<https://github.com/baolintian/MyDoc/tree/d06e3d9d48aba21365092c1ce5f7fac7d99055e3>)，因为这个没有什么坑只要改改`conf.py`里面的参数就可以了。（这里面我遇到了很多的坑，比如如果有`.readthedoc.yml`，会需要`contents.rst`和python`requirements.txt`文件，`latex`不能正确的构建环境等等，最后是用了别人的一个模板，然后修改了相关的配置参数就成功了。至今仍然不明白为什么latex构建的环境是失败的。）
3. 上传github
4. ReadtheDoc关联仓库，并且自动的构建



## 说明

1. Sphinx使用`.rst`格式能够获得最佳的书写体验，但是可能需要一定的学习的成本，同时也是支持markdown格式进行文档的书写

2. 本地使用`make html`只能生成静态的`html`文件，需要手动的找到文件，并打开，并不像`mkdocs`一样。

## 拓展阅读

[官方文档](<https://docs.readthedocs.io/en/latest/webhooks.html>)

