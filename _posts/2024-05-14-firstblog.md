---
layout: post
title: 我的第一篇博客搭建之旅
categories: [教程]
description: 第一篇博客搭建的过程及整体规划
keywords: 博客搭建, GitHub pages，AI 顶级博客，0基础搭建博客
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
---

# 前言

很久之前就想搭建一个个人博客，主要用来进行[知识管理]和[内容分享]！
因为时间和拖延症，一直也没动手搞起来，最近得闲，便找了找个人博客搭建的教程，完成了自己的首个博客搭建。
本片文章将介绍整个博客搭建的0-1过程，以及该博客网站的未来规划。

# 博客搭建完整过程
## 有哪些博客框架可以选择？
### Solo（#10）
- **简介**: Solo 是一款为程序员设计的动态博客系统，具有社区功能，使博客与社区互动。
- **官网**: [b3log.org/solo](http://b3log.org/solo)
- **技术**: Java 编写，易于注册使用，适合技术背景者自行部署。
- **功能**:
  - 支持 Markdown 编辑器多种模式。
  - 自定义导航和永久链接。
  - SEO 参数配置和代码高亮。
  - 支持导入 Hexo/Jekyll/Markdown。
  - 静态站点生成，适合 GitHub Pages。
- **示例博客**: 
  - 88250.b3log.org
  - www.rainsheep.cn
  - leif.fun
  - expoli.tech
  - www.lyile.cn
- **教学资源**: [Bilibili 视频](http://www.bilibili.com/video/BV1xz…)

### Pelican（#09）
- **简介**: 由 Python 编写的静态网站生成器，适合熟悉 Python 的用户。
- **官网**: [blog.getpelican.com](http://blog.getpelican.com)
- **特点**:
  - 支持 Markdown 和 reStructuredText。
  - 自定义 Jinja 模板。
  - 快速重建时间和插件生态系统。
- **资源**:
- 主题网站：[GitHub上的多种主题](https://github.com/getpelican/pelican-themes)
- 案例网站：[www.fullstackpython.com](www.fullstackpython.com)

### Hexo（#08）
- **简介**: 快速、简洁、高效的跨平台博客框架。
- **官网**: [hexo.io](http://hexo.io)
- **安装**: `npm install -g hexo-cli`
- **插件**: 丰富的插件生态，如后台 UI、哔哩哔哩番剧页面等。
- **主题**: 官网有 300+ 主题，其中示例如： [www.madelove.top](www.madelove.top)。

### Jekyll（#07）
- **简介**: 支持 Markdown 和 Textile 的静态站点生成器，GitHub Pages 基于此构建。
- **官网**: [jekyllrb.com](http://jekyllrb.com)
- **中文资源**: [jekyllcn.com](http://jekyllcn.com)
- **主题**: GitHub 上有大量主题可供选择。[github.com/jekyll/jekyll/wiki/Sites](https://github.com/jekyll/jekyll/wiki/Sites)

### Octopress（#06）
- **简介**: Jekyll 的增强版，更易于插件管理和样式集成。
- **官网**: [octopress.org](http://octopress.org)
- **资源**: GitHub 上有主题和插件。[github.com/imathis/octopress/wiki/3rd-Party-Octopress-Themes](https://github.com/imathis/octopress/wiki/3rd-Party-Octopress-Themes)

### Hugo（#05）
- **简介**: 用 Go 语言编写的快速静态网站生成器。
- **官网**: [gohugo.io](http://gohugo.io)  中文镜像[www.gohugo.org](www.gohugo.org)
- **特点**: 快速编译、跨平台、易安装和部署。
- **资源**:官网提供很多优秀的网站作品,可取官网查看

### VuePress（#04）
- **简介**: 以 Markdown 为中心，适合 Vue 框架开发者。
- **官网**: [vuepress.vuejs.org](http://vuepress.vuejs.org)
- **特点**: 单页面应用，SEO 友好。
- **资源**:github上丰富的插件和主题：[github.com/vuepress/awesome-vuepress](https://github.com/vuepress/awesome-vuepress)

### gitbook（#03）
- **简介**: 文档管理平台，适合电子书格式的博客。
- **官网**: [docs.gitbook.com](http://docs.gitbook.com)
- **资源**:网站案例：[docs.gitbook.com](docs.gitbook.com)
### Docsify（#02）
- **简介**: 无需构建，直接发布 Markdown 的文档网站生成器。
- **官网**: [docsify.js.org](http://docsify.js.org)
- **资源**: [github上的丰富主题和插件](https://github.com/docsifyjs/awesome-docsify)

### WordPress（#01）
- **简介**: 全球使用最广泛的CMS软件，一个基于PHP和MySQL的免费开源内容管理系统。
- **官网**: [wordpress.org](http://wordpress.org)
- **资源**: 大量免费主题和插件。[8 千多个免费主题](wordpress.org/showcase)

## 怎么选择适合自己的框架？
1.如果想做的漂亮，有丰富的图文，华丽的界面。那么就用**WordPress**。
**缺点**:需要自己部署服务器，使用成本和技术要求高。

2.如果想简单搭建个人博客，喜欢干净简洁的界面，只专注于内容本身，那么使用**Jekyll**。
**优点**:可以直接使用GitHub pages搭建个人博客，不需要自己有服务器，有现成的模板可以开箱即用。

**笔者精力有限，选择使用 Jekyll ，通过创建GitHub pages来搭建了本博客网站。
从寻找模板，了解框架结构，进行简单修改，到开始写这首篇博客，耗时两天**

## 怎么使用GitHub pages搭建个人博客？
1. 创建 GitHub 仓库
- 访问 [GitHub](https://github.com) 并登录你的账户。
- 创建一个新的仓库，命名为 `username.github.io`，其中 `username` 是你的 GitHub 用户名。

2. 初始化 Jekyll 项目
- 在你的仓库中，点击 "Create new file" 创建一个名为 `index.html` 的文件。
- 输入以下内容来初始化你的 Jekyll 项目：

```html
<!DOCTYPE html>
<html>
<head>
  <title>Your Blog Title</title>
</head>
<body>
  <h1>Welcome to my blog!</h1>
  <p>This is a test post.</p>
</body>
</html>
```
-提交这个文件。

3. 启用 GitHub Pages
在你的仓库页面，点击 "Settings"。
向下滚动到 "GitHub Pages" 部分。
在 "Source" 下拉菜单中选择 main 分支。
点击 "Save"。

4. 自定义你的 Jekyll 博客
安装 Jekyll 到你的本地机器（如果你还没有安装的话）。
将你的仓库克隆到本地。
使用 Jekyll 的命令行工具来创建新的页面、文章和布局。
```
jekyll new myblog
cd myblog jekyll
serve
```
这将启动一个本地服务器，你可以在浏览器中预览你的网站。

5. 发布你的博客
当你对博客的本地预览满意后，将更改推送到你的 GitHub 仓库。
```
git add
git commit -m "Initial commit"
git push origin main
```
几分钟后，你的网站应该就可以通过 https://username.github.io 访问了。

6. 持续更新和维护
继续添加新的文章和页面，使你的博客更加丰富。
定期更新 Jekyll 版本和主题以保持最佳性能。

**最简单的方法是，可以直接克隆我的项目，然后按照教程进行简单修改就行了。[创建一个和我一样的博客教程](https://github.com/iwillrun/iwillrun.github.io/blob/master/README.md)**

# 博客规划
## 首页
- 分享AI领域高质量的**新闻**：使用AI agent动态获取全网AI领域重大事件，优中选优，打破信息壁垒。
- 分享AI领域高质量的**博客**：了解AI领域最重要的技术应用和大佬们的顶级思考。
- 分享AI领域高质量的**AI产品**：了解哪些AI产品获得了成功？以及为什么成功？还能一直成功下去吗？
- 分享AI领域高质量的**商业案例**：探索AI领域未来的赛道机会，为创业者们提供方向。
## 开源项目
- 分享最顶级的AI 开源项目，改写生产力。
## AI教程
- 分享AI领域实用教程，探索AI在各个行业和工作上的实际应用，掌握这些来扩大自己的小金库。
## AI百科
- 搭建AI领域知识图谱，实现AI ALL IN ONE，让所有人在这里开始了解AI，学习AI，使用AI
## AI导航
- 从这里，去往AI领域的各个顶级站点。
