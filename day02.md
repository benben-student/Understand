# Arguments 对象

 **`arguments`** 是一个对应于传递给函数的参数的类数组对象。 

`arguments`对象不是一个 [`Array`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array) 。它类似于`Array`，但除了length属性和索引元素之外没有任何`Array`属性。例如，它没有 [pop](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) 方法。但是它可以被转换为一个真正的`Array`：

```
var args = Array.prototype.slice.call(arguments);
var args = [].slice.call(arguments);

// ES2015
const args = Array.from(arguments);
const args = [...arguments];
```

可以使用索引确定单个参数的类型。

```
console.log(typeof arguments[0]); //this will return the typeof individual arguments.
```

### [对参数使用扩展语法](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/arguments#对参数使用扩展语法)

您还可以使用[`Array.from()`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/from)方法或[扩展运算符](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)将参数转换为真实数组：

```
var args = Array.from(arguments);
var args = [...arguments];
```

## [属性](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/arguments#properties)

- `arguments.callee`

  指向参数所属的当前执行的函数。

- `arguments.length`

  传递给函数的参数数量。

- `arguments[@@iterator]`

  返回一个新的[Array 迭代器](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/@@iterator) 对象，该对象包含参数中每个索引的值。