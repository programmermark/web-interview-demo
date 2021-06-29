### Javascript 面试题 - 类型转换

##### 一、truely 变量和 falsely 变量

> truely 变量: !!varName 为 true 的即是 truely 变量；
> falsely 变量: !!varName 为 false 的即是 falsely 变量；

falsely 变量包括：

```
  !!0 === false
  !!NaN === false
  !!'' === false
  !!null === false
  !!undefined === false
  !!false === false
```

除此之外，都是 truely 变量。

**truely 变量和 falsely 变量的作用是：if(varName) 就是依据变量是 truely 变量还是 falsely 变量来判断的**

举例说明：

```
var a = NaN; // falsely变量
a = 0;
a = "";
a = null;
a = undefined;
a = false;
if(a) {
  console.log('truely变量');
} else {
  console.log('falsely变量');
}

var b = -1; // truely变量
if(b) {
  console.log('truely变量');
} else {
  console.log('falsely变量');
}

```
