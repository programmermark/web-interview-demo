### CSS 面试题 - 定位

##### 一、absolute 和 relative 分别依据什么定位？

> relative: relative 依据自身进行定位，根据 top、left、bottom、right 的值相对当前位置进行偏移；
> absolute: absolute 依据距离当前元素最近的设置`position: relative | fixed | sticky;`的元素进行定位，如果没有找到会依据**body**进行定位

##### 二、居中对齐（水平垂直）有哪些实现方式？

> 水平居中：

1. inline 元素：设置父元素`text-align: center;` 让字元素水平居中
2. block 元素：设置子元素`margin: auto;` 让字元素自动填充 margin；
3. absolute 元素：设置子元素`left: 50%; + margin-left: -50%的元素宽度;`

> 垂直居中：

1. inline 元素：设置父元素`line-height: 等于元素height的值`；
2. absolute 元素：设置子元素`top: 50%; margin-top: -50%的元素高度`;
3. absolute 元素：`top: 50%; transformY(-50%);`;
4. absolute 元素：`top: 0; left: 0; bottom: 0; right: 0; margin: auto;`;

> 水平垂直居中：

1. inline 元素：设置父元素`text-align: center; line-height: 等于元素height的值`；
2. block 元素：设置子元素`margin: auto;` 让子元素自动填充 margin 实现水平垂直居中；
3. absolute 元素：设置子元素`top: 50%; left: 50%; margin-left: -50%元素宽度； margin-top: -50%元素高度; `;
4. absolute 元素：设置子元素`top: 50%; left: 50%; transform(-50%, -50%); `;
5. absolute 元素：设置子元素`top: 0; left: 0; bottom: 0; right: 0; margin: auto;`;
