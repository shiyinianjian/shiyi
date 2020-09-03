---
title: hexo ayer主题
date: 2020-09-03 11:45:40
tags: hexo
categories: themes
---

# hexo ayer主题

历时之久，终于动手，谨此纪念。早有了解，只是未曾下笔。
最近又重新学习了hexo并重新构建了博客，实现了万里长征的第一步，并献给同样喜欢ayer主题的兄弟姐妹。

## 1、初始化博客项目

```
# hexo初始化
hexo init
```

## 2、生成静态文件


```
# 生成静态文件 
hexo g

# 启动项目
hexo s
```

## 3、下载ayer主题
进入themes目录，下载ayer主题

```
# 下载（克隆）ayer主题
git clone https://gitee.com/mirrors/ayer.git
```

## 4、更改主题
编辑**博客根目录**下_config.yml文件

```
# 更换主题为ayer
theme: ayer
```

## 5、查看主题效果

<img src="http://images.shuaiqiang.net/1.png" alt="ayer-init" style="zoom:50%;" />

## 6、重新构建ayer主题

主题的基本结构介绍这里就不多说了，不清楚的小伙伴可以点击[hexo主题文档](https://hexo.io/zh-cn/docs/themes)查看，咱们要做的是通过ayer主题的构架和模板构建自己的个人世界，基于“个人世界”的核心咱们自然要重新设置一番

### 1.主题的配置文件

themes/ayer/_config.yml 更改相关的设置，例如：侧边栏菜单、不蒜子统计、友盟统计、网易云插件等，大家自行设置，随意

### 2.创建分类

```
# 创建分类
hexo new page categorie
```

然后将以下内容添加到/source/categories/index.md文件

```
---
type: "categories"
layout: "categories"
---
```

自我解读：layout的设置会在/themes/ayer/layout文件夹里找到对应的文件categories.ejs，从而在生成分类页面时根据categories.ejs设置的属性和样式生成分类页面

### 3.创建标签

```
# 创建标签
hexo new page tags
```

然后将以下内容添加到/source/tags/index.md文件

```
---
type: "tags"
layout: "tags"
---
```

自我解读：layout的设置会在/themes/ayer/layout文件夹里找到对应的文件tags.ejs，从而在生成标签页面时根据tags.ejs设置的属性和样式生成标签页面

### 4.控制台

访问博客，打开控制台（F12或Fn+F12）即可看到主题作者留下的“彩蛋”，不过，既然要私人订制，找到源代码任君处置

themes/ayer/source/dist目录下，使用记事本打开main.js文件，Ctrl+F快捷键搜索console.log找到“彩蛋”数据

### 5.私有文件

themes/ayer/layout/_partial目录下，使用记事本打开head.ejs文件可以看到主题作者私有文件

```
https://cdn.jsdelivr.net/gh/Shen-Yu/cdn/css/remixicon.min
```

可替换为公共文件[remixicon](http://remixicon.cn/)

```
https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css
```

**注意：更换为公共文件会影响Icon（图标）**

## 7、至此，持续更新中

爱恨随意，悉听君便。

友情链接（原创作者链接）：[ayer主题](https://shen-yu.gitee.io/)

