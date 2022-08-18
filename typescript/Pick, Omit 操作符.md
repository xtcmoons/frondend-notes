## TS Pick


Pick 
```
从类型定义的属性中，选取指定一组属性，返回一个新的类型
```

```TS
/**
 * From T, pick a set of properties whose keys are in the union K
 */
type Pick<T, K extends keyof T> = {
    [P in K]: T[P];
};
```

原理解析

1, K extends keyof T:
   
   用来获取T类型的所有键的联合类型

```TS
interface Person {
  name: string
  age: number
  id: string
  sex: number
}

// Person 所有类型的联合类型
type Keys = keyof Person // 等同于 'name' | 'age' | 'id' | 'sex'
```

2, P in K

   in 操作符可以操作联合类型，枚举类型

```TS

interface Person {
  name: string
  age: number
  id: string
  sex: number
}

// Person 所有类型的联合类型
type Keys = keyof Person // 等同于 'name' | 'age' | 'id' | 'sex'

// Man 类型于 Person 相等
type Man = {
  [key in Keys] : Person[key]
}


```

# Omit

Omit 于 Pick 类似，Omit是剔除莫个属性，然后返回一个新的类型

```TS
/**
 * Construct a type with the properties of T except for those in type K.
 */
type Omit<T, K extends keyof any> = Pick<T, Exclude<keyof T, K>>;

```



## 参考
[Pick 原理解析](https://blog.csdn.net/weixin_44051815/article/details/123858655)

[精读 Pick](https://github.com/ascoders/weekly/blob/master/TS%20%E7%B1%BB%E5%9E%8B%E4%BD%93%E6%93%8D/243.%E7%B2%BE%E8%AF%BB%E3%80%8APick%2C%20Awaited%2C%20If...%E3%80%8B.md)