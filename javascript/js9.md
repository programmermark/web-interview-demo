### Javascript 面试题 - BOM 操作 api

##### 一、BOM 是什么？

BOM: 浏览器对象模型

##### 二、navigator（userAgent）和 screen

navigator.userAgent: 用户代理字符串，包含浏览器对不同浏览器的支持，即字符串可以包含对其他浏览器的支持，不能完全用该字段包含'chrome'、'safari'来判断当前浏览器是否是谷歌浏览器或者 safari 浏览器。

screen: screen.width 获取屏幕的宽度，screen.height 获取屏幕的高度。

##### 三、location 和 history

location apis：

location.href: 当前的导航栏链接
location.protocol: 当前页面的协议，http 或者 https
location.pathname: 当前页面的导航
location.search: 当前页面导航链接的参数，?以及后面的内容

##### 四、如何识别浏览器类型？

navigator.userAgent.includes('Chrome');

##### 五、如何拆解 URL 的各个部分？
