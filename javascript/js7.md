### Javascript 面试题 - 异步进阶

1. 请描述 event loop 的机制，可画图；
2. 什么是宏任务和微任务，两者有什么区别？
3. promise 有哪三种状态？如何变化？

pending(进行中) resolved(成功) rejected(失败)
pending => resolved
pending => rejected

pending 状态，不会触发 then 和 catch；
resolved 状态，会触发 then 回调函数；
rejected 状态，会触发 catch 回调函数；

then 正常返回 resolved，出现异常返回 rejected;
catch 正常返回 resolved，出现异常返回 rejected;

4. promise then 和 catch 的连接
5. async/await 的语法
6. promise 和 setTimeOut 顺序问题
7. promise、setTimeOut、 async/await 的输出顺序问题

##### 一、event loop（事件循环）

1. JavaScript 是单线程运行的；
2. 异步基于回调来实现；
3. event loop 是异步回调的实现原理；

##### 二、promise 进阶

> 一个 Promise 必然处于以下三种状态之一：pending(待定)、fulfilled(已兑现)、rejected(已拒绝)；
> 一个 Promise 的状态变化只会有如下两种：pending => fulfilled 或者 pending => rejected，状态一旦发生变更就不可逆；状态 fulfilled(已兑现)和 rejected(已拒绝)又被统称为 resolved(已决议)，表示 promise 状态已确定并且不可变更。

##### 三、async/await

> async 关键字声明的函数会返回一个 promise 对象;
> await 关键字只能在有 async 关键字声明的函数内部使用，await 下方的代码相当于被包裹在一个 then()方法的内部；
> await 相当于 Promise 的 then 方法，所以当 await 后面的代码返回一个 rejected 状态的 Promise 时，await 后的代码不会执行反而会报错（由于 rejected 状态的 promise 本身就会报错，除非被 catch(try catch 或者 catch 方法)）；

使用示例：

```
  // fn1调用后返回一个promise对象
  const fn1 = async function() {
    return 'fn1';
  };

  const fn2 = async function() {
    const result = await fn1();
    console.log('result', result);
  }
  console.log('fn2', fn2());

  // 输出结果： fn2 Promise {<pending>}
  // 输出结果：result fn2
```

根据上面的例子可以看出：async 关键字声明的函数 fn2 返回的也是一个 promise 对象，在 fn2 调用完毕后再调用异步的 fn1 输出'fn1'.

##### 四、微任务/宏任务

微任务先于 DOM 渲染触发，宏任务后于 DOM 渲染触发。

宏任务包括：setTimeOut setInterval ajax DOM 时间
微任务：Promise、async/await
