- [教程](http://www.codeceo.com/article/es6-next-javascript.html)
- [在线练习](https://babeljs.io/repl/)
- [Babel 运行代码](https://babeljs.io/repl/#?experimental=false&evaluate=true&loose=false&spec=false&code=%2F%2F%20let%0A%0Aif(true)%20%7B%0A%20%20let%20x%20%3D%201%3B%0A%7D%0A%2F%2F%20console.log(x)%3B%20%2F%2F%20x%20is%20not%20defined%0A%0A%0A%0Alet%20list%20%3D%20%5B1%2C%203%2C%205%2C%208%5D%3B%0Afor(let%20i%20%3D0%2C%20l%20%3D%20list.length%3B%20i%20%3C%20l%3B%20i%2B%2B)%20%7B%0A%20%20%2F%2F%20do%20something%0A%7D%0A%0Aconsole.log(i)%3B%20%2F%2F%20i%20is%20not%20defined%0A%0Afor(var%20i%20%3D0%2C%20l%20%3D%20list.length%3B%20i%20%3C%20l%3B%20i%2B%2B)%20%7B%0A%20%20%2F%2F%20do%20something%0A%7D%0Aconsole.log(i)%3B%20%2F%2F%204%0A%0A%0A%2F%2F%20const%0A%0Aconst%20MY_CONSTANT%20%3D%201%3B%0A%2F%2F%20MY_CONSTANT%20%3D%202%3B%20%20%2F%2F%20Error%0A%2F%2F%20const%20SOME_CONST%3B%20%2F%2F%20Error%0A%0Aconst%20MY_OBJECT%20%3D%20%7Bname%3A%20'AidenZou'%7D%3B%0AMY_OBJECT.name%20%3D%20'%E5%AD%90%E5%87%A1'%3B%20%20%20%2F%2F%20Cool%0A%0A%0A%2F%2F%20%E7%AE%AD%E5%A4%B4%E5%87%BD%E6%95%B0%0A%0Alet%20users%20%3D%20%5B%7Bname%3A%20'AidenZou'%2C%20age%3A%2018%7D%2C%20%7Bname%3A%20'%E5%AD%90%E5%87%A1'%2C%20age%3A15%7D%5D%3B%0A%0A%2F%2F%20ES6%20%E7%AE%AD%E5%A4%B4%E5%87%BD%E6%95%B0%0Alet%20names%20%3D%20users.map(%20item%20%3D%3E%20item.name)%3B%0Aconsole.log(names)%20%20%2F%2F%20%5B%22AidenZou%22%2C%22%E5%AD%90%E5%87%A1%22%5D%0A%0A%2F%2F%20ES5%0Alet%20ages%20%3D%20users.map(function(item)%20%7B%0A%20%20return%20item.age%3B%0A%7D)%3B%0Aconsole.log(ages)%3B%20%20%2F%2F%20%5B18%2C15%5D%0A%0Aconsole.log(%5B1%2C%202%5D.map(%20()%20%3D%3E%201%20))%3B%20%2F%2F%20%5B1%2C1%5D%0Aconsole.log(%5B1%2C%202%5D.map(%20(n%2C%20index)%20%3D%3E%20n%20*%20index%20))%3B%20%2F%2F%20%5B0%2C2%5D%0A%0A%5B1%2C%203%2C%205%5D.map(%20n%20%3D%3E%20%7B%0A%20%20n%20%3D%20n%20%25%203%3B%0A%20%20return%20n%3B%0A%7D)%3B%0A%0A%2F%2F%20ES6%0Alet%20book%20%3D%20%7B%0A%20%20%20title%3A%20'X'%2C%0A%20%20%20sellers%3A%20%5B'A'%2C%20'B'%5D%2C%0A%20%20%20printSellers()%20%7B%0A%20%20%20%20%20%20this.sellers.forEach(seller%20%3D%3E%20console.log(seller%20%2B%20'%20sells%20'%20%2B%20this.title))%3B%0A%20%20%20%7D%0A%7D%0Abook.printSellers()%3B%0A%0A%2F%2F%20ES5%0Avar%20book5%20%3D%20%7B%0A%20%20%20title%3A%20'X'%2C%0A%20%20%20sellers%3A%20%5B'A'%2C%20'B'%5D%2C%0A%20%20%20printSellers%3A%20function()%20%7B%0A%20%20%20%20%20%20var%20that%20%3D%20this%3B%0A%20%20%20%20%20%20this.sellers.forEach(function(seller)%20%7B%0A%20%20%20%20%20%20%20%20console.log(seller%20%2B%20'%20sells%20'%20%2B%20that.title)%0A%20%20%20%20%20%20%7D)%0A%20%20%20%7D%0A%7D%0Abook5.printSellers()%3B%0A%0A%0A%2F%2F%20%E5%AD%97%E7%AC%A6%E4%B8%B2%0A%0A'aiden%20zou'.startsWith('aiden')%3B%20%20%2F%2F%20true%0A'aiden%20zou'.endsWith('aiden')%3B%20%20%20%20%2F%2F%20false%0A'aiden%20zou'.includes('aiden')%3B%20%20%20%20%2F%2F%20true%0A%2F%2F%20%E6%96%B9%E4%BE%BF%E5%88%9B%E5%BB%BA%E9%87%8D%E5%A4%8D%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E6%96%B9%E6%B3%95%0A'aiden%20zou'.repeat(3)%3B%20%20%20%20%20%20%20%20%20%20%20%20%2F%2F%20aiden%20zouaiden%20zouaiden%20zou%0A%0A%2F%2F%20%E6%A8%A1%E6%9D%BF%E5%AD%97%E7%AC%A6%E4%B8%B2%0Alet%20name%20%3D%20'Aiden'%2C%0A%20%20%20apples%20%3D%205%2C%0A%20%20%20pears%20%3D%207%2C%0A%20%20%20bananas%20%3D%20function()%20%7B%20return%203%3B%20%7D%0A%0Aconsole.log(%60This%20is%20%24%7Bname%7D.%60)%3B%20%20%2F%2F%20This%20is%20Aiden.%0A%0Aconsole.log(%60He%20carries%20%24%7Bapples%7D%20apples%2C%20%24%7Bpears%7D%20pears%2C%20and%20%24%7Bbananas()%7D%20bananas.%60)%3B%20%20%2F%2F%20He%20carries%205%20apples%2C%207%20pears%2C%20and%203%20bananas.%0A%0A%2F%2F%20ES5%0Aconsole.log('He%20carries%20'%20%2B%20apples%20%2B%20'%20apples%2C%20'%20%2B%20pears%20%2B%20'%20pears%2C%20and%20'%20%2B%20bananas()%20%2B'%20bananas.')%3B%20%20%2F%2F%20He%20carries%205%20apples%2C%207%20pears%2C%20and%203%20bananas.%0A%0Alet%20xstr%20%3D%20%601...%0A2...%0A3%20lines%20long!%60%3B%20%2F%2F%20Yay%0A%0Aconsole.log(xstr)%0A%2F%2F%201...%0A%2F%2F%202...%0A%2F%2F%203%20lines%20long!%0A%0A%2F%2F%20ES5%0Avar%20xstr5%20%3D%20%221...%5Cn%22%20%2B%20%0A%222...%5Cn%22%20%2B%0A%223%20lines%20long!%22%3B%0A%0A%2F%2F%20res%0Avar%20res%20%3D%20%221...%5Cn2...%5Cn3%20lines%20long!%22%3B)

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



## 字符串

### 方法

> String的prototype中添加了几个方便的方法，大部分是indexOf方法的变通：

```
'aiden zou'.startsWith('aiden');  // true
'aiden zou'.endsWith('aiden');    // false
'aiden zou'.includes('aiden');    // true
// 方便创建重复字符串的方法
'aiden zou'.repeat(3);            // aiden zouaiden zouaiden zou
```

### 模板字符串

> 模板字符串提供了一个简洁的方式去创建字符串和实现字符串插值。你可能已经熟悉了它的语法，模板字符串基于符号和花括号符号和花括号{…}，要使用引号将其包围。

```
let name = 'Aiden',
   apples = 5,
   pears = 7,
   bananas = function() { return 3; }

console.log(`This is ${name}.`);  // This is Aiden.

console.log(`He carries ${apples} apples, ${pears} pears, and ${bananas()} bananas.`);  // He carries 5 apples, 7 pears, and 3 bananas.

// ES5
console.log('He carries ' + apples + ' apples, ' + pears + ' pears, and ' + bananas() +' bananas.');  // He carries 5 apples, 7 pears, and 3 bananas.
```

> 和ES5相比较，模板字符串仅仅只是方便字符串的串联。模板字符串通常应用于多行字符串，请记住，空白是字符串的一部分。

```
let xstr = `1...
2...
3 lines long!`; // Yay

console.log(xstr)
// 1...
// 2...
// 3 lines long!

// ES5
var xstr5 = "1...\n" + 
"2...\n" +
"3 lines long!";

// res
var res = "1...\n2...\n3 lines long!";
```

