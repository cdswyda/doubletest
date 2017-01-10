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


> 其他情况暂未尝试, 可查看[https://app.yinxiang.com/shard/s72/nl/16907507/fc6f1003-7810-4cc1-b665-fc8cdaacc026](https://app.yinxiang.com/shard/s72/nl/16907507/fc6f1003-7810-4cc1-b665-fc8cdaacc026)
