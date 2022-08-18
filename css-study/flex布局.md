## flex layout 

flex 模型说明

![](https://github.com/xtcmoons/frondend-notes/blob/main/css-study/image/flex-layout.jpg)

当元素表现为 flex 时，它们沿着两个轴来布局:

* 主轴 (main axio)  是沿着flex元素放置的方向延伸的抽。 该轴的开始和结束被称为 main start 和 main end。
* 交叉轴 (corss axio) 是垂直于flex元素放置方向的轴。该轴的开始和结束被称为 corss start 和 corss end。
* 设置了 display: flex 的父元素被称为 flex 容器 (flex container)。
* 在flex容器中表现为柔性的盒子被称为flex项 (flex item)。

### 一 容器属性

* flex-direction  
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

### 二 项目属性

* order
* flex-grow
* flex-shrink
* flex-basis
* flex
* align-self

1. flex子项的margin值是不会合并的，这一点合普通的块级元素不一样。
2. flex子项如果被设置为绝对定位，则会脱离弹性布局。

## 参考

[flex layout](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Flexbox)

[Flex 布局教程：语法篇](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html?utm_source=tuicool)

[Flex 布局教程：实例篇](https://www.ruanyifeng.com/blog/2015/07/flex-examples.html)

[Flexbox布局中不为人知的细节](https://mp.weixin.qq.com/s?__biz=Mzg4MjE5OTI4Mw==&mid=2247487491&idx=1&sn=673efc5655f50b4118723cf09a1eea71&chksm=cf5b0f9ff82c86891da10c98592cd9eaf2ceb5e1947be58b6376782fa29e8b3dee160d7fede1&cur_album_id=1803251908673896452&scene=190#rd)