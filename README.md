# js-handle-data
> js的数据处理

## forEach
1. 改变数组自身 没有返回值
```
let arr = [{
  name:'xxx',
  age: 18
}]

arr.forEach(item => {
  <!-- 不能return跳出循环 -->
  item.age = item.age+1
})

// [{name: 'xxx', age: 19}] 元素引用值改变了

let arr2 = [1,2,3]
arr2.forEach(item => {
  item = item*2
})
// [1,2,3]  元素数值没有改变
```

## map
1. 新建数组 原数组不变
2. 每个元素都调用一个提供的函数后返回结果
```

```

## 参考资料
> https://juejin.im/post/5ca96c76f265da24d5070563
