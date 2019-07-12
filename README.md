# mcs
A note for the development of wechat mini-program

### pre-development preparation 
[微信公众号平台](https://mp.weixin.qq.com)
[微信小程序开发官方文档](https://developers.weixin.qq.com/doc/)

import和require的区别
node编程中最重要的思想就是模块化，import和require都是被模块化所使用。

遵循规范
require 是 AMD规范引入方式
import是es6的一个语法标准，如果要兼容浏览器的话必须转化成es5的语法

调用时间
require是运行时调用，所以require理论上可以运用在代码的任何地方
import是编译时调用，所以必须放在文件开头

本质
require是赋值过程，其实require的结果就是对象、数字、字符串、函数等，再把require的结果赋值给某个变量
import是解构过程，但是目前所有的引擎都还没有实现import，我们在node中使用babel支持ES6，也仅仅是将ES6转码为ES5再执行，import语法会被转码为require

* 在nodejs中，模块大概可以分为核心模块和文件模块。

> 核心模块，是被编译成二进制代码，引用的时候只需require表示符即可，如(require('net'))。

> 文件模块，是指js文件、json文件或者是.node文件。在引用文件模块的时候后要加上文件的路径
