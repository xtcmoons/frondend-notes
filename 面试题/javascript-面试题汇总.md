1,  如何理解this关键字

2， call, apply, bind 基本语法
### call 是一个方法，是函数的方法
call 可以调用函数，call可以改变函数this的指向


### 这里的this指向 window
```js
function fun() {
  console.log(this);
}

fun.call()
```

### 这里的this指向 cat
```js
function fun() {
  console.log(this.name);
}

let cat = {
  name: '喵喵'
}

fun.call(cat)

```

call 第一个参数代表你要改变的this， 第二个参数是你要调用函数的参数列表

```js

let dog = {
  name: '旺财',
  sayName() {
    console.log('我是', this.name)
  },
  eat(food1, food2) {
    console.log('我要吃 ', food1, food2)
  }

}

let cat = {
  name: '喵喵'
}

dog.sayName.call(cat)
dog.eat('骨头')
dog.eat.call(cat, '鱼', '肉')
// apply 和 call 区别是后面参数列表是用的一个数组
dog.eat.apply(cat, ['鱼', '肉'])

// bind 不能调用方法，是生产函数
let fun = dog.eat.bind(cat, '鱼', '肉')
fun()


```



原型
《javascript高级程序设计》这样描述原型
每个函数都会创建一个prototype属性，这个属性是一个对象，包含应该由特定引用类型的实例共享的属性和方法。实际上，这个对象就是通过调用构造函数创建的对象的原型。使用原型对象的好处是，在它上面定义的属性和方法都可以被对象实例共享。原来在构造函数中直接赋给对象实例的值，可以直接赋值给它们的原型。


[js的原型与原型链](https://juejin.cn/post/7109064730924285966)

[原型链](https://xjl271314.github.io/docs/javascript/prototype.html)