# 测试同时推送到两个仓库

## 两个空仓库的情况下
直接修改`.git/config`文件即可。

在执行 ` git remote add origin git@github.com:cdswyda/doubletest.git` 之后查看文件

```
[remote "origin"]
	url = git@github.com:cdswyda/doubletest.git
	url = git@git.coding.net:cdswyda/doubletest.git
	fetch = +refs/heads/*:refs/remotes/origin/*
```

原本文件中只有一个url，第二个是新添加的。

之后进行正常的提交操作即可。


> 其他情况暂未尝试, 可查看[http://note.youdao.com/share/?id=b53801ca4e44f48ba50bda7a2d264d8f&type=note#/](http://note.youdao.com/noteshare?id=b53801ca4e44f48ba50bda7a2d264d8f&sub=wcp1484049030830411)
