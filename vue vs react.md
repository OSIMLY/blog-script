# 从 vue 到 react，前端框架的融会贯通 Vue 和 React 的区别是什么？
马上就要进入农历新年，在这辞旧迎新的时候确实需要总结一下这一年的技术心得了。
react 是对 javascript 的一种扩展，使得 js 可以方便的描述界面结构，vue 则是设计了一套优雅的 api，继承了结构，样式与行为分离的 web 思想，实现了平滑演进，在我看来也是最有可能被吸收为 web 标准的解决方案。
从本质上讲，我们在响应式框架中所构造的界面是虚拟 dom 界面，已经不再是传统意义上的静态 html 界面了。真正的 html 界面和操作它的一系列 dom 方法已经成为了底层技术。react 提供的解决方案是把构造 vdom 的 createElement 方法简化成 JSX 的语法。Vue 则是根据 Template 模板生成 Render 函数。这给我们造成一种仿佛在书写 HTML 代码的错觉，很显然是一种更为亲切的语法糖。
虽然目前在 JS 语言的语法层面并没有为变量提供响应式感知的功能，但是 Vue 却通过定义 get、set 属性的方式实现了这点，即调用 get 时注册订阅，调用 set 时再依次通知订阅者更新。一个简单的 = 运算符就实现了响应机制。React 则是通过 setState 方法来激活更新（小程序也是类似此种方式），显然若论优雅性 Vue 比 React 要好。