
## 介绍 5 个常用的 CSS 单位，包括 px, em, rem, vw & vh, vmin & vmax

# px 像素

单位	相对于
em	在 font-size 中使用是相对于父元素的字体大小，在其他属性中使用是相对于自身的字体大小，如 width
ex	字符“x”的高度
ch	数字“0”的宽度
rem	根元素的字体大小
lh	元素的 line-height
vw	视窗宽度的 1%
vh	视窗高度的 1%
vmin	视窗较小尺寸的 1%
vmax	视图大尺寸的 1%


# em 和 rem 区别

1, em是一种相对长度的单位, 相对于自身元素的大小，如果没有设置就参考父级容器的字号大小或者浏览器的字号大小。
例如：给父容器大小设置为 font-size 16px, 在给容器的宽度设置为10em，最后容器宽度为 160px.

2, rem是css3的新标准，也是一种相对长度单位，其相对于HTML根标签的字号大小.
例子 给 HTML 设置 font-size 为 14px， 容器宽度为10rem， 最后浏览器中换算成像素为 140px.


[CSS 的值与单位](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Values_and_units)