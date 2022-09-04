

#  React 15 架构

React 15 架构可以分为两层

* Reconciler （协调器） ---- 负责找出变化的组件
* Renderer (渲染器) ---- 负责将变化的组件渲染到页面上

React 15 Reconclier 的缺点是同步递归更新，并且不可中断。 后续架构改为可中断的异步更新。


#  React 16 架构

React 16 架构可以分为三层

* Scheduler (调度器) ---- 调度任务的优先级，高任务优先进入Reconciler 
* Reconciler (协调器) ---- 负责找出变化的组件
* Renderer (渲染器) ---- 负责将变化的组件渲染到页面上

### Scheduler 

我们以浏览器是否有空闲时间作为任务中断的标准，那么我们需要一种机制，当浏览器有剩余时间通知我们。
部分浏览器实现了这个API，[requestIdleCallback](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/requestIdleCallback)
但是React由于兼容性，稳定性等原因实现了更加稳定的 requestIdleCallback 的 polyfill 这就是 Scheduler。
除了在空闲时间触发回调功能外，Scheduler还提供了多种调度优先级任务设置。

### Reconciler

在React 15中Reconciler 是递归处理虚拟DOM的。 在React16中，Reconciler 与 Renderer不在交替工作。 当Scheduler将任务交给Reconciler后，
Reconciler会为变化的虚拟DOM打上增/删/更新的标记。
整个Scheduler 于 Reconciler 的工作都在内存中进行。只有当所有的组件都完成了Reconciler 工作，才会统一交给 Renderer 。
Reconciler内部采用了Fiber的架构

### Renderer

Renderer 根据 Reconciler 为虚拟DOM打的标记，同步执行对应的DOM操作。

Scheduler 和 Renderer 随时可能被中断。 中断的原因

* 有其他更高的优先级任务

* 当前帧没有剩余的时间 


# React 渲染流程

* schedule 调度 scheduler 小顶堆

* render 协调 reconciler - fiber dfs update 

* commit 渲染 renderer ReactDom 

# 参考

[同步更新 vs 异步更新](https://codesandbox.io/s/concurrent-3h48s?file=/src/index.js)

[同步递归更新](https://codesandbox.io/s/fervent-sutherland-pf7sg?file=/src/App.js)

[React 技术揭秘](https://react.iamkasong.com/)

[React 源码解析](https://react.jokcy.me/)

[react源码阅读-react-基础](https://www.tangdingblog.cn/blog/react/reactCode-react-1-2019-12-01/)

[React 虚理DOM之diff算法](../images/16de41554a3ff3e2_tplv-t2oaga2asx-zoom-in-crop-mark_3024_0_0_0.awebp)