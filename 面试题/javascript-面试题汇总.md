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


