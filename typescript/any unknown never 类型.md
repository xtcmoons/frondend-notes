
# any  unknown  never

## any
   没有类型校验，

```TS
function anyDemo(a: any) {
  console.log(a.length);
}

```

## unknown 
   类型未知，需要做类型校验

```TS

function unknownDemo(a: unknown) {
  // 必须做类型判断
  if (typeof a === 'string') {
    console.log(a.length);
  }
  // 不做类型判断会报错
  // console.log(a.length);
}

```

## never
   这个类型永远不可能，一般用在程序运行和抛出异常 funtion 中
   或者用类型收窄

```TS

function neverDemo(): never {
  throw new Error('never')
}
```

类型收窄
```TS
enum SexEnum {
  MAN,
  WOMAN,
  // UNKNOWN   // 放开注释下面函数会报错
}

function getSex(type: SexEnum): string {
  switch (type) {
    case SexEnum.MAN:
      return 'man'
    case SexEnum.WOMAN:
      return 'woman'
    default:
      const value: never = type
      return value
  }
}

```