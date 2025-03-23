+++
title = 'Hugo 的使用指南'
date = 2025-03-23T14:29:41+08:00
draft = false
tags = ['Hugo', '教程', '静态网站']
categories = ['技术']
+++

## Hugo 简介

Hugo 是一个用 Go 语言编写的静态网站生成器，以其构建速度快和灵活性而闻名。它可以在几秒钟内生成一个完整的网站，非常适合用于博客、文档网站或任何静态内容网站。

## 安装 Hugo

根据不同的操作系统，安装 Hugo 的方式也不同：

### macOS

```bash
brew install hugo
```

### Windows

```bash
choco install hugo -confirm
```

### Linux

```bash
sudo apt-get install hugo
```

## 创建新网站

```bash
hugo new site myblog
cd myblog
```

## 安装主题

Hugo 有丰富的主题库，你可以在 [Hugo 主题库](https://themes.gohugo.io/) 中找到适合你的主题。以下是安装 Ananke 主题的示例：

```bash
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
```

然后在 `hugo.toml` 配置文件中添加：

```toml
theme = 'ananke'
```

## 创建内容

```bash
hugo new content posts/my-first-post.md
```

## 本地预览

```bash
hugo server -D
```

这将启动一个本地服务器，通常在 http://localhost:1313/ 可以访问。

## 构建网站

```bash
hugo
```

这将生成静态文件到 `public` 目录中，然后可以将其部署到任何静态文件服务器上。

## 常用配置

Hugo 的主要配置文件是 `hugo.toml`，以下是一些常用配置：

```toml
baseURL = 'https://example.org/'
languageCode = 'zh-cn'
title = '我的博客'
theme = 'ananke'

[params]
  author = '博主名称'
  description = '博客描述'
  favicon = 'favicon.ico'
  site_logo = 'images/logo.png'
  background_color_class = 'bg-black'
  recent_posts_number = 5
```

## 结论

Hugo 是一个强大而灵活的静态网站生成器，非常适合博客和文档网站的开发。它的高效、简单和灵活性使其成为很多开发者的首选工具。
