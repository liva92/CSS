﻿# BFC

标签： CSS

---

### 一、定义：
BFC 全称为 block formatting context，中文为“块级格式化上下文”
如果一个元素具有 BFC，内部子元素再怎么翻江倒海、翻
云覆雨，都不会影响外部的元素。

### 二、那什么时候会触发 BFC 呢？常见的情况如下：

 - <html>根元素；
 - float 的值不为 none；
 - overflow 的值为 auto、 scroll 或 hidden；    
 - display 的值为 table-cell、 table-caption 和 inline-block 中的任何一个；
 - position 的值不为 relative 和 static。



### 三、用途：
1. BFC 元素是不会发生 margin 重叠的；
2. BFC 元素可以用来清除浮动的影响:
.lbf-content { overflow: hidden; }    /* IE7+ */
3. 实现自适应布局
	普通流体元素在设置了 overflow:hidden 后，会自动填满容器中除了浮动元素以外的剩余空间，形成自适应布局效果.

![此处输入图片的描述][1]

 
  [1]: https://github.com/liva92/CSS/blob/master/images/bfc.png
