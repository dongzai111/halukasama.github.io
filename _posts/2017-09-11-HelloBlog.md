---
layout:     post
title:      "Hello Blog"
subtitle:   ""
date:       2017-09-11 12:00:00
author:     "Wjl"
header-img: "img/post_helloblog.jpg"
catalog: true
tags:
  - Test
---

> "面向搜索引擎"编程的日子  
感谢，公司的前辈，google，
豆子的[Qt学习之路](https://www.devbean.net/)以及[鸟哥的私房菜](http://linux.vbird.org/)CSDN博客众，[StackExchange](https://stackexchange.com/)系列网站的大佬,
使我长时间受益于从分享经验中获取知识，解决问题．  
"想成为那样的人"这样的念头也在心里渐渐生根发芽．

我的记性不算太好
有些事不记下来，就担心明天忘掉，  
笔记与其说是加深记忆，还不如说是让自己有安全感．  
来到这里，我扔了小本子，跟着大佬开启了共享文档+gitLab+邮件列表的协作模式．  
要离开了，未来还是一个未知数,索性就把自己的点滴全数搬到这里．  
闲言少叙，现在将搭建github静态博客的过程录入吧．

# 1. Local Env  
下载ruby源码  
[下载地址](https://www.ruby-lang.org/en/downloads)  
```Bash
tar xvf ruby-2.3.4.tar.gz
cd ruby-2.3.4
./configure --preifx="yourinstalldir"
make
sudo make install
```
gem也被打包安装,执行
```
gem install jekyll
```
测试
```Bash
jekyll new blog
cd blog
jekyll serve
```
浏览器访问127.0.0.1:4000  
如果有默认界面，代表成功
[其他安装方式](http://jekyllrb.com.cn/docs/quickstart/)
# 2. GitHub Page
登录github  
创建名为：youname.github.io的repository  
clone下来  
去网上下载一个基于jekyll并且你喜欢的主题  
有前端经验的这里可以自由发挥了  
解压并进入该目录，执行
```
jekyll build
```
编译完成后执行
```
jekyll serve
```
打开浏览器刷新你的127.0.0.1:4000，成功的话你下载的主题可以正常显示
最后将其提交到刚才新建的repository, push之前可以添加ignore文件忽略＿site  
[详细指南](http://jekyllrb.com/docs/github-pages/)

至此，blog就初步完成了，访问youname.github.io看看吧
写blog之前建议先了解一下[jekylldocs](http://jekyll.com.cn/docs/home)中的
编辑内容部分
