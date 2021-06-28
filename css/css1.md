### CSS 面试题 - 布局（1）

##### 一、盒模型的宽度如何计算？

> offsetWidth = 元素的宽度 + 元素的左 padding + 元素的右 padding + 元素左边框宽度 + 元素右边框宽度 + 元素的垂直滚动条宽度（如果有）；

> clientWidth = 元素的宽度 + 元素的左 padding + 元素的右 padding

> scrollWidth: 在元素没有超出不显示滚动条的情况下，等于元素的内容宽度 + 元素的左 padding + 元素的右 padding，在显示滚动条的情况下，等于元素的内容宽度 + 元素的左 padding + 元素的右 padding（包括超出不显示的部分）。

##### 二、margin 纵向重叠问题？

> 相邻元素的 margin-bottom 和 margin-top 会发生重叠，空白的 p 元素也会发生重叠；

##### 三、margin 负值的问题？

> margin-top 和 margin-left 为负值，元素会向上、向左移动；
> margin-right 为负值，右侧的元素会向左移动，元素自身不会移动；
> margin-bottom 为负值，下方元素会向上移动，元素自身不会移动；
