# Clarity

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/guozhenyi/hexo-theme-clarity/blob/main/LICENSE)

[预览](https://www.guozhenyi.com)｜[English Document](./README-en.md)

一款还在持续演进的简洁、明快的 Hexo 主题。由 [maupassant](https://github.com/tufu9441/maupassant-hexo) Fork 而来。

我在原主题 maupassant 上做了一些改进，本想合并到 maupassant，又担心我的这些改动太激进了而被作者拒绝，就干脆 Fork 过来做演进了。

## 安装

### 方式一

初次安装时，建议用这种方式，可以先试试这个主题是否符合自己的审美。这种安装方式需要 Hexo >= 5.0 版本。

在 hexo 创建的项目根目录下执行：

```bash
npm i hexo-theme-clarity
```

修改 hexo 根目录下 _config.yml 文件中主题设置为 clarity。

```diff
_config.yml
- theme: some-theme
+ theme: clarity
```

### 方式二

在使用此主题的过程中，有不满意的地方，想要自定义修改主题源代码，那么可以改为这种安装方式。

在 Hexo 创建的项目根目录下执行：

```shell
git clone --depth 1 https://github.com/guozhenyi/hexo-theme-clarity.git themes/clarity
npm install hexo-renderer-pug --save
npm install hexo-renderer-sass-next --save
```

同样的，需要修改 hexo 根目录下 _config.yml 文件中主题设置为 clarity。

```diff
_config.yml
- theme: some-theme
+ theme: clarity
```

## 配置

### 主题配置

无论使用以上哪一种主题安装方式，我们都建议你在站点根目录新建一个主题配置文件来修改主题配置信息。

#### 方式一

当你以 npm 包方式安装主题时，你可以复制主题配置文件到项目根目录：

```bash
cp node_modules/hexo-theme-clarity/_config.yml _config.clarity.yml
```

#### 方式二

当你以克隆主题仓库代码到 themes/clarity 时，你可以使用如下方式复制主题配置文件：

```bash
cp themes/clarity/_config.yml _config.clarity.yml
```

之后在 _config.clarity.yml 文件中修改主题配置信息即可。

### 配置详细描述

- disqus - [Disqus](https://disqus.com) 评论系统, 支持 [DisqusJS](https://github.com/SukkaW/DisqusJS) API.
- uyan - [Uyan](http://www.uyan.cc) id
- livere - [LiveRe](https://livere.com) data-uid
- changyan - [Changyan](http://changyan.kuaizhan.com) appid
- gitalk - [Gitalk](https://github.com/gitalk/gitalk) 评论系统
- valine - [Valine](https://valine.js.org) 评论系统
- minivaline - [MiniValine](https://github.com/MiniValine/MiniValine) 评论系统
- waline - [Waline](https://waline.js.org) 评论系统
- utterances - [Utterances](https://utteranc.es) 评论系统
- twikoo - [Twikoo](https://twikoo.js.org) 评论系统
- Artalk - [Artalk](https://artalk.js.org) 评论系统
- google_search - 默认使用Google搜索引擎
- baidu_search - 若想使用百度搜索，将其设定为 `true`
- swiftype - [Swiftype Search](https://swiftype.com) key
- self_search - 基于jQuery的 [本地搜索引擎](https://www.hahack.com/codes/local-search-engine-for-hexo/), 需要安装 [hexo-generator-search](https://github.com/wzpan/hexo-generator-search) 插件使用
- google_analytics - [Google Analytics](https://www.google.com/analytics/) 跟踪ID
- baidu_analytics - [Baidu Analytics](https://tongji.baidu.com) 跟踪ID
- microsoft_clarity - [Microsoft Clarity](https://clarity.microsoft.com/) 跟踪ID
- fancybox - 是否启用 [Fancybox](https://fancyapps.com/fancybox/) 图片灯箱效果
- show_category_count - 是否在侧边栏显示分类数目
- toc_number - Show the list number of toc
- shareto - 是否显示分享按钮, 需要安装 [hexo-helper-qrcode](https://github.com/yscoder/hexo-helper-qrcode) 插件使用
- busuanzi - 是否使用 [不蒜子](http://ibruce.info) 页面访问统计
- wordcount - 是否使用 [hexo-wordcount](https://github.com/willin/hexo-wordcount) 统计文章字数
- widgets_on_small_screens - 是否在移动设备屏幕底部显示侧边栏
- algolia - Algolia docsearch
- canvas_nest - 是否使用 [canvas-nest.js](https://github.com/hustcc/canvas-nest.js/blob/master/README-zh.md) 动态背景
- donate - 是否在每篇文章后面显示捐赠按钮
- post_copyright - 是否在每篇文章后面显示版权信息
- love - 是否在任意点击处出现桃心
- plantuml - 是否使用 PlantUML 生成 UML 图表
- copycode - 是否为代码快启用一键复制功能
- dark - Enable to toggle between light/dark modes of the theme
- totop - 是否使用返回顶部小火箭图标
- external_css - 是否加载外部CSS文件
- post_content_length - Abstract length of each post
- show_forever - 是否在页脚显示十年之约的链接
- recent_post_num - 最近文章显示数量
- recent_comment_num - 最近评论显示数量
- icp - ICP 备案号
- bei - 网安备案号
- menu - Customize your menu of pages here, just follow the format of existied items. Don't forget to create corresponding folders inlcuding `index.md` in `source` folder to ensure the pages will correctly display. [FontAwesome](https://fontawesome.com) icon fonts have been integrated, and you can choose other icons which you like [here](https://fontawesome.com/icons/) and use them according to the instruction.
- widgets - Choose and arrange the widgets in sidebar here.
- info - Set your personal information of the info widget here.
- links - Edit your blogroll here, and an independent blogroll page can be displayed by setting `layout: blogroll` of a page.
- timeline - 网站历史时间线，在页面 `front-matter` 中设置 `layout: timeline` 可显示
- Static files - 静态文件存储路径，方便设置CDN缓存。
- Theme version - For automatic refresh of static files on CDN.

## 主题特性
#### 网站图标

若要设置网站 Favicon，可以将 **favicon.ico** 放在 Hexo 根目录的 `source` 文件夹下，建议的大小：32px*32px。

若要为网站添加苹果设备图标，请将命名为 **apple-touch-icon.png** 的图片放在同样的位置，建议的大小：114px*114px。

#### 文章摘要

首页默认显示文章摘要而非全文，可以在文章的 `front-matter` 中填写一项 `description:` 来设置你想显示的摘要，或者直接在文章内容中插入 `<!--more-->` 以隐藏后面的内容，若两者都未设置，则自动截取文章第一段作为摘要。

#### 添加页面

在 `source` 目录下创建相应名称的文件夹，然后在文件夹中创建 `index.md` 文件，并在 `index.md` 的 `front-matter` 中设置 `layout` 为 `layout: page` 。现已支持添加标签页面，将页面的 `layout` 设置为 `layout: tagcloud` 即可。若需要单栏页面，就将 layout 设置为 `layout: single-column`。

#### 文章目录

在文章的 `front-matter` 中添加 `toc: true` 即可让该篇文章显示目录。

#### 文章评论

文章和页面的评论功能可以通过在 `front-matter` 中设置 `comments: true` 或 `comments: false` 来进行开启或关闭（默认开启）。比如我们创建的 `about` 页面通常不想要评论功能，就可以通过在 `about/index.md` 的头部添加 `comments: false` 来禁用评论功能。

```index.md
---
title: 关于
date: 2025-02-25 20:58:32
comments: false
---

contents of about ...

```

#### 语法高亮

要启用代码高亮，请在Hexo目录的 `_config.yml` 中将 `highlight` 选项按照如下设置：

```YAML
highlight:
  enable: true
  auto_detect: true
  line_number: true
  tab_replace:
```

#### 数学公式

要启用数学公式支持，请在 Hexo 目录的 `_config.yml` 中添加：

Add
```YAML
mathjax: true
```

并在相应文章的 front-matter 中添加 `mathjax: true` ，例如：

```YAML
title: Test Math
date: 2016-04-05 14:16:00
categories: math
mathjax: true
---
```

数学公式的默认定界符是 `$$...$$` 和 `\\[...\\]`（对于块级公式），以及 `$...$` 和 `\\(...\\)`（对于行内公式）。

但是，如果你的文章内容中经常出现美元符号“`$`”, 或者说你想将“`$`”用作美元符号而非行内公式的定界符，请在 Hexo 目录的 `_config.yml` 中添加：

```YAML
mathjax2: true
```

而不是 `mathjax: true`。 相应地，在需要使用数学公式的文章的 front-matter 中也添加 `mathjax2: true`。

#### 支持语言

目前支持简体中文（zh-CN），繁体中文（zh-TW），英语（en），法语（fr-FR），德语（de-DE），韩语（ko）和西班牙语（es-ES），欢迎翻译至其它语言。

## 问题解决

- 检查一下终端当前的目录是否为 Hexo 的根目录，并包含 `source/` 和 `themes/`。
- 使用过程中遇到问题欢迎提交 [issue](https://github.com/guozhenyi/hexo-theme-clarity/issues).

## 浏览器支持

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Opera |
| --------- | --------- | --------- | --------- | --------- |
| IE9+, Edge| last 10 versions| last 10 versions| last 7 versions| last 10 versions

## 贡献代码

接受贡献： [pull request](https://github.com/guozhenyi/hexo-theme-clarity/pulls).

## 贡献者

<a href="https://github.com/guozhenyi/hexo-theme-clarity/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=guozhenyi/hexo-theme-clarity" />
</a>
