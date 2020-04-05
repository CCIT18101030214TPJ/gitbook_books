# 六.Hexo部署到Github

**Step1：修改配置文件**

这一步是将hexo和Github关联起来，在你的博客根目录（我的是：blog）下找到 _config.yml， 可以用记事本或者其他编辑工具打开，在最下方找到：



```
deploy:
  type: git
  repo: git@github.com:yourname/yourname.github.io.git 
  branch: master
```

repo中yourname是你的用户名。也可以如下获取：

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200328184826aa.png)

<font color="red">注</font>:配置文件里面所有 : 后面都有一个<font color="red">空格</font>，没有会出错。

**Step2：开始部署**

这个时候需要先安装deploy-git ，也就是部署的命令,这样你才能用命令部署到GitHub。在根目录下的git bash中输入：

```
npm install hexo-deployer-git --save
```

然后接着逐次输入：

```markdown
hexo clean
hexo g
hexo d
```

<font color="red">注</font>:输入hexo d时可能有时会跳出窗口要你输入username和password。

这个时候在你的github仓库中你会发现会出现跟你博客根目录一样的文件，你的根目录上的文件已经部署到你的github仓库上了。

打开浏览器，输入<font color="red">xxxx.github.io</font>，这里请按照  你的github用户名.github.io 输入，就可以访问你的博客啦。

