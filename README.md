# 依赖安装

还是在 Hexo 根目录，如果以下插件已安装过，无需再次安装。

## Less

主题默认使用 less 作为 css 预处理工具。

```
$ npm install hexo-renderer-less --save

```

## Feed

用于生成 rss。

```
$ npm install hexo-generator-feed --save

```

## Json-content

用于生成静态站点数据，用作站内搜索的数据源。

```
$ npm install hexo-generator-json-content --save

```

## QRCode

用于生成微信分享二维码。

> 可选，不安装时会请求 jiathis Api 生成二维码。

```
$ npm install hexo-helper-qrcode --save

```

## gitment

```
$ npm i --save gitment
```

```
 id: '页面 ID', // 可选。默认为 location.href
 owner: '你的 GitHub ID',
 repo: '存储评论的 repo',
 client_id: '你的 client ID',
 client_secret: '你的 client secret'
```

[点击此处](https://github.com/settings/applications/new) 来注册一个新的 OAuth Application。其他内容可以随意填写，但要确保填入正确的 callback URL（一般是评论页面对应的域名，如 `https://imsun.net`）。

# 开启标签页

```
hexo new page tags

```

修改 `hexo/source/tags/index.md` 的元数据

```
layout: tags
comments: false
---
```

# 开启分类页

仅 card theme 支持。

```
hexo new page categories

```

修改 `hexo/source/categories/index.md` 的元数据

```
layout: categories
comments: false
---
```