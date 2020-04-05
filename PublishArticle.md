# 7.发布文章

> 概要

- 1.首先，你需要了解markdown语法，如果不了解可以百度[Markdown](https://www.baidu.com/s?ie=UTF-8&wd=markdown语法 "Markdown")
- 2.主题默认文章Hello World，但不同的Hexo主题md文件格式不一样
- 3.可以下载编辑器，推荐[Typora](https://www.typora.io/ "Typora")，界面简洁，方便。

**Step1：编写博客**

首先我们看看在安装hexo默认主题landscape的默认文章 （在博客根目录下的 **\source\\_posts** 下 ）

```
---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

<!-- more -->

## Quick Start

```

如果没有下载编辑器，我们只需在**_posts** 下新建一个Hello World2.md文件，把文档前面的一部分copy来：

```
---
title: Hello World
---
```

title就是文章的标题，然后我们写一个Hello World2（可自行修改），并且写一点内容：

```
---
title: Hello World2
---
### 你好
这是我的第一篇博客
```

**Step2：上传到github**

然后在根目录下鼠标右击点git bash在窗口中依次输入：

```
hexo clean
hexo g
hexo d
```

完成后，打开浏览器，输入<font color="red">xxxx.github.io</font>（xxxx为你的用户名）就可以看到我们的文章了。

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200328195757aa.png)

