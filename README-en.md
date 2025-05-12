# Clarity

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/guozhenyi/hexo-theme-clarity/blob/master/LICENSE)

[Preview](https://www.guozhenyi.com)

A clean Hexo theme template with great performance on different devices. 

forked and modified from [maupassant](https://github.com/tufu9441/maupassant-hexo).

## Installation

### Type 1

First install this theme, you can use this installation method to have a try. This installation method need Hexo 5.0 or later.

In root directory of the hexo project:

```bash
npm i hexo-theme-clarity
```

Modify theme setting in _config.yml to clarity.

```diff
_config.yml
- theme: some-theme
+ theme: clarity
```

### Type 2

If you want to modify the theme source code for your site, you can install it in this way.

In root directory of the hexo project:

```shell
git clone --depth 1 https://github.com/guozhenyi/hexo-theme-clarity.git themes/clarity
npm install hexo-renderer-pug --save
npm install hexo-renderer-sass-next --save
```

Similarly, modify theme setting in _config.yml to clarity.

```diff
_config.yml
- theme: some-theme
+ theme: clarity
```

## Configuration

### Theme Configuration

We recommend that you create a new theme configuration file in the site root directory to modify the theme configuration information.

#### Type 1

When you install a theme as an npm package:

```bash
cp node_modules/hexo-theme-clarity/_config.yml _config.clarity.yml
```

#### Type 2

When you clone the theme repository code to themes/clarity:

```bash
cp themes/clarity/_config.yml _config.clarity.yml
```

After that, just change the theme configuration information in the _config.clarity.yml file.

### Configuration Details

- disqus - [Disqus](https://disqus.com) comment system, integrated with [DisqusJS](https://github.com/SukkaW/DisqusJS) API.
- uyan - [Uyan](http://www.uyan.cc) id
- livere - [LiveRe](https://livere.com) data-uid
- changyan - [Changyan](http://changyan.kuaizhan.com) appid
- gitalk - [Gitalk](https://github.com/gitalk/gitalk) comment system
- valine - [Valine](https://valine.js.org) comment system
- minivaline - [MiniValine](https://github.com/MiniValine/MiniValine) comment system
- waline - [Waline](https://waline.js.org) comment system
- utterances - [Utterances](https://utteranc.es) comment system
- twikoo - [Twikoo](https://twikoo.js.org) comment system
- Artalk - [Artalk](https://artalk.js.org) comment system
- google_search - Default search engine
- baidu_search - Search engine for users in China
- swiftype - [Swiftype Search](https://swiftype.com) key
- self_search - A jQuery-based [local search engine](https://www.hahack.com/codes/local-search-engine-for-hexo/), with the dependency on the plugin [hexo-generator-search](https://github.com/wzpan/hexo-generator-search)
- google_analytics - [Google Analytics](https://www.google.com/analytics/) tracking id
- baidu_analytics - [Baidu Analytics](https://tongji.baidu.com) tracking id
- microsoft_clarity - [Microsoft Clarity](https://clarity.microsoft.com/) tracking id
- fancybox - Enable [Fancybox](https://fancyapps.com/fancybox/)
- show_category_count - Show the count of categories in the sidebar widget
- toc_number - Show the list number of toc
- shareto - Enable share button, with the dependency on the plugin [hexo-helper-qrcode](https://github.com/yscoder/hexo-helper-qrcode)
- busuanzi - Enable [Busuanzi](http://ibruce.info) page views
- wordcount - Enable [hexo-wordcount](https://github.com/willin/hexo-wordcount) of each post
- widgets_on_small_screens - Show the widgets at the bottom of small screens
- algolia - Algolia docsearch
- canvas_nest - Enable [canvas-nest.js](https://github.com/hustcc/canvas-nest.js/blob/master/README-zh.md) dynamic background
- donate - Enable donate button after each post
- post_copyright - Enable copyright info after each post
- love - Enable peach heart when clicking anywhere
- plantuml - Enable PlantUML to generate UML diagram
- copycode - Enable one-click copy of code blocks
- dark - Enable to toggle between light/dark modes of the theme
- totop - Enable the rocketship to-top button
- external_css - Enable loading an external CSS file
- post_content_length - Abstract length of each post
- show_forever - Whether to display foreverblog link in footer.
- recent_post_num - Recent post number
- recent_comment_num - Recent comment number
- menu - Customize your menu of pages here, just follow the format of existied items. Don't forget to create corresponding folders inlcuding `index.md` in `source` folder to ensure the pages will correctly display. [FontAwesome](https://fontawesome.com) icon fonts have been integrated, and you can choose other icons which you like [here](https://fontawesome.com/icons/) and use them according to the instruction.
- widgets - Choose and arrange the widgets in sidebar here.
- info - Set your personal information of the info widget here.
- links - Edit your blogroll here, and an independent blogroll page can be displayed by setting `layout: blogroll` of a page.
- timeline - Show a timeline of the website by setting `layout: timeline` of a page.
- Static files - Static files directory, for convenience of CDN usage.
- Theme version - For automatic refresh of static files on CDN.

## Features
#### Logo
You can set a **favicon.ico** for your website, please put it into `source` folder of hexo directory, recommended size: 32px*32px.

You can add a website logo for apple devices, please put an image named **apple-touch-icon.png** into `source` folder of hexo directory, recommended size: 114px*114px.

#### Abstract
You can control the abstract of a post shown at index, by either filling a `description:` item in `front-matter` of the `post.md`, or just inserting a `<!--more-->` before your hidden content.

#### Page
Create folders inlcuding `index.md` in `source` folder to add pages, and add a `layout: page` in `front-matter` of `index.md`. A tagcloud page can be enabled by setting `layout: tagcloud` of a page. If you need a single column page without sidebar, just set `layout: single-column` instead of `layout: page`.

#### Table of Contents
TOC in a post can be enabled by adding a `toc: true` item in `front-matter`.

#### Comments
Comment feature of each post and page can be enabled (default) and disabled by adding a `comments: true` or a `comments: false` in `front-matter`. This could be useful when you want comment feature for a guestbook page, but don't want comment feature for a about page.

#### Syntax Highlighting
Highlighted code showcase is supported, please set the `highlight` option in `_config.yml` of hexo directory like this:

```YAML
highlight:
  enable: true
  auto_detect: true
  line_number: true
  tab_replace:
```

#### Math Equation
Add
```YAML
mathjax: true
```
in Hexo's `_config.yml`.

In the post which you would like to use math equation, add `mathjax: true` in the `front-matter`. For example:

```YAML
title: Test Math
date: 2016-04-05 14:16:00
categories: math
mathjax: true
---
```
The default math delimiters are `$$...$$` and `\\[...\\]` for displayed mathematics,
and `$...$` and `\\(...\\)` for in-line mathematics.

However, if your post contains dollar signs (`$`), and they appear often in non-mathematical parts, in other words, you want to use `$` as dollar sign not inline math delimiter, please add

```YAML
mathjax2: true
```
in Hexo's `_config.yml` instead of `mathjax: true`. Correspondingly, add `mathjax2: true` to the `front-matter` of the post in which
you would like to use math equation.

#### Languages
Seven languages are available for this theme currently: Simplified Chinese (zh-CN), Traditional Chinese (zh-TW), English (en), French (fr-FR), German (de-DE), Korean (ko) and Spanish (es-ES). Contributions of translating to other languages will be highly appreciated.

## Solutions
- Check whether your Terminal's current directory is in hexo's root directory which contains `source/`, `themes/`, etc.

- If you have any trouble in using this theme, please feel free to open an [issue](https://github.com/guozhenyi/hexo-theme-clarity/issues).

## Browsers Support
| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)<br/>Opera |
| --------- | --------- | --------- | --------- | --------- |
| IE9+, Edge| last 10 versions| last 10 versions| last 7 versions| last 10 versions

## Contributing
All kinds of contributions (enhancements, new features, documentation & code improvements, issues & bugs reporting) are welcome.

Looking forward to your [pull request](https://github.com/guozhenyi/hexo-theme-clarity/pulls).

## Contributors
Thanks for all contributors of this repo.

<a href="https://github.com/guozhenyi/hexo-theme-clarity/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=guozhenyi/hexo-theme-clarity" />
</a>
