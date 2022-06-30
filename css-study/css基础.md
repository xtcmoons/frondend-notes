## 层叠样式表(Cascading Style Sheet, 简称CSS)

CSS是为网页添加样式的代码。

css 语法 见下图

![](https://github.com/xtcmoons/frondend-notes/blob/main/css-study/image/mastering-margin-collapsing-demo-2.png)


## 一切皆盒子

在编写CSS时你会发现，你的工作一直围绕着一个个盒子展开 --- 设置尺寸，颜色，位置等等。 见下图

![](https://github.com/xtcmoons/frondend-notes/blob/main/css-study/image/box-model-demo.png)

#### 图一

![](https://github.com/xtcmoons/frondend-notes/blob/main/css-study/image/box-model.png)


#### 图二

## 见图一

* padding: 即内边距，围绕着内容的空间
* border: 即边框，紧接着内边距的线
* margin: 即外边距，围绕元素外部的空间，一直是透明状态, 具有外边距重叠
* content: 即内容区，真正显示内容的空间

## 参考

[CSS 基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/CSS_basics)

[盒模型](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/The_box_model#%E4%BD%BF%E7%94%A8display_inline-block)