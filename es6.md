[在线练习](https://babeljs.io/repl/)

## 变量

- 使用var声明变量时，该变量的作用域是其最近的函数。
- 而使用let声明变量，它的作用域只在包含它的块。

### let

#### code：作用域

```
if(true) {
  let x = 1;
}
console.log(x); // x is not defined
```

#### 经典的数组循环

```
let list = [1, 3, 5, 8];
```

##### let方案
```
for(let i =0, l = list.length; i < l; i++) {
  // do something
}

console.log(i); // i is not defined
```

##### var方案
```
for(var i =0, l = list.length; i < l; i++) {
  // do something
}
console.log(i); // 4
```

> 此方案很容易出现Bug


### const

- 使用const，你可以声明一个只读的值，必须直接指定一个值
- 如果尝试改变它的值或者没有立即指定一个值，就会得到下面的错误：

repl: Line 26: "MY_CONSTANT" is read-only
repl: Unexpected token (27:16)

```
const MY_CONSTANT = 1;
// MY_CONSTANT = 2;  // Error
// const SOME_CONST; // Error
```

```
const MY_OBJECT = {name: 'AidenZou'};
MY_OBJECT.name = '子凡';   // Cool
```

> 注意，你还是可以修改对象的属性或者数组的成员


## 箭头函数

```
let users = [{name: 'AidenZou', age: 18}, {name: '子凡', age:15}];
```

### ES6 箭头函数

```
let names = users.map( item => item.name);
console.log(names)  // ["AidenZou","子凡"]
```

### ES5
```
let ages = users.map(function(item) {
  return item.age;
});
console.log(ages);  // [18,15]
```

> 箭头函数的语法，其中没有function关键字，剩下的就是0个或多个参数、(=>)箭头和函数表达式。注意：return语句将隐式地被添加进来。
> 如果是0个或多个参数，必须添加括号：

```
console.log([1, 2].map( () => 1 )); // [1,1]
console.log([1, 2].map( (n, index) => n * index )); // [0,2]
```

> 如果需要更多的逻辑或者空白区域，可以将函数表达式放在({…})块中。

```
[1, 3, 5].map( n => {
  n = n % 3;
  return n;
});
```

> 箭头函数不仅仅意味着更少的字符，它的行为也不同于常规的函数。一个箭头函数从它的外界上下文中继承this和arguments关键字。这表示你可以摆脱以前那些难看的语句，比如var that = this，而且不需要绑定函数到正确的上下文中。下面有一个例子（注意：this.title等同于ES5版本的that.title）：

```
// ES6
let book = {
   title: 'X',
   sellers: ['A', 'B'],
   printSellers() {
      this.sellers.forEach(seller => console.log(seller + ' sells ' + this.title));
   }
}
book.printSellers();

// ES5
var book5 = {
   title: 'X',
   sellers: ['A', 'B'],
   printSellers: function() {
      var that = this;
      this.sellers.forEach(function(seller) {
        console.log(seller + ' sells ' + that.title)
      })
   }
}
book5.printSellers();
```

