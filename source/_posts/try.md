title: 在自己服务器上做git
date: 2014-07-18 04:19:10
tags: git
category: git

---
之前一直没有在自己服务器上建git，以为很复杂。。。看了眼之后发现还挺简单，这样维护起来就方便多啦


* 首先要建立一个bare的仓库
* 建立一个工作区的文件夹，在仓库外
* 在hooks/post-receive	

		!/bin/sh
		GIT_WORK_TREE=～/mywebsit git checkout -f
* 把本地内容push到该仓库中

接下来就能自动更新了！