### Javascript 面试题

##### 一、值类型和引用类型都有哪些？

> 值类型：值类型变量存储的值本身；
> 引用类型：引用类型变量存储的是值的存储地址的引用；

> 值类型包括：一般也被成为基本数据类型，在最新的标准中包括 6 种：Number(整数或者浮点数)、BigInt(任意精度的整数)、String(字符串)、Boolean(布尔类型，包括 true、false)、undefined、Symbol。

> 引用类型包括：对象、数组、null、函数。

##### 二、typeof 能判断哪些类型？

> typeof 关键字可以判断所有值类型，对于引用类型，typeof 可以判断函数，但是对于对象、数组、null，typeof 无法区分。

代码示例：

```
console.log(typeof 2.3); // 'number'
console.log(typeof 9007199254740991n); // 'bigint'
console.log(typeof 'animal'); // 'string'
console.log(typeof undefined); // 'undefined'
console.log(typeof false); // 'boolean'
console.log(typeof Symbol('dog')); // 'symbol'

/** 引用类型 */
console.log(typeof function fn(){}); // 'function'
console.log(typeof null); // 'object'
console.log(typeof []); // 'object'
console.log(typeof {}); // 'object'
```
