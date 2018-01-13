---
title: 在其他电脑修改已经创建好的 hexo 项目
categories:
- hexo
- git
tags: [hexo,git,deploy,branch]
---


## 添加 ssh key 到 github 上

### 获取 ssh key

两种方式：

- Git Bash

```bash
$ cat ~/.ssh/id_rsa.pub
```

将内容复制

- git GUI

`Help->Show SSH Key->Copy To Clipboard` 

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnf7pr52fvj20e507hwek.jpg)

### 添加到 github

` setting-> ssh and gpg-> add ssh key` 。title 里随便填个设备名，下面的输入框粘贴我们刚刚复制的内容。最后点击 `add ssh key` 即可添加成功。

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnf7v90zeag20eb08wdsx.gif)

## 克隆仓库到本地

打开 git bash，先把你的项目克隆到本地，两种克隆方式：

- `HTTPS` ：每次提交的时候要输入用户名和密码。
- `SSH` ：添加了 ssh key 到 github 上的话，就不用输入用户名和密码。

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnf7za2nv2j20c00780t1.jpg)

点击右边的小按钮复制链接。然后在 git bash 中输入如下命令：

```bash
$ git clone git@github.com:kinglion580/kinglion580.github.io.git
```

这样就把仓库克隆下来了。

除了 clone ，也可以直接到 `releases` 中去下载需要的版本，然后解压也是可以

## 安装 hexo

首先进入克隆下来的仓库的目录下

```bash
$ cd kinglion580.github.io
```

然后执行：

```bash
$ hexo help
ERROR Local hexo not found in E:\github\kinglion580.github.io
ERROR Try running: 'npm install hexo --save'
```

这个时候是会报错的。我们需要安装 hexo

```bash
$ npm install hexo --save
```

再运行 `hexo help ` 可以看到如下信息：

```bash
$ hexo help
Usage: hexo <command>

Commands:
  clean     Remove generated files and cache.
  config    Get or set configurations.
  deploy    Deploy your website.
  generate  Generate static files.
  help      Get help on a command.
  init      Create a new Hexo folder.
  list      List the information of the site
  migrate   Migrate your site from other system to Hexo.
  new       Create a new post.
  publish   Moves a draft post from _drafts to _posts folder.
  render    Render files with renderer plugins.
  server    Start the server.
  version   Display version information.

Global Options:
  --config  Specify config file instead of using _config.yml
  --cwd     Specify the CWD
  --debug   Display all verbose messages in the terminal
  --draft   Display draft posts
  --safe    Disable all plugins and scripts
  --silent  Hide output on console

For more help, you can use 'hexo help [command]' for the detailed information
or you can check the docs: http://hexo.io/docs/
```

## 安装依赖的插件

在 `package.json` 文件中保存了 hexo 的版本和依赖的软件：

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnf8mpwuj1j20nu0g3q44.jpg)

执行 `npm install` 的时候自动将需要的这些软件都安装上了。

执行 `hexo s` 后，在浏览器输入地址 `localhost:4000` 就可以看到博客了。

除了修改了系统主配置文件 `_config.yml` 需要重新生成启动外，修改其他的文件直接刷新浏览器就可以看到效果。

## 关于推送

首先将源码推送到 github 上（source 分支），然后再使用 hexo 的命令生成且推送到 master 分支上。

在仓库根目录下：

` $` 左边是代表分支，不用输入，只输` $ ` 右边

```bash
source$ git add .
source$ git commit -m 'your descri'
source$ git push origin source
```

将 hexo 生成内容推送到 master 分支：

```bash
$ hexo clean
$ hexo g -d
```

> hexo 默认就是推送到 master 分支上，这个配置在系统主配置文件 `_config.yml` 中：
>
> `deploy` 配置项，想更改分支直接修改 `branch` 值。
>
> ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnf928vg84j20ep043jrl.jpg)
