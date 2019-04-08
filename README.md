# js-handle-data
> 简述js的数据处理

## forEach
**forEach() 方法对数组的每个元素执行一次提供的函数。**  
> 数组执行forEach方法，传入callBack回调函数，回调函数中进行操作。   cb(item,index,array)   

**不可链式调用**
> 既然我操作的是数组本身那么我是不是就可以继续链式调用其他数组的方法呢？答案是不可以。

**如果数组在迭代时被修改了，其他元素会被跳过**

**替代for循环**

**不能中途跳出**

**改变数组自身 没有返回值  (操作自身)**

## map
1. 新建数组 原数组不变
2. 每个元素都调用一个提供的函数后返回结果
```

```

## 参考资料
> https://juejin.im/post/5ca96c76f265da24d5070563
