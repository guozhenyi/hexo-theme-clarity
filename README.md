# Clarity

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/guozhenyi/hexo-theme-clarity/blob/main/LICENSE)

[预览](https://www.guozhenyi.com)｜[English Document](./README-en.md)

一款还在持续演进的简洁、明快的 Hexo 主题。由 [maupassant](https://github.com/tufu9441/maupassant-hexo) Fork 而来。

我在原主题 maupassant 上做了一些改进，本想合并到 maupassant，又担心我的这些改动太激进了而被作者拒绝，就干脆 Fork 过来做演进了。

## 安装

在 Hexo 创建的项目根目录中，安装主题和模板引擎：

```shell
$ git clone https://github.com/guozhenyi/hexo-theme-clarity.git themes/clarity
$ npm install hexo-renderer-pug --save
$ npm install hexo-renderer-sass-next --save
```

之后，在 `_config.yml` 文件中将 `theme` 的值改为 `clarity`。

## 配置

默认配置:

```YAML
disqus:
  enable: false ## If you want to use Disqus comment system, please set the value to true.
  shortname: ## Your disqus_shortname, e.g. username
  api: ## You can visit Disqus comments in China mainland without barriers using Disqus API, e.g. https://disqus.skk.moe/disqus/
  apikey: ## Your API key obtained in Disqus API Application, e.g. yk00ZB1fjYGRkrCrDDRYDUjpp26GJWJiJRZQZ5SY0r3th5FMW6pnSzQMnWH7ua7r
  admin: ## Username of your Disqus moderator, e.g. username
  admin_label: ## The text of Disqus moderator badge, e.g. Mod
uyan: ## Your uyan_id. e.g. 1234567
livere: ## Your livere data-uid, e.g. MTAyMC8zMDAxOC78NTgz
changyan: ## Your changyan appid, e.g. cyrALsXc8
changyan_conf: ## Your changyan conf, e.g. prod_d8a508c2825ab57eeb43e7c69bba0e8b
gitalk: ## See: https://github.com/gitalk/gitalk
  enable: false ## If you want to use Gitment comment system please set the value to true.
  owner: ## Your GitHub ID, e.g. username
  repo: ## The repository to store your comments, make sure you're the repo's owner, e.g. gitalk.github.io
  client_id: ## GitHub client ID, e.g. 75752dafe7907a897619
  client_secret: ## GitHub client secret, e.g. ec2fb9054972c891289640354993b662f4cccc50
  admin: ## Github repo owner and collaborators, only these guys can initialize github issues.
valine: ## See: https://valine.js.org
  enable: false ## If you want to use Valine comment system, please set the value to true.
  appid: ## Your LeanCloud application App ID, e.g. pRBBL2JR4N7kLEGojrF0MsSs-gzGzoHsz
  appkey: ## Your LeanCloud application App Key, e.g. tjczHpDfhjYDSYddzymYK1JJ
  notify: false ## Mail notifier, see https://github.com/xCss/Valine/wiki/Valine-评论系统中的邮件提醒设置
  verify: false ## Validation code.
  placeholder: Just so so ## Comment box placeholders.
  avatar: "mm" ## Gravatar type, see https://github.com/xCss/Valine/wiki/avatar-setting-for-valine
  pageSize: 10 ## Number of comments per page.
  guest_info: nick,mail,link ## Attributes of reviewers.
minivaline: ## See: https://github.com/MiniValine/MiniValine
  enable: false ## If you want to use MiniValine comment system, please set the value to true.
  appId: ## Your LeanCloud application App ID, e.g. pRBBL2JR4N7kLEGojrF0MsSs-gzGzoHsz
  appKey: ## Your LeanCloud application App Key, e.g. tjczHpDfhjYDSYddzymYK1JJ
  placeholder: Write a Comment ## Comment box placeholder.
  adminEmailMd5: ## The MD5 of Admin Email to show Admin Flag.
  math: true ## Support MathJax.
  md: true ## Support Markdown.
  # MiniValine's display language depends on user's browser or system environment
  # If you want everyone visiting your site to see a uniform language, you can set a force language value
  # Available values: en  | zh-CN | (and many more)
  # More i18n info: https://github.com/MiniValine/minivaline-i18n
  lang:
waline: ## See: https://waline.js.org/
  enable: false ## If you want to use Waline comment system, please set the value to true.
  serverURL: ## Your server url, e.g. https://your-domain.vercel.app
  pageSize: 30 ## The desired number of comments shown in each page.
  wordLimit: 500 ## Limit the number of words in comments, 0 means no limit.
  requiredMeta: ['nick','mail'] ## Required user information, e.g. ['nick','mail','link']
  count: 5 ## The number comments displayed in the recent_comments widget, default is 10.
utterances: ## See: https://utteranc.es
  enable: false ## If you want to use Utterances comment system, please set the value to true.
  repo: ## The repository utterances will connect to, e.g. tufu9441/comments
  identifier: title ## The mapping between blog posts and GitHub issues.
  theme: github-light ## Choose an Utterances theme which matches your blog.
twikoo: ## See: https://twikoo.js.org
  enable: false ## If you want to use twikoo comment system, please set the value to true.
  envId: ## Tencent CloudBase envId
  region: ## Tencent CloudBase region, e.g. ap-shanghai
  path: ## Article path, e.g. window.location.pathname

google_search: true ## Use Google search, true/false.
baidu_search: false ## Use Baidu search, true/false.
swiftype: ## Your swiftype_key, e.g. m7b11ZrsT8Me7gzApciT
self_search: false ## Use a jQuery-based local search engine, true/false.
google_analytics: ## Your Google Analytics tracking id, e.g. UA-42425684-2
baidu_analytics: ## Your Baidu Analytics tracking id, e.g. 8006843039519956000
microsoft_clarity:  ## Your Microsoft Clarity tracking id, e.g. zg2ctuea9j
fancybox: true ## 是否启用图片灯箱效果，默认启用。设为 false 可禁用。
show_category_count: false ## If you want to show the count of categories in the sidebar widget please set the value to true.
toc_number: true ## If you want to add list number to toc please set the value to true.
shareto: false ## If you want to use the share button please set the value to true, and you must have hexo-helper-qrcode installed.
busuanzi: false ## If you want to use Busuanzi page views please set the value to true.
wordcount: false ## If you want to display the word counter and the reading time expected to spend of each post please set the value to true, and you must have hexo-wordcount installed.
widgets_on_small_screens: false ## Set to true to enable widgets on small screens.
canvas_nest:
  enable: false ## If you want to use dynamic background please set the value to true, you can also fill the following parameters to customize the dynamic effect, or just leave them blank to keep the default effect.
  color: ## RGB value of the color, e.g. "100,99,98"
  opacity: ## Transparency of lines, e.g. "0.7"
  zIndex: ## The z-index property of the background, e.g. "-1"
  count: ## Quantity of lines, e.g. "150"
donate:
  enable: false ## If you want to display the donate button after each post, please set the value to true and fill the following items on your need. You can also enable donate button in a page by adding a "donate: true" item to the front-matter.
  github: ## GitHub URL, e.g. https://github.com/Kaiyuan/donate-page
  alipay_qr: ## Path of Alipay QRcode image, e.g. /img/AliPayQR.png
  wechat_qr: ## Path of Wechat QRcode image, e.g. /img/WeChatQR.png
  btc_qr: ## Path of Bitcoin QRcode image, e.g. /img/BTCQR.png
  btc_key: ## Bitcoin key, e.g. 1KuK5eK2BLsqpsFVXXSBG5wbSAwZVadt6L
  paypal_url: ## Paypal URL, e.g. https://www.paypal.me/tufu9441
post_copyright:
  enable: false ## If you want to display the copyright info after each post, please set the value to true and fill the following items on your need.
  author: ## Your author name, e.g. tufu9441
  copyright_text: ## Your copyright text, e.g. The author owns the copyright, please indicate the source reproduced.
love: false ## If you want the peach heart to appear when you click anywhere, set the value to true.
plantuml: ## Using PlantUML to generate UML diagram, must install hexo-filter-plantuml (https://github.com/miao1007/hexo-filter-plantuml).
  render: "PlantUMLServer" ##  Local or PlantUMLServer.
  outputFormat: "svg" ## common options: svg/png
copycode: true ## If you want to enable one-click copy of the code blocks, set the value to true.
dark: false ## If you want to toggle between light/dark themes, set the value to true.
totop: true ## If you want to use the rocketship button to return to the top, set the value to true.
external_css: false ## If you want to load an external CSS file, set the value to true and create a file named "external.css" in the source/css folder.
post_content_length: 180 ## Set the length of the post summary displayed on home page when no description written.
icp: ## 显示 icp 信息
bei: ## 显示公安部备案信息

menu: # 菜单项，记得要在 source 创建 directory 中填写的目录（archives不用自己创建，about需要自己创建）
  - page: home
    directory: .
    icon: fa-home
  - page: archive
    directory: archives/
    icon: fa-archive
  - page: about
    directory: about/
    icon: fa-user
  - page: rss
    directory: atom.xml
    icon: fa-rss

widgets: ## Seven widgets in sidebar provided: search, info, category, tag, recent_posts, recent_comments and links.
  - search
  - info
  - category
  - tag
  - recent_posts
  - recent_comments
  - links

info:
  avatar: /img/avatar.png
  discription: To be a better man.
  outlinkitem:
    - name: twitter
      outlink: https://twitter.com/username
      message: Twitter
    - name: envelope
      outlink: mailto:admin@domain.com
      message: Email
    - name: github
      outlink: https://github.com/username
      message: Github
    - name: rss
      outlink: /atom.xml
      message: RSS

links:
  - title: site-name1
    url: http://www.example1.com/
    src: https://www.example1.com/favicon.ico
    desc: XXX's Blog
  - title: site-name2
    url: http://www.example2.com/
    src: https://www.example1.com/favicon.ico
    desc: YYY's Blog
  - title: site-name3
    url: http://www.example3.com/
    src: https://www.example3.com/favicon.ico
    desc: ZZZ's Blog

timeline:
  - num: 1
    word: 2014/06/12-Start
  - num: 2
    word: 2014/11/29-XXX
  - num: 3
    word: 2015/02/18-DDD
  - num: 4
    word: More

# Static files
js: js
css: css

# Theme version
version: 1.0.0
```

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
