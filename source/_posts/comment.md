---
title: 添加评论
categories:
- hexo
- comment
tags: [hexo,comment,gitment,valine]
---

## gitment

待补

## valine

- [valine github](https://github.com/xcss/Valine)
- [valine 说明文档](https://valine.js.org/#/)

1. valine 基于 leancloud ，先要注册一个 leancloud 账号 [点击这里注册](https://leancloud.cn/dashboard/login.html#/signup)

2. 然后 [创建应用](https://leancloud.cn/dashboard/applist.html#/newapp)

3. 选择刚刚创建的`应用`>`设置`>选择`应用 Key`

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnfa98p9j3j20930c174s.jpg)

4. 在安全中心配置安全域名 `https://kinglion580.github.io` 

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnfaesgcoij207706d74a.jpg)

5. 修改系统配置文件 `_config.yml` 的配置 `valine `  ，具体配置参见 https://valine.js.org/#/configuration
