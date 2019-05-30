---
layout: post
title: 使用GitHub+Jekyll搭建个人博客
tags:
- Jekyll
- github
categories: 其他
description: 介绍如何使用github和jekyll搭建个人博客
---
# 起点
&emsp;&emsp;最近心血来潮想写博客了，主要也是如果只是看书、看文章根本没法将知识化为己有。期望通过自己写出来以后能够加深印象，再不济也可以方便以后复习之用。  
&emsp;&emsp;要写博客首先要有自己的博客，这篇文章就是将我搭建个人博客的过程记录下来，已备以后查看。同时也将本文作为博客之路的起点吧。  

---
# 使用GitHub+Jekyll搭建个人博客
&emsp;&emsp;在网上查了下搭建个人博客的方法，最终选择了使用GitHub加Jekyll搭建自己的博客网站。原因是首先这种方式相当于把网站托管在GitHub上，不需要担心服务器、流量的问题，其次Jekyll有许多样式好看的模板供选择，不需要自己去写网站代码。既然是要写博客，那就应该把精力放在博客文章的编写上。  
&emsp;&emsp;这种方式搭建个人博客，其实就是将生成的静态网页托管在GitHub上，由GitHub去解析展现，也就是GitHub提供的github pages功能。国内的gitee也有同样的服务。而之所以选择github的原因我也不知道，随机吧。  
&emsp;&emsp;接下来介绍下搭建的步骤。  
## 注册GitHub账号
&emsp;&emsp;既然使用了GitHub那肯定首先需要有GitHub的账号。注册账号的过程就不描述了，登录到[github.com](www.github.com)上注册就行了。  
## 在GitHub上创建仓库
1. New repository  
在github上点击New repository，如下图  
![](index_files/274732471.png)

2. 输入仓库名称，点击创建仓库  
仓库名称的格式应该是要符合 xxx.github.io 这样的。以后xxx.github.io就是博客的地址了。创建完仓库后这个地址就可以访问了，只是里面没有文件，所以会显示404。  
![](index_files/275048045.png)
3. 将仓库clone到本地  
后续将博客文件放入到仓库中push到github上，通过前面的域名就可以访问了。当然文件及目录的格式还是要符合一定规则的。既然是github+Jekyll，那这个规则就属于Jekyll的范畴了。  
## Ruby环境安装
&emsp;&emsp;Jekyll依赖Ruby环境，所以先要在本机安装下Ruby。  
### 安装Ruby
1. 下载[ruby](https://rubyinstaller.org/downloads/)  
按照自己的系统下载相对应的版本即可，不过从我的惨痛经历来看，必须是WITH DEVKIT版本，WITHOUT DEVKIT是不行的！我安装的是Ruby+Devkit 2.5.5-1(x64)。  
2. 安装ruby  
这个没什么好说的，按照提示一直确定下去就可以了。  
安装完成后使用ruby -v和gem -v测试是否安装成功。  
3. 下载[RbuyGems](https://rubygems.org/pages/download)  
下载完成后解压，进入解压后的根目录，执行命令  
`ruby setup.rb`
一说使用rubyinstaller安装Ruby之后都附带了Gems，也就是不需要单独安装RubyGems了，**待测试**。  
## 下载Jekyll
&emsp;&emsp;安装完Ruby后，在命令行执行命令`gem install jekyll`安装完成后就可以创建自己的博客模板了。  
1. 进入想要存放博客文件的目录下执行命令  
`jekyll new myblog`
2. 进入创建好的博客目录  
`cd myblog`
3. 启动服务  
`jekyll serve`
4. 访问博客  
在浏览器输入http://127.0.0.1:4000/即可看到创建好的blog  
## 使用Jekyll主题
&emsp;&emsp;我们在前面创建的自己的博客模板比较简单，也不够美观，我们可以从网上下载自己喜欢的Jekyll主题模板，按照自己的需求做适量改动即可。  
&emsp;&emsp;进入[jekyll主题网站](http://jekyllthemes.org/)，点击自己喜欢的主题进入详情页，可以下载源码，也可以看到演示效果。  
&emsp;&emsp;下载主题后，接口像前面所介绍的方式启动和访问博客。  
**注意**  
&emsp;&emsp;启动博客可能为报错，需要先安装bundle，然后使用bundle启动博客服务。  
1. 安装bundler  
`gem install bundler`
2. 启动博客服务  
`bundler exec jekyll serve`
## 上传自己的博客 ##
&emsp;&emsp;上面步骤完成以后就可以在本地看到博客的效果，但是我们想要的是在线访问博客，这也就是我们一开始创建github仓库的作用。在我们的博客目录下编辑完成博客文章后，推送到github上即可我们创建的仓库名称也就是域名访问到博客了。  
&emsp;&emsp;*Jekyll的目录结构及语法，可以参考[Jekyll官方网站](http://jekyllcn.com/docs/home/)*  


*参考*：  
*1. [Github+Jekyll搭建个人网站详细教程](https://www.jianshu.com/p/9f71e260925d)*  
*2. [jekyll+github搭建个人博客总结](https://www.cnblogs.com/yehui-mmd/p/6286271.html)*  

---
# 后续
&emsp;&emsp;Jekyll中的文件格式是markdown文件，所以自然就需要使用markdown来编辑博客文章。本文也是我第一次编辑md文件，由于对md语法不熟悉，在编辑的过程中需要经常查找教程。所以为了尽快熟悉markdown语法，也为了便于以后使用时参考，我的下一篇博客会是markdown基本语法介绍。  

 

