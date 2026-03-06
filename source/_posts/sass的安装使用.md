---
title: sass的安装使用
date: 2016-01-26 17:09:43
tags:
---

用scss来书写css还是很方便的。首先是ruby的下载与安装,下载地址是http://rubyinstaller.org/downloads/ 。下载完以后，我们打开安装文件，点击下一步安装即可，注意 在这里下面打上勾，防止以后运行命令的时候找不到。

安装完成后，点击后打开。运行命令
```bash
gem install sass
```

然后等待安装完成，第一次安装可能会花费时间比较长，也有可能是被屏蔽了，多试几次就可以。

下一步我们安装compass，运行命令
```bash
gem install compass
```

然后也是等待安装。安装完成后 运行 `sass -v` 和 `compass -v`。表明已经安装成功。

对于使用，比如你新建一个项目叫test在e盘下， 首先进入e盘的test里。 然后我们在test中建一个文件夹用来存放css样式 ， 用命令
```bash
compass create style
```

点回车，会生成一大堆代码，style文件就建好了，style文件夹里生成了这几个文件：

然后接着上面的黑框输入如下内容 表明监听成功，然后就可以在sass文件夹下的文件里写样式了（比如在ie.scss里）。

引用样式还是引stylesheets文件夹下的css文件，比如
```html
<link style="stylesheet" href="style/stylesheets/ie.css">
```
