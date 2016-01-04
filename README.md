# index

## 前端工具

- js.js

> 这被描述为“微型检查库”，它提供了一个很好的API，允许你做各种数据进行检测。

```
is.decimal(41.5); // true
is.number('hello'); // false
is.regexp(/test/); // true
is.usZipCode('90201'); // true
is.socialSecurityNumber('017-90-7890'); // true
is.hexColor('#333'); // true
is.odd(42); // false
is.domNode(el); // depends on the value of el
is.iphone(); // depends on device
is.ipad(); // depends on device
is.inNextWeek(myDate); // depends on date value
```
