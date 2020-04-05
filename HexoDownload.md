# 三.安装Hexo

前面git和nodejs安装好后，就可以安装hexo博客框架了。

首先创建一个文件夹，命名为你想要的名字，我的名字是blog，这个文件夹在后续就是用来存放你所创建博客的所有文件。这个文件也称根目录。

**Step1：安装Hexo**

在这个blog文件夹（你所创建的文件夹）下直接鼠标右键git bash打开，这个时候会有命令窗口弹出。或者（win+r）输入cmd，然后cd到你创建的blog文件夹。

在窗口中输入：

```
npm install -g hexo-cli 
```

然后等待安装，过程如下，这个过程需要的等待，请耐心。

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//timg.jpg)

**Step2：检验是否安装成功**

在窗口中接着输入hexo -v来检验是否安装成功

```
hexo -v
```

结果显示：

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200327184951a.png)

至此已全部安装完。

**Step3：初始化网址**

在窗口中接着输入：

```
hexo init
```

这个过程可能会比较慢，请耐心等待

最后尾部结果如下：

```
added 432 packages in 59.037s
INFO Start blogging with Hexo!
```

表明初始化已成功。

**Step4：安装网址所需要的依赖插件**

在窗口中接着输入：

```
npm install
```

完成后，在你的根目录（blog文件夹）下会出现以下文件：

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200327195413aa.png)

在这里解释一下：

- node_modules: 依赖包
- public：存放生成的页面
- scaffolds：生成文章的一些模板
- source：用来存放你的文章
- themes：主题
- _config.yml: 博客的配置文件
- db.json：source解析所得到的
- package.json：项目所需模块项目的配置信息

**Step5：生成静态网页和开启本地服务**

在窗口中接着输入：

```
hexo g//生成静态网址
hexo s//开启本地服务器
```

结果显示：

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200327202538aa.png)

在浏览器输入网址[http://localhost:4000](https://link.zhihu.com/?target=http%3A//localhost%3A4000/)就可以查看你的本地博客网页了。

页面如下：

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//7a0fb1a640d490f234de14c9e5d89732.jpg)

如果想关闭本地服务，Ctrl+C 就可以了 或者关闭这个命令窗口。

<font color="red">注</font>：每次想浏览你的本地博客都需在你的根目录下鼠标右击打开git bash 在窗口中输入<font color="red">hexo s</font>命令字符。