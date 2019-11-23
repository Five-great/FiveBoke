---
title: 同时部署coding与github
date: 2018-09-28 11:43:55
top: true
img:
categories: 前端
tags: 
   - Hexo
---
    
# 前言
之前我是把hexo托管在github，但是毕竟github是国外的，访问速度上还是有点慢，所以想也部署一套在国内的托管平台，
所以就决定部署到coding。 查询了多方资料，终于鼓捣出了本地一次部署，同时更新到github以及coding。
##### 具体过程如下：
 ##### 一·注册
   先注册好[coding](https://coding.net) 和 [github](https://github.com)
 
 ##### 二·创建仓库
    这里只介绍coding上面如何创建项目，以及把本地hexo部署到coding上面，
	还不懂如何创建hexo的,百度很多。首先我们创建一个项目，创建后进入项目的代码模块，获取到这个项目的ssh地址，
	我的是 https://git.coding.net/five-great/five-great.git
 
 ##### 三·同步本地hexo到coding上
    把获取到了ssh配置在上面的_config.yml文件中的deploy下，如果是第一次使用coding的话，需要设置SSH公钥，
	生成的方法可以参考coding帮助中心
如果


本地打开 id_rsa.pub 文件，复制其中全部内容，填写到SSH_RSA公钥key下的一栏，公钥名称可以随意起名字。完成后点击“添加”，
然后输入密码或动态码即可添加完成。没有的话先生成，如何生成百度好了。

添加后，在git bash命令输入：

ssh -T git@git.coding.net
如果得到下面提示就表示公钥添加成功了：

Coding.net Tips : [Hello ! You've conected to Coding.net by SSH successfully! ]

 ##### 四·配置_config.yml
  在Hexo根目录下_config.yml文件中的deploy如下
根据Hexo官方文档需要修改成下面的形式

  ```git
  deploy:
  type: git
  message: [message]
  repo:
    github: <repository url>,[branch]
    coding: <repository url>,[branch]
 ```
  
  我的为
    
	```git
     deploy: 
     type: git
     repo:
       github: git@github.com:Five-great/Five-great.github.io.git #SSH形式
       coding: https://git.coding.net/five-great/five-great.git   #http形式
       branch: master 
    ```
	
##### 五·pages服务方式部署
   部署博客方式有两种，第一种就是pages服务的方式，也推荐这种方式，因为可以绑定域名，而第二种演示的方式必须升级会员才能绑定自定义域名。pages方式也很简单
就是在source/需要创建一个空白文件，至于原因，是因为 coding.net需要这个文件来作为以静态文件部署的标志。就是说看到这个Staticfile就知道按照静态文件来发布。

 ```git
 cd source/
 touch Staticfile  #名字必须是Staticfile
 ```
 
分支选择master，因为前面配置的分支是master,因此开启之后，也需要是master。然后看起之后就可访问了。

注意：
如果你的项目名称跟你coding的用户名一样，比如我的用户是叫tengj,博客项目名也叫tengj
那直接访问 tengj.coding.me就能访问博客，否则就要带上项目名：tengj.coding.me/项目名 才能访问
推荐项目名跟用户名一样，这样就可以省略项目名了



  最后使用部署命令就能把博客同步到coding上面：
  
 ```git
 hexo c
 hexo g
 hexo d
 ```


  我的博客：
   github: https://five-great.github.io/
   coding: https://five-great.coding.me/