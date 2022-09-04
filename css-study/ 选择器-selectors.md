## 选择器 (Selectors)

### 基本选择器

* 通配选择器 (universal selector) *, ns|*, *|*, |*   --- 不推荐使用，性能最低的CSS选择器
* 元素选择器 (type selector) elementname (元素名称)
* 类选择器 (class selector) .classname (类名) [class selector](https://codepen.io/xtcmoons/pen/yLjyNrE)
* ID 选择器 (ID selector) #idname (ID 名)
* 属性选择器 (attribute selector) [attr=value] [属性=值]

### 分组选择器

*  选择器列表 A, B  --- 指定同时选择 A 和 B 元素。 这是一种选择多个匹配元素的分组方法.


### 组合选择器

* 相邻兄弟选择器 A + B  -- 指定A和B选择的元素具有相同的父元素，并且B选择的元素在水平方向上紧随A选择的元素
* 普通兄弟选择器 A ~ B -- 指定由A和B选择的元素共享相同的父元素，并指定A选择的元素在B选择的元素之前（但不一定紧接在B之前）
* 子选择器 A > B -- 指定B选择的元素是A选择的元素的直接子元素
* 后代选择器 A B  -- 指定B选择的元素是A选择的元素的后代，但不一定是直接子代。
* 列关系的双管通道 A || B


选择器	示例	学习 CSS 的教程
类型选择器	h1 { }	类型选择器
通配选择器	* { }	通配选择器
类选择器	.box { }	类选择器
ID 选择器	#unique { }	ID 选择器
标签属性选择器	a[title] { }	标签属性选择器
伪类选择器	p:first-child { }	伪类
伪元素选择器	p::first-line { }	伪元素
后代选择器	article p	后代运算符
子代选择器	article > p	子代选择器
相邻兄弟选择器	h1 + p	相邻兄弟
通用兄弟选择器	h1 ~ p	通用兄弟



### 参考

[选择器](https://www.w3school.com.cn/css/css_selectors.asp)

[选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference#%E9%80%89%E6%8B%A9%E5%99%A8)

[选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#%E9%80%89%E6%8B%A9%E5%99%A8%E5%88%97%E8%A1%A8)