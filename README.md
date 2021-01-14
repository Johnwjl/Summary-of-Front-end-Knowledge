# vue

### data为什么只能是函数

- **data** 如果是引用类型，比如函数，复用组件的时候，因为是同一个引用，改变其中一个会影响其他。

### 刷新页面后 **vuex** 值丢失

- 原因： 因为store里的数据是保存在运行内存中的,当页面刷新时，页面会重新加载vue实例，store里面的数据就会被重新赋值初始化
- 解决：将state的数据保存在localstorage、sessionstorage或cookie中（[三者的区别](https://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies)），这样即可保证页面刷新数据不丢失且易于读取。

### localstorage、sessionstorage，cookie 三者区别

- localStorage: localStorage的生命周期是永久的，关闭页面或浏览器之后localStorage中的数据也不会消失。localStorage除非主动删除数据，否则数据永远不会消失。
- sessionStorage:sessionStorage的生命周期是在仅在当前会话下有效。sessionStorage引入了一个“浏览器窗口”的概念，sessionStorage是在同源的窗口中始终存在的数据。只要这个浏览器窗口没有关闭，即使刷新页面或者进入同源另一个页面，数据依然存在。但是sessionStorage在关闭了浏览器窗口后就会被销毁。同时独立的打开同一个窗口同一个页面，sessionStorage也是不一样的。
- cookie:cookie生命期为只在设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭。 存放数据大小为4K左右,有个数限制（各浏览器不同），一般不能超过20个。缺点是不能储存大数据且不易读取。
- 数据存放大小：cookie：4KB左右，localStorage和sessionStorage：可以保存5MB的信息。

### 前端性能优化

- 减少 HTTP 请求
- 使用字体图标代替图片图标
- 压缩前端资源文件
- 图片懒加载/延时加载
- 使用 flexbox 而不是较早的布局模型



### vue router

[Vue-Router面试题汇总 (juejin.cn)](https://juejin.cn/post/6844903961745440775)

