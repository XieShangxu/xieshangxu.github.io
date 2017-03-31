---
layout: post
title: 只需半小时！使用Github Pages和Jekyll搭建专属的炫酷博客
---

### 初衷

今天心血来潮，想要体验如何简单搭建博客的过程。
其实现在可以写博客的地方实在太多了，[WordPress](https://wordpress.com){:target="_blank"}、[简书](http://www.jianshu.com){:target="_blank"}、[掘金(技术类)](https://www.juejin.im){:target="_blank"}等等。。但是在第三方平台上写博客总感觉缺乏点仪式感，于是想稍微花点时间为自己量身打造一个。

### 调查

对于技术人员来说，很多人都有自己的个人网站。上网稍微调查了一番，发现很多人在讲Github Pages + Jekyll。我想：git大法好啊！接下来就是入坑过程。

### 干货

> 因为本人使用Mac，所以接下来的教程以Mac为例子.

一、 #### 首先创建一个属于自己的Github Page

不知道怎么弄的同学可以参考[这篇文章](http://www.jianshu.com/p/6d8978c380e7){:target="_blank"}

神马？你没有github账号？？你确定你是个搞技术的？？？

二、 #### 进入git项目的目录中

三、 #### 安装Jekyll

因为最新的Jekyll都要求Ruby的版本在2.1以上（否则安装过程中会出错），所以建议安装或者更新到较新版本的Ruby。这里可以使用以下命令：

{% highlight shell %}
curl -sSL https://get.rvm.io | bash -s stable --ruby
{% endhighlight %}

然后根据提示**执行对应的source命令**。

再然后执行：

{% highlight shell %}
rvm install 2.2
rvm use 2.2 --default
{% endhighlight %}

Ruby安装完毕，接下来就是我们的主角Jekyll登场啦！

安装Jekyll和bundle:

{% highlight shell %}
gem install jekyll bundle
{% endhighlight %}

到这里如果没有出错，你离成功不远了。

四、 #### 下载Jekyll主题

我想大多数人是不想自己从头开始写样式的（至少我是这样的[:捂脸])，于是主题这个东西就显得很有用了。我在网上被安利了一个主题，个人也觉得不错，那就顺道再安利吧。[主题地址](https://github.com/onevcat/vno-jekyll)

你可以git clone或者直接下载下来，将其中的所有文件都拷贝到当前目录下。

五、 #### 安装主题以及预览

怀着忐忑的心执行：

{% highlight shell %}
bundle install
{% endhighlight %}

如果执行成功，那说明你已经接近成功了！

怀着期待的心执行：

{% highlight shell %}
jekyll serve
{% endhighlight %}

如果不出意外，那么你现在就可以访问[预览](http://localhost:4000)了！

六、 #### 上传代码

接下来你只需要把所有的代码上传到git就行了，就是这么简单。

七、 #### 绑定域名

如果你还想绑定域名，也很简单。
> 比如你的域名是dashuaige.com

那么只需要在项目中加一个名为CNAME的文件，写入`dashuaige.com`就可。

另外给你的域名加一个CNAME记录，填写**XXX.github.io.**（XXX就是你自己的github名字）。

> 这里末尾一定要加一个.!!!
