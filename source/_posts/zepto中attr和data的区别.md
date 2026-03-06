---
title: zepto中$.attr 和 $.data 的区别
date: 2017-01-04 23:37:05
tags:
---

今天遇到的一个问题，是zepto中关于$el.attr('data-id') 和 $el.data('id')取到的数据类型问题。抽出时间来深刻的剖析一下zepto的源码实现。
