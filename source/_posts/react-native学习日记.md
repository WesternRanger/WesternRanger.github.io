---
title: react-native学习日记
date: 2016-12-25 15:33:48
tags:
---

前端领域发展之迅速，令人瞠目结舌。

如果你心目中的前端就是html css jquery这些东西的话，在我心中，那是上个世代的前端。但我不骗你，这样的前端目前仍然是主流需求。

很多朋友跟我说html+css+js很简单啊，我上学的时候就学过。是啊，你给我讲讲浏览器渲染dom的过程吧。你应该很精通了吧。如果你说，这个过程是这样滴：

1. 计算CSS样式
2. 构建Render Tree
3. Layout – 定位坐标和大小，是否换行，各种position, overflow, z-index属性 ……
4. paint 开始画

好的，你还不错嘛，来来来，再来聊聊 Reflow 和 Repaint吧？越详细越好、说重点、不得少于800字，呵呵呵。

dom的东西太多，创建一个dom属性和方法一共228个（嗯？一个div是这样的吧）聊太多我怕把你聊哭。

你说dom太小儿科，来点稍微高大上的东西吧。聊聊 Cascading Style Sheets？嗯。讲一下css优先级？水平三栏布局写三种实现？不许用table、inline-block!!!聊聊 block formatting context？写css的人怎么能没用过sass和less，哦在sass里写个函数，定义几个变量真的可以让共用的css调用起来更加方便，最近貌似一个叫PostCSS的家伙挺火，因为vue-loader？

与时俱进，前端逐渐从pc端转换到移动端

移动端适配是个大问题。不知道REM适配你能算个前端？稍微有点逼格的公司的UI出图的时候都会给前端3倍dpr和2倍dpr的图各一张。移动端用户体验节省流量同样重要，你来做下适配？你不知道什么是dpr？物理像素和设备独立像素知道？等一下，设计师过来告诉你说1px怎么这么宽，你来适配一下？卧槽？1px？我这就是写的1px啊！！！适配个屌啊？怎么适配？嗯，google上适配Retina屏1px线的文章一抓一大片哦。

一些基础css东西我不会又有什么关系呢？我照样可以干活，嗯。我一个小小样式冲突就可以让你盯着屏幕瞅一天。

嗯。该聊聊js了，哦不，应该叫ES6，是啊。现在还有几个人不用ES6啊。但是大多数浏览器对ES6支持不是很完善，chrome也是如此，你需要用babel转一下，babel5和babel6是不一样的哦。你需要配置前端自动化工具，gulp、webpack、grunt你值得拥有。结合jquery／zepto用起来更流弊？写个ajax回调分分钟进入回调地狱，啥？用window.fetch结合promise，再牛逼的你可以用generator啊。浏览器不支持咋办？用polyfill啊。人家说都2017年了，你还用jquery／zepto？没用过vue+vuex／react+redux你好意思说你是做前端的？你们还跟我聊MVC架构？我日，前端都分MVVM啦。

你所谓的前端html+css+js就上面这些？嗯。恭喜你，你可以进入一家公司实习了。

经过这么多年发展，js已经可以运行到几乎所有平台了，嗯！！！之前的报道JavaScript 统治的世界，烤面包机将能运行 JS 了，这并不是噱头。js要统治世界了JavaScript 就要统治世界了？，话虽然说的比较绝对，毕竟近几年的的js发展势头喜人。

在我看来，成为一个合格的初中级前端工程师，要集 知识广度&&代码能力&&艺术美感 于一体，为了达成这个目的，你至少还要具备如下技能：

作为一个前端,你怎么能不会切图？基础的ps操作？
npm玩的6吗？nrm是个啥？nvm／n呢？
yarn有什么优势？yarn.lock 对比 npm-shrinkwrap.json 有什么进步？
怎么优化dom加载？react／vue的 virtual dom 怎么实现的，jsx是什么？
如何提高用户访问网站的响应速度？CDN是什么？
说说http请求？http和https的区别？
http缓存是怎么回事？
webapp的登陆状态如何与客户端保持一致？
webapp如何与客户端native通信？
cookie与localStorage／sessionStorage有什么异同？
说说window.history对象吧。history.pushState和history.replaceState有什么区别
听说过hjax吗？pjax呢？
webapp单页面应用如何解决seo问题？
hybrid开发模式优缺点？
phoneGap和React Native有什么本质区别？
React Native相对于纯native app有什么优缺点？
会写动画吗？能用canvas写一个愤怒的小鸟吗？熟悉svg吗？
RESTful接口前端渲染界面 VS server端渲染界面 的优点。
让一个网站同时支持pc端&手机端，你有几种方案？
linux shell基本操作会吧？chmod 571 file.js 是什么意思？
用过express吧？怎么把你的个人网站部署到服务器？
如果让你做自己的个人网站，如何进行用户权限管理？
了解mongoDB吗？什么是关系型数据库？
用过mysql吗？如何做msyql的io方面优化？
如果要做一个商品的秒杀功能，为避免客户端重复下单（前一段时间的阿里月饼事件），你会怎么限制？你如何去跟服务端沟通？
写过爬虫吗？分析一下爬虫的原理。为什么要爬虫？
node & python 爬虫的优缺点。
什么是跨域？前端跨域的几种方式。
jsonp跨域的实现原理。有什么缺点？
XSS攻击的原理？如何防御？什么是CSRF攻击？怎么防御？
iframe还有应用场景吗？
用过zsh？zsh对比bash有哪些优点？
用过atom吗？atom是怎么用什么语言开发的？
git&svn的使用经历？对比一下各自的优缺点？
用过那些好用的git&svn的图形化工具？
fiddler&charles&wireshark都用过吗？怎么抓包https？
开发webapp如何在设备上调试
喜欢写markdown吗，用过哪些好用的书写markdown的工具？
有没有做过微信开发？说一下微信开发的认证流程。

暂时就想到这么多，随着阅历增加，会不断补充。这不，写这么多就是个引子，就是为了说明，前端工程师能做的事情还是很多的，不要妄自菲薄。作为一个涉事不深的前端工程师，应该有足够的自学动力、没有这股动力去探索未知的领域，凭什么去涨薪拿什么去买房子？（认真脸）土豪请忽略。

最近一直琢磨如何用webapp跟native进行交互，我寻思要想深刻理解，不仅要在项目中推敲，有条件的话还是自己写native模拟一下，嗯。如果RN足够熟练了，可以放弃RN直接上手swift。祝好～

开始我的RN踩坑之旅～

RN学习第一弹 -react-native 入坑之 hello world demo
