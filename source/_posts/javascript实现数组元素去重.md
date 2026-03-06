---
title: javascript实现数组元素去重
date: 2016-02-20 09:21:44
tags:
---

如题,这算是一个比较经典的面试题了吧.在日常开发中也会经常遇到.研究一下还是很有价值的,让我们剖析一下.

随意定义一个数组,比如
```javascript
var arr = [1,2,2,3,4];
```

arr[1]和arr[2]都为2，我们只保留一个。

在解决这个问题之前我们了解一下一种结构叫做"哈希表"，类似这种：
```javascript
var hash_example = {
  "百度" :"http://www.baidu.com/",
  "Google" :"http://www.google.com/",
  "微软" :"http://www.microsoft.com/"
};
```

怎么样，并不陌生吧，我们最熟悉的键值对形式。刚才那个arr数组有五个元素，我们可以给他对应的做一个五个元素的hash表，让他的每个元素作为hash表的"键"，这样：
```javascript
var hash_example = {
  1 : " ",
  2 : " ",
  2 : " ",
  3 : " ",
  4 : " "
};
```

在hash_example中有两个重复的项。我们如果把每个键的值用true和false表示，第一次粗现就标记为true，第二次就标记为false，我们只需要去掉键值为false的项，然后把存下来的键放到数组里就ok了。
```javascript
var hash_example = {
  1 : true,
  2 : true,
  2 : false,
  3 : true,
  4 : true
};
```

利用这个原理，我们首先定义一个空数组来存放去重之后的结果
```javascript
var newArr = [];
```

然后定义一个hash表结构
```javascript
var hash = {};
```

遍历数组，构建哈希表，并得出新数组
```javascript
for(var i=0;i<arr.length;i++){
  if(!hash[arr[i]]){
    newArr.push(arr[i]);
    hash[arr[i]] = true;
  }
}
```

大功告成。

西泊浪人©blog.western-ranger.com
