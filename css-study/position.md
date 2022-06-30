## Position 定位

position 定位方式有以下几种:

* static 该关键字制定元素使用正常文档的布局行为，即元素在文档常规流中当前的布局位置。此时 top, right, bottom, left, 和 z-index 属性无效 
* relative  该关键字下，元素先放置在未添加定位的位置，在不改变页面布局的前提下调整元素位置（因此会在此元素未添加定位时所在的位置留下空白）
* absolute 该关键字下，元素会被移除正常文档流，并不为元素预留空间，通过指定元素相对于非 static 定位祖先元素偏移，来确定元素位置。 绝对定位可以设置外边距(margin), 且不会与其他边距合并。
* fixed 该关键字下，元素会被移除正常文档流，并不为元素预留空间。而是通过指定元素相对于屏幕视窗位置 (viewport) 的位置， 来指定元素的位置. fixed 属性会创建新的层叠上下文。当元素祖先的 transform, perspective 或 filter 属性非 none 时，容器由视口改为该祖先。
* sticky 该关键字下， 元素根据正常文档流进行布局。然后相对于它最近的滚动祖先元素，基于top, right, bottom, left 的值进行偏移. 该值总是创建一个新的层叠上下文（stacking context）.注意，一个 sticky 元素会“固定”在离它最近的一个拥有“滚动机制”的祖先上（当该祖先的overflow 是 hidden, scroll, auto, 或 overlay时），即便这个祖先不是最近的真实可滚动祖先。这有效地抑制了任何“sticky”行为



## 参考
[position](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position)