<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [推荐阅读](#%E6%8E%A8%E8%8D%90%E9%98%85%E8%AF%BB)
- [Releases](#releases)
  - [关于 releases](#%E5%85%B3%E4%BA%8E-releases)
    - [限制](#%E9%99%90%E5%88%B6)
  - [创建 release](#%E5%88%9B%E5%BB%BA-release)
    - [从 tag 创建](#%E4%BB%8E-tag-%E5%88%9B%E5%BB%BA)
    - [发布本地的包](#%E5%8F%91%E5%B8%83%E6%9C%AC%E5%9C%B0%E7%9A%84%E5%8C%85)
- [Tag](#tag)
  - [列出标签](#%E5%88%97%E5%87%BA%E6%A0%87%E7%AD%BE)
  - [创建标签](#%E5%88%9B%E5%BB%BA%E6%A0%87%E7%AD%BE)
    - [附注标签](#%E9%99%84%E6%B3%A8%E6%A0%87%E7%AD%BE)
    - [轻量标签](#%E8%BD%BB%E9%87%8F%E6%A0%87%E7%AD%BE)
  - [推送标签](#%E6%8E%A8%E9%80%81%E6%A0%87%E7%AD%BE)
    - [单个](#%E5%8D%95%E4%B8%AA)
    - [多个](#%E5%A4%9A%E4%B8%AA)
- [Wikis](#wikis)
  - [关于 wikis](#%E5%85%B3%E4%BA%8E-wikis)
  - [通过在线界面添加维基页面](#%E9%80%9A%E8%BF%87%E5%9C%A8%E7%BA%BF%E7%95%8C%E9%9D%A2%E6%B7%BB%E5%8A%A0%E7%BB%B4%E5%9F%BA%E9%A1%B5%E9%9D%A2)
  - [搜索](#%E6%90%9C%E7%B4%A2)
- [issue](#issue)
  - [从 milestones 新建 issue](#%E4%BB%8E-milestones-%E6%96%B0%E5%BB%BA-issue)
  - [从 projects 新建 issue](#%E4%BB%8E-projects-%E6%96%B0%E5%BB%BA-issue)
- [milestones](#milestones)
  - [创建一个 milestones](#%E5%88%9B%E5%BB%BA%E4%B8%80%E4%B8%AA-milestones)
  - [将 issue 和 milestones 关联](#%E5%B0%86-issue-%E5%92%8C-milestones-%E5%85%B3%E8%81%94)
- [Projects](#projects)
  - [关于 Projects](#%E5%85%B3%E4%BA%8E-projects)
  - [自动将 issue 链接到 to do 那列](#%E8%87%AA%E5%8A%A8%E5%B0%86-issue-%E9%93%BE%E6%8E%A5%E5%88%B0-to-do-%E9%82%A3%E5%88%97)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# 推荐阅读

- [git中文文档](https://git-scm.com/book/zh/v2)
- [github help](https://help.github.com/)
- [create releases](https://help.github.com/articles/creating-releases/)
- [link to release](https://help.github.com/articles/linking-to-releases/)
- [打标签](https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE)

# Releases

## 关于 releases

发行版是 GitHub 为用户打包和提供软件的方式。releases 里面可以放不同版本的软件，用户可以从中下载。使用 releases，您可以提供二进制文件的链接以及描述更改的发行说明。

![img](https://help.github.com/assets/images/help/releases/overview.png)

### 限制

我们不会限制二进制发布文件的总大小，也不会限制用于发布它们的带宽。但是，每个文件都必须小于 `2 GB`。

## 创建 release

[create releases](https://help.github.com/articles/creating-releases/)

创建 release 前要创建 tag。有下面两种创建方式：

- 从 tag 创建
- 发布一个本地的包

### 从 tag 创建

[link to release](https://help.github.com/articles/linking-to-releases/)

步骤：

1. [创建 tag](#tag) ：这一步完成过后在 releases 页面会出现一个 release

2. 点击 releases 页面的版本号

   ![img](https://help.github.com/assets/images/help/releases/release_tag_name.png)

3. 跳转到的页面点 edit，填好各种信息

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbhnuvxsyj20lr0kddg9.jpg)

4. update release 过后

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbhr5uhgij20n80fjaaa.jpg)

### 发布本地的包

release 基础就是 tag ，所以要在有 tag 的情况下。发布的时候要关联 tag

1. 在GitHub上，导航到存储库的主页面。


2. 在您的存储库名称下，单击 **releases**。

   ![发行标签](https://help.github.com/assets/images/help/releases/release-link.png)


3. 点击 **Draft a new release**。

   ![发布草稿按钮](https://help.github.com/assets/images/help/releases/draft_release_button.png)


4. 为您的版本键入一个版本号。版本基于[Git标签](https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE)。我们建议命名符合[语义版本的](http://semver.org/)标签。

   ![发布标签的版本](https://help.github.com/assets/images/help/releases/releases_tag_version.png)


5. 选择一个包含您想要发布的项目的分支。通常情况下，`master` 除非您发布测试版软件，否则您需要针对您的分支进行发布。

   *Select a branch that contains the project you want to release. Usually, you'll want to release against your `master` branch, unless you're releasing beta software.*

   ![发布标记的分支](https://help.github.com/assets/images/help/releases/releases_tag_branch.png)


6. 输入描述您的版本的标题和描述。

   ![发布说明](https://help.github.com/assets/images/help/releases/releases_description.png)


7. 如果您想将二进制文件与发行版一起包括在内，例如编译后的程序，请在二进制文件夹中手动拖放或选择文件。

   *If you'd like to include binary files along with your release, such as compiled programs, drag and drop or select files manually in the binaries box.*

   ![提供一个DMG的发布](https://help.github.com/assets/images/help/releases/releases_adding_binary.gif)


8. 如果版本不稳定，请选择“ **这是预发行版”，**以通知用户尚未准备好生产。

   *If the release is unstable, select **This is a pre-release** to notify users that it's not ready for production.*

   ![标记为预发行](https://help.github.com/assets/images/help/releases/prerelease_checkbox.png)


9. 如果您准备公布您的版本，请点击**发布版本**。否则，请单击**保存草稿**以稍后处理。

   *If you're ready to publicize your release, click **Publish release**. Otherwise, click **Save draft** to work on it later.*

   ![发布或草稿释放按钮](https://help.github.com/assets/images/help/releases/release_buttons.png)

# Tag

像其他版本控制系统（VCS）一样，Git 可以**给历史中的某一个提交**打上**标签**，**以示重要**。 比较有代表性的是人们会使用这个功能来标记发布结点（v1.0 等等）。 在本节中，你将会学习如何列出已有的标签、如何创建新标签、以及不同类型的标签分别是什么。

- 列出标签 `git tag`
- [创建 `git tag -a [tagname] -m '[tag description]'`](#创建标签)
- [推送 ](#推送标签)
  - `git push origin [tagname]`
  - `git push origin --tags`

**这样创建过后会自动生成一个 release**

## 列出标签

```bash
$ git tag
```

## 创建标签

Git 使用两种主要类型的标签：轻量标签（lightweight）与附注标签（annotated）。

一个`轻量标签`很像一个不会改变的分支 - 它只是一个**特定提交的引用**。

然而，`附注标签`是存储在 Git 数据库中的一个**完整对象**。 它们是可以被校验的；其中包含打标签者的名字、电子邮件地址、日期时间；还有一个标签信息；并且可以使用 GNU Privacy Guard （GPG）签名与验证。 **通常建议创建附注标签**，这样你可以拥有以上所有信息；但是如果你只是想用一个临时的标签，或者因为某些原因不想要保存那些信息，轻量标签也是可用的。

### 附注标签

运行 `tag` 命令时指定 `-a` 选项：

```bash
$ git tag -a v0.1 -m 'my version 0.1'
$ git tag
v0.1
```

> `-m` 选项指定了一条将会存储在标签中的信息。 如果没有为附注标签指定一条信息，Git 会运行编辑器要求你输入信息。

通过使用 `git show` 命令可以看到标签信息与对应的提交信息：

```bash
$ git show
commit ad204d47e2bc887acac78c1027f18622bcff34d4 (HEAD -> source, tag: v0.1, origin/source, origin/HEAD)
Author: kinglion580 <1609019405@qq.com>
Date:   Tue Jan 9 20:45:02 2018 +0800

    fix deploy

diff --git a/_config.yml b/_config.yml
index 959ad9f..7f8d6c5 100644
--- a/_config.yml
+++ b/_config.yml
@@ -76,9 +76,10 @@ theme: indigo

 # Deployment
 ## Docs: https://hexo.io/docs/deployment.html
+## repo: https://github.com/kinglion580/kinglion580.github.io.git
 deploy:
   type: git
-  repo: https://github.com/kinglion580/kinglion580.github.io.git
+  repo: git@github.com:kinglion580/kinglion580.github.io.git
   branch: master
```

> 输出显示了打标签者的信息、打标签的日期时间、附注信息，然后显示具体的提交信息。

### 轻量标签

另一种给提交打标签的方式是使用轻量标签。 轻量标签本质上是将提交校验存储到一个文件中 - 没有保存任何其他信息。 创建轻量标签，**不需要**使用 `-a`、`-s` 或 `-m` 选项，只需要提供标签名字：

```
$ git tag v1.4-lw
$ git tag
v1.4-lw
```

这时，如果在标签上运行 `git show`，你不会看到额外的标签信息。 命令只会显示出提交信息：

```
$ git show v1.4-lw
commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Mon Mar 17 21:52:11 2008 -0700

    changed the version number
```

## 推送标签

### 单个

`git push origin [tagname]`

例如：

```bash
$ git push origin v0.1
```

### 多个

`git push origin --tags`

如果想要一次性推送很多标签，也可以使用带有 `--tags` 选项的 `git push` 命令。 这将会把所有不在远程仓库服务器上的标签全部传送到那里。

```bash
$ git push origin --tags
Counting objects: 1, done.
Writing objects: 100% (1/1), 160 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To git@github.com:schacon/simplegit.git
 * [new tag]         v1.4 -> v1.4
 * [new tag]         v1.4-lw -> v1.4-lw
```

> **注意：标签和分支概念不一样，标签并不能像分支一i样来回移动。不能真的被检出。**

# Wikis

## 关于 wikis

正如编写好的代码和优秀的测试很重要，优秀的文档可以帮助其他人使用和扩展您的项目。

每个GitHub存储库都配备了一个托管文档的部分，称为*wiki*。

*Just as writing good code and great tests are important, excellent documentation helps others use and extend your project.*

*Every GitHub repository comes equipped with a section for hosting documentation, called a wiki.*

![主要的wiki展示](https://help.github.com/assets/images/help/wiki/wiki_main_showcase.png)

GitHub Wiki是您的存储库中的一个地方，您可以共享关于您的项目的长篇内容，例如如何使用它，如何设计它，如何设计其核心原则，等等。README旨在快速引导读者了解您的项目可以做什么，而维基可以用来提供额外的文档。

使用wiki，您可以[像GitHub上的其他地方一样编写内容](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github)。我们使用[我们的开源Markup库](https://github.com/github/markup)将不同的格式转换成HTML，所以当您制作维基页面时，您可以选择使用Markdown，RST，Textile或任何其他支持的格式编写。

Wiki可以直接在GitHub上进行编辑，也可以离线使用文本编辑器，只需推送更改即可。维基通过设计协作。默认情况下，只有存储库上的协作者可以对Wiki进行更改，但是可以将其配置[为对公共存储库中的所有用户](https://help.github.com/articles/changing-access-permissions-for-wikis)启用。

*GitHub Wikis are a place in your repository where you can share long-form content about your project, such as how to use it, how it's been designed, manifestos on its core principles, and so on. Whereas a README is intended to quickly orient readers as to what your project can do, wikis can be used to provide additional documentation.*

*With wikis, you can [write content just like everywhere else on GitHub](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github). We use [our open-source Markup library](https://github.com/github/markup) to convert different formats into HTML, so you can choose to write in Markdown, RST, Textile, or any other supported format when you craft wiki pages.*

*Wikis can be edited directly on GitHub, or you can work with a text editor offline and simply push your changes. Wikis are collaborative by design. By default, only collaborators on your repository can make changes to wikis, but you can configure this to be enabled [for all users on public repositories](https://help.github.com/articles/changing-access-permissions-for-wikis).*

## 通过在线界面添加维基页面

您可以使用我们的Web界面将新的wiki页面直接添加到您的存储库。

1. 在GitHub上，导航到存储库的主页面。

2. 在您的存储库名称下，单击  **Wiki**。

   ![Wiki菜单链接](https://help.github.com/assets/images/help/wiki/wiki_menu_link.png)

3. 从顶部菜单栏中，单击**新建页面**。

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbhzrd8eyj20ns06g3yl.jpg)

4. Wiki页面可以包含GitHub支持的任何标记。默认选择是Markdown，但是您可以使用“编辑模式”下拉菜单切换到不同的标记语言。

   ![Wiki标记选择](https://help.github.com/assets/images/help/wiki/wiki_dropdown_markup.gif)

5. 使用文本编辑器来添加页面的内容。您还可以使用顶部的维基工具栏使用[图形化的所见即所得编辑器](https://en.wikipedia.org/wiki/WYSIWYG)输入文本 。

   ![所见即所得](https://help.github.com/assets/images/help/wiki/wiki_wysiwyg.png)

6. 输入描述您添加的新文件的提交消息。

   ![Wiki提交消息](https://help.github.com/assets/images/help/wiki/wiki_commit_message.png)

7. 要将更改提交到wiki，请单击**保存页面**。


## 搜索

https://help.github.com/articles/searching-wikis/

You can search wikis by using search qualifiers in any combination to narrow your search results.

**Tips:**

- For a list of search syntaxes that you can add to any search qualifier to further improve your results, see "[Understanding the search syntax](https://help.github.com/articles/understanding-the-search-syntax)".
- Use quotations around multi-word search terms. For example, if you want to search for issues with the label "In progress," you'd search for `label:"in progress"`. Search is not case sensitive.

> **Search within a user or organization's repositories**

To find wiki pages from all repositories owned by a certain user or organization, use the `user` or `org`qualifier. To find wiki pages from a specific repository, use the `repo` qualifier.

| Qualifier                    | Example                                  |
| ---------------------------- | ---------------------------------------- |
| `user:*USERNAME*`            | [**user:defunkt**](https://github.com/search?q=user%3Adefunkt&type=Wikis) matches wiki pages from repositories owned by @defunkt. |
| `org:*ORGNAME*`              | [**org:github**](https://github.com/search?q=org%3Agithub&type=Wikis&utf8=%E2%9C%93) matches wikis in repositories owned by the GitHub organization. |
| `repo:*USERNAME/REPOSITORY*` | [**repo:defunkt/gibberish**](https://github.com/search?q=user%3Adefunkt&type=Wikis) matches wiki pages from @defunkt's "gibberish" repository. |

> **Search within a wiki page title or body text**

The `in` qualifier limits the search to the wiki page title or body text. Without the qualifier, both the title and body text are searched.

| Qualifier  | Example                                  |
| ---------- | ---------------------------------------- |
| `in:title` | [**usage in:title**](https://github.com/search?q=usage+in%3Atitle&type=Wikis) matches wiki page titles with the word "usage." |
| `in:body`  | [**installation in:body**](https://github.com/search?q=installation+in%3Abody&type=Wikis) matches wiki pages with the word "installation" in their main body text. |

> **Search by last updated date**

The `updated` qualifier matches wiki pages that were last updated within the specified date range.

Dates support [greater than, less than, and range qualifiers](https://help.github.com/articles/understanding-the-search-syntax).

| Qualifier              | Example                                  |
| ---------------------- | ---------------------------------------- |
| `updated:*YYYY-MM-DD*` | [**usage updated:>2016-01-01**](https://github.com/search?q=usage+updated%3A%3E2016-01-01&type=Wikis) matches wiki pages with the word "usage" that were last updated after 2016-01-01. |

# issue

- issue 的种类用 label 标记
- issue 的处理进度用 milestones 标记
- 更高端的管理方式，[使用 Projects](#Projects)

## 从 milestones 新建 issue

1. [新建一个 milestones](#创建一个-milestones) 

2. 在创建的 milestones 里点击 new issue ，添加一个 issue。

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbkv7lndtj20se04ct8s.jpg)

3. 相关信息填写好后 submit 就可以了

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbkwnf8jlj20tf0bmmxh.jpg)

## 从 projects 新建 issue

移步至 [projects](#Projects)

# milestones

您可以使用里程碑跟踪存储库中的问题组或进程请求的**进度**。

s里程碑里可以和问题以及请求相关联。

## 创建一个 milestones

1. 点击 issues-》milestones

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbk785ix7j20t30dzq3s.jpg)

2. 点击 new milestone

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbk8doghpj20s103qweg.jpg)

3. 填写相关信息

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbka3en9lj20sw0gfgls.jpg)

4. 填写好后提交

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbkb6f2ypj20sk06z74e.jpg)

## 将 issue 和 milestones 关联

进入到 issue 界面可以选 issue 属于哪个 milestone

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbkg9feuhj20tf0kw75v.jpg)

不用点击 commit

在里程碑里可以查看到包括的 issue

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbklntcebj20sq0dijs1.jpg)

> 可以鼠标按住勾选框左边的地方拖动调整`优先顺序`
>
> 可以点击最上面的勾选框对包含的 issue `筛选`

解决一个 issue 就 close 掉 issue ，在里程碑的界面会显示处理进度

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbkb6f2ypj20sk06z74e.jpg)

# Projects

## 关于 Projects

projects 相当于融合了 issue 的 label 和 milestone。在一个界面就行操作。

projects 提供项目管理功能。可以点击 Projects 进入管理界面，点击添加会让你输入项目名，下面的选项可以选择 auto ，也就是自动套用有的模板，就出现下面的界面。

下图框选部分相当于是一个 milestone。

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnblvkpqvmj20sy07mmx9.jpg)

下图这个东西叫看板。里面的列相当于 label。

![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnblcbr24ej21gr0lr76y.jpg)

> 可以把右边列的 issue 拖动到左边的列中去，也可以添加一个 card 转换成 issue。
>
> 上面显示的是进度。
>
> 在 issue 界面中被 close 的 issue 会自动出现在 done 那列中。

> 只用拖动和一些简单的操作就可以管理进度，非常方便，而 milestone 的方式是采用勾选框勾选。
>
> projects 里面可以增加列，也就是说可以采用添加列的方式实现一些其他的功能，比如说添加列来归类 issue 的种类。

## 自动将 issue 链接到 to do 那列

1. 点击 Manage automation

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbm71gv6ej2092076dfu.jpg)

2. 勾选

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbm8b93x1j20cq0a174k.jpg)

   第一个勾选框意思就是新添加的 issue 和请求自动移动到这里

   第二个就是重新打开的 issue 和请求自动移动到这里

3. 连接

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbmci1raqj20t00diaay.jpg)

4. 在 projects 页面就可以看到 issue 自动出现在 to do 那列

   ![](http://ww1.sinaimg.cn/large/8f2bdb7fgy1fnbme1q6w0j20d807gt8s.jpg)














