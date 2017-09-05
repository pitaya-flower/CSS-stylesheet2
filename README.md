## text-align: center的作用是什么，作用在什么元素上？能让什么元素水平居中

text-align:center;可以让inline 和inline-block的元素居中。


## IE 盒模型和W3C盒模型有什么区别?

W3C盒模型中padding、border所占的空间不在width、height范围内；IE 盒模型width包括content+padding+border；

## *{ box-sizing: border-box;}的作用是什么？

*{ box-sizing: border-box;}的作用是对所有元素应用IE盒模型，指定的任何内边距和边框都将在已设定的宽度和高度内进行绘制。

## line-height: 2和line-height: 200%有什么区别?

line-height:2指行高为文字大小的2倍;line-height: 200%则行高为父元素文字大小的2倍。

line-height属性为百分数时会根据父元素的字体大小先计算出行高值然后再让子元素继承;而为数字时会根据子元素的字体大小动态计算出行高值让子元素继承。

## inline-block有什么特性？如何去除缝隙？高度不一样的inline-block元素如何顶端对齐?

inline-block呈现行内元素的特性，不占据一整行，宽度大小由内容决定，同时又有块级元素的特性，可设置宽高和内外边距。

如何去除缝隙：

（1）移除标签间的空格

元素间的间隙出现的原因是元素标签之间的空格，把空格去掉间隙自然就会消失。

(2)为inline-block的父元素设置font-size:0,再将设置了inline-block的元素重新设置font-size.

高度不一样的inline-block元素如何顶端对齐?

将inline-block元素设置为vertical-align:top;

## CSS sprite 是什么?

叫css精灵，是一种网页图片应用处理方式。将不同的图片/图标合并到一张图片上。这样可以减少网络请求次数，提高网页加载性能。

## 让一个元素"看不见"有几种方式？有什么区别?

display：none;

将元素设置为display:none后，元素在页面上将彻底消失，元素本来占有的空间就会被其他元素占有，也就是说它会导致浏览器的重排和重绘。

visibility:hidden

和display:none的区别在于，元素在页面消失后，其占据的空间依旧会保留着，所以它只会导致浏览器重绘而不会重排。适用于那些元素隐藏后不希望页面布局会发生变化的场景。

opacity:0

这种方法和visibility:hidden的一个共同点是元素隐藏后依旧占据着空间，但我们都知道，设置透明度为0后，元素只是隐身了，它依旧存在页面中。

background-color：rgba（0，0，0，0）；

设置背景色透明
