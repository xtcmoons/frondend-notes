
# JavaScript 错误类型

* SyntaxError: 语法错误
* ReferenceError: 引用错误 
* RangeError: 范围错误 专指参数超范围
* TypeError: 类型错误 错误的调用了对象的方法
* EvalError: eval()方法错误
* URLError: url地址错误


### 1. Uncaught ReferenceError (引用错误)

引用一个不存在的变量时发生的错误。将一个值分配给无法分配的对象。
比如：对函数的运行结果或者函数赋值。

```js

// 使用未声明的变量
console.log(author);

```

### 2.TypeError （类型错误）

```js

```




# try catch 能捕获到那些异常?

js线程执行已经在 try 中，才能捕获异常。如果之前，之后都无法捕获.

不要用try catch 包裹Promise。Promise的异常不会往上抛。


[详解 JS 错误类型](https://segmentfault.com/a/1190000022746484)

[try catch 能捕获到那些异常](https://juejin.cn/post/6844904143891464200)
