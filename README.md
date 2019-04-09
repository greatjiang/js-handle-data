# 简述js的数据处理

## forEach
**forEach() 方法对数组的每个元素执行一次提供的函数。**  
> 数组执行forEach方法，传入callBack回调函数，回调函数中进行操作。  
> (callback(element[, index[, array]])[, thisArg])

**不可链式调用**
> 既然我操作的是数组本身那么我是不是就可以继续链式调用其他数组的方法呢？答案是不可以。

**替代for循环**

**不能中途跳出**
> 不能return

**改变数组本身**

**如果数组在迭代时被修改了，其他元素会被跳过**

**数组元素数值类型不改变，元素引用类型改变**

**不能过滤**
> 不能根据条件return 过滤个鬼啊

[forEach](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

## map
**map() 方法创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果**
> 必须return 不然返回 [null,null,...]   
> (callback(element[, index[, array]])[, thisArg])

**函数只会在有值的时候被调用**
> 返回null

**不修改原数组**

**无法过滤**

[map](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

## filter
**创建新数组 通过回调函数检测(test)所有元素**   
> (callback(element[, index[, array]])[, thisArg])

**不修改原数组**

**可以过滤**

[filter](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

## sort
> sort((a,b)=> {return xxx})

**根据Unicode码排序**

**改变原数组**

**自定义排序条件**
```
arr.sort((a,b)=>{
  return a.age - b.age
})
```
[sort](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)

## some
**检查是否含有满足条件的元素**
> (callback(element[, index[, array]])[, thisArg])
> 只要有一个满足条件立即返回true

**不改变原数组**

[some](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/some)

## every
**检测数组所有元素是否满足所有条件**
> (callback(element[, index[, array]])[, thisArg])

[every](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/every)

## find
**方法返回数组中满足提供的回调函数的第一个元素的值**
> (callback(element[, index[, array]])[, thisArg])

[find](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/find)

## findIndex()
**方法返回数组中满足提供的回调函数的第一个元素的索引**
> (callback(element[, index[, array]])[, thisArg])

[findIndex](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)

## 对照表
--|every|filter|find|forEach|map|some|sort
--|:--:|--:|--:|--:|--:|--:|--:
值|返回boolean|返回匹配的新数组|返回第一个匹配的元素|操作原数组|返回新数组|返回boolean|操作原数组
return|是|是|是|否|是|是|是
应用|判断|筛选|查找|循环|新数组|判断|排序


## 参考资料
> https://juejin.im/post/5ca96c76f265da24d5070563
