---
title: js重复绑定事件
date: 2016-01-26 17:12:34
tags:
---

昨天被自己绑定click事件坑了一下子，学浅乃危险之事。如果读书多了就不会犯这样的错误了。

这样一个下拉框，点击"我选1"会生成一条"hello world！！！"，点"继续添加"则会继续添加，一次生成一条。如果点击"我选2"也会像之前一样，首先把之前的记录清除掉，再生成一条，可以继续添加。

代码如下：
```javascript
var nodeArea = '<div class="moOrRanArea" style="border:#000 solid 1px;margin:10px 0;">\
  hello world!!!\
</div>';
$("#moOrRan").change(function(){
  if(this.value!=0){
    $(".externalArea .moOrRanArea").remove();
    $(".externalArea").show().append($(nodeArea));
    $("#addArea").bind("click",function(){
      $(".externalArea").append($(nodeArea));
    })
  }else{
    $(".externalArea").hide();
    $(".externalArea .moOrRanArea").remove();
  }
})
```

看起来没啥问题，但是实际运行是有问题的，从"我选1"切换到"他选二"，刚切换过去是这样的：我点一次"继续添加"就成这样了：点击一次，增加了两条！！！

我考虑了半天。。。然后打断点各种试，发现
```javascript
$("#addArea").bind("click",function(){
  $(".externalArea").append($(nodeArea));
})
```
从"我选1"切换到"他选2"的时候，每点击一次继续添加，这段代码执行了两边。原来是"$("#addArea")"，这个dom元素添加了两次click事件。

解决方案：
```javascript
$("#addArea").unbind("click").bind("click",function(){...})
```
首先绑定unbind就搞定。
