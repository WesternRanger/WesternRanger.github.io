---
title: javascript实现数组铺平
date: 2016-02-20 10:42:40
tags:
---

首先解释一下"铺平"，比如一个数组：`[1,[7,3],4]`，他的第二个元素还是一个数组，我们需要把它提取出来，最后应该是这样`[1,7,3,4]`，这就是铺平。

思路很简单，遍历数组，每个元素判断是否为数组元素，不是的话就push到一个新数组，是的话就遍历当前数组元素，不是数组元素的继续push… 这样周而复始的递归调用。听糊涂了吧。直接上代码吧。

一个待铺平的数组
```javascript
var arr = [1,[[2,3],3],4];
```

定义一个空数组存放处理结果：
```javascript
var newArr = [];
```

判断是否为数组的jQueryAPI ：isArray，然后写一个处理数组的function：
```javascript
var dealArr = function(arr){
  for (var i = 0;i<arr.length;i++){
    $.isArray(arr[i]) ? dealArr(arr[i]) : newArr.push(arr[i]);
  }
  return newArr;
};
```

这样一个处理数组铺平的函数就写好了。其实我们还可以拓展一下。我们发现自己没做多少工作，很多工作都是让jQuery的那个api－isArray给帮忙做了。我们知道js的六大数据类型： mumber string boolean null undefined object 这之中并没有array类型，想想就知道jQuery肯定是在isArray判断了数组类型，那么它到底怎么判断的，我们需要探究一下，jQuery源码，如果不想读源码，就直接百度或者google。网上一堆结果。你会发现这样一句话：

```javascript
Object.prototype.toString.call(obj)
```

没错，这就是原生js判断数据类型的方法：可以参考 如何判断js中的数据类型

我们给数组对象添加一个铺平数组的api：panelArr

```javascript
Array.prototype.panelArr = function(){
  var newArr = [];
  var isArray = function(obj) {
    return Object.prototype.toString.call(obj) === '[object Array]';
  };
  var dealArr = function(arr){
    for (var i = 0;i<arr.length;i++){
      isArray(arr[i]) ? dealArr(arr[i]) : newArr.push(arr[i]);
    }
  };
  dealArr(this);
  return newArr;
};
```

可以验证一下，比如执行 `[1,[[2,3],3],4].panelArr()` 的结果就是 `[1,2,3,3,4]`。

西泊浪人©blog.western-ranger.com
