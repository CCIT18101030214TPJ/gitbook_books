# 五.SSH配置

因为需要部署到你的github仓库，每次更改都要deploy ，如果不配置ssh key 每次你都需要输入github 账号密码，太过烦琐。

**Step1.生成SSH**

回到你根目录下的git bash窗口中，输入代码：

```
git config --global user.name "yourname"//yourname填写你的github用户名
git config --global user.email "youremail"//youremail填写你的github的邮箱
```

上面的yourname 和 youremail分别指你的github用户名以及github绑定的邮箱。

可以用以下两条，检查一下你有没有输对：

```
git config user.name
git config user.email
```

然后在执行如下命令生成秘钥和公钥:

```
ssh-keygen -t rsa -C "youremail"
```

执行了这个命令会提示你秘钥和公钥存储路径和密码以及确认密码，你连续按三次Enter就好。

```
Enter file in while to save the key(/C/Users/......)
```

执行命令时会有上面所示的代码，这就是你的秘钥和公钥的存储路径，按照所提示的路径打开<font color="red">id_rsa.pub</font>，将里面所有的内容全部复制出来。

<font color="red">注</font>:<font color="red">id_rsa</font>是你这台电脑的私人秘钥，不能给别人看的，<font color="red">id_rsa.pub</font>是公共秘钥，可以随便给别人看。把这个公钥放在GitHub上，这样当你链接GitHub自己的账户时，它就会根据公钥匹配你的私钥，当能够相互匹配时，才能够顺利的通过git上传你的文件到GitHub上。

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200328173631bbbb.png)

**Step2：添加到github**

到你的github主页点击右上角头像，setting -> SSH and GPG keys，新建SSH key。

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200328180736aa.png)

这里的title可以随便填写，我填的是我的用户名。key里面要把你的id_rsa.pub里面的信息复制进去，然后点击Add SSH key。

![](https://cdn.jsdelivr.net/gh/CCIT18101030214TPJ/resource//QQ截图20200328181045aa.png)

这里验证一下是否连接成功，在根目录下的git bash中输入：

```
ssh -T git@github.com
```

会有如下提示：

```
The authenticity of host 'github.com (52.74.223.119)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)?
```

输入：<font color="red">yes</font>，会有以下提示：

```
Hi yremp2! You've successfully authenticated, but GitHub does not provide shell access.
```

这表示配置成功，就可以下一步操作了。