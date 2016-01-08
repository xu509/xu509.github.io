---
layout: post
title: 使用Github pages,jekyll搭建个人博客
date:   2016-01-08 16:30:59 +0800
category: github
tags: jekyll githubPages
---

#使用Github pages,jekyll搭建个人博客
花了一天搭起了这个博客，在这儿做记录。

我把整个搭建过程分为5个步骤：

- github上创建Repository
- Repostory上创建CNAME文件， 将个人域名进行解析
- 安装jekyll以及必须的软件
- 上传一篇新的文章

接下来依次来详解各个步骤。

---

##1 github上创建Repository
首先，创建一个库，库名为 username.github.io
![例图](https://pages.github.com/images/user-repo@2x.png)

> **注意**：username必须和你的用户名一样，例如我是xu509，则资源名必须为xu509.github.io

使用git将项目克隆到本地，具体不再赘述。

[参考链接](https://pages.github.com/)

---

##2 创建CNAME文件，将个人域名进行解析

项目根目录中，添加CNAME文件，并且添加你准备使用的域名。比如我使用的是二级域名，则：
![创建CNAME]({{site.url}}/assets/2016-01-08-setupblog/2.png)

进入域名解析，将需要解析的域名cname指向username.github.io.
![域名解析]({{site.url}}/assets/2016-01-08-setupblog/1.png)

> **注意**：文件名必须为**CNAME**，域名的指向**username.github.io.**中的**.**不要遗漏

至此，打开次级域名应已能链接至github page。

[参考链接](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/)

---

##3 安装jekyll以及相关必须软件

首先需要安装ruby，[ruby官网](https://www.ruby-lang.org/zh_cn/)

安装RubyGems,[RubyGems地址](https://rubygems.org/pages/download)

> **注意**: RubyGems通过命令台 ruby setup.rb进行安装

通过RubyGems安装jekyll:

`
  gem install jekyll
`
[jekyll安装参考链接](http://jekyllrb.com/docs/installation/)


安装完成后，使用jekyll命令
`
~: jekyll new myblog
~: cd myblog
~/myblog:  jekyll serve
`

这时候，就可以通过 http://localhost:4000看到jekyll模版了。
[参考](http://jekyllrb.com/docs/quickstart/)

---

##4 上传第一篇博文
myblog的目录_posts下存储的就是博文，可直接复制一篇后，就能在本机看到效果。具体的jekyll编写规则需查阅官网：http://jekyll.bootcss.com/docs/posts/。

一切就绪后，将根目录直接提交至github，就大功告成！。

这是我的github page项目地址：https://github.com/xu509/xu509.github.io
