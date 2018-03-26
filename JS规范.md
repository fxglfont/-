# 命名规范：作用范围＋类型＋命名
- 通常在 JavaScript 中被认为是减法，所以不允许使用，使用　_　区分  
类的命名：（pascal大驼峰式）　如：ClassPage  
类文件命名规范：类的文件名与类的名字保持一致。如：class_page.js   
类的实例对象的命名（对象变量命名）: （Hungarian）（Camel小驼峰式）。如：Global_classPage_one  
类的继承：如：ClassPage_PageGroup  
类属性：attr_str_name，　或者 m_  
类方法： 动词＋名词　fn_printTable  
私有属性、方法以下划线 _ 开头 var _privateMethod = {};  
回调函数： on_printTable  
参数：param_str_name  
全局变量: 如：Global_Obj_Config   
常量(不可修改)：全大写 (UPPERCASE )  
局部变量：（Hungarian）（Camel小驼峰式）如：l_s_name   
静态变量命名：静态变量应该带前缀‘s’  
JS模板文件名命名: 所有字母都使用小写，使用'_'作为每个词的分界  
boolean 类型的变量使用 is 或 has 开头  
Promise 对象用动宾短语的进行时表达  
不要使用js关键字作为申明的变量或者方法名称  
# 代码书写规范
通常运算符 ( = + - * / ) 前后需要添加空格  
使用 2 个空格符号来缩进代码块，不使用tab  
每行代码字符小于 80，意思是不要出现横向滚动条  
字符串: 统一使用单引号(‘)，不使用双引号(“)。这在创建 HTML 字符串非常有好处  
运算符前后添加空格  
字面量布尔值不能使用在条件表达式里面  
不要省略if for while do...while try...catch...finally语句大括号  
变量定义在变量声明时进行初始化，未初始化的变量放在声明语句的最后  
三目运算符用来进行条件性的赋值，不要用来当做简写的 if 语句使用(主要)  
圆括号内挨着圆括号的地方不添加空格  
圆括号: 谨慎地使用圆括号。  
# 最佳实践
格式化你的 IIFE 代码  
```
(function(){
  'use strict';
 
  // Code goes here
 
}());
```  
启用严格模式，最好是在独立的 IIFE 中应用它  
避免在你的脚本第一行使用它而导致你的所有脚本都启动了严格模式，这有可能会引发一些第三方类库的问题  
不要在 Array 上使用 for-in 循环   
&& 和 || 的 断言 特性   
所有的变量以及方法，应当定义在 function 内的首行  
使用 === 操作符，那比较的双方必须是同一类型为前提的条件下才会有效   
推荐：考虑抛出对象而不仅仅是字符串（默认的抛出值）  
this 关键字 限制它的使用场景   
不要使用 switch switch 在所有的编程语言中都是个非常错误的难以控制的语句  
处理JS被禁用的情况，使用<noscript>来向你的用户解释情况  
对于对象属性使用for ... in循环时，需要通过hasOwnProperty方法过滤非自身属性  
控制流申明if, for, while, switch, try不要嵌套太多层,最多3曾  
js文件行数不要太长，最大行数为1000行(主要)  
js方法行数不要太长，最大行数为100行(主要)  #性能优化
避免不必要的 DOM 操作 当一个元素出现多次时，将它保存在一个变量中  
缓存数组长度  
避免使用 jquery 实现动画  
js代码要写在js文件中，在html的<body></body>最末尾的位置引入  
对象声明直接使用 {} 浏览器对常用的数据类型做了优化处理  
数组（Array）使用[]声明  
不要使用 eval()语句  
不要使用with语句  
通常能用CSS实现的效果要避免使用JS来实现。CSS性能比JS要高  
在项目满足条件的情况下，使用最新的jQuery版本  
JS要避免直接写在页面中，加快页面加载速度  
# JavaScript 注释
## 单行注释
必须独占一行。// 后跟一个空格，缩进与下一行被注释说明的代码一致。    
## 多行注释
避免使用 /*...*/ 这样的多行注释。有多行注释内容时，使用多个单行注释。   
## 函数/方法注释
函数/方法注释必须包含函数说明，有参数和返回值时必须使用注释标识。  
参数和返回值注释必须包含类型信息和说明；   
当函数是内部函数，外部不可访问时，可以使用 @inner 标识；   
```
/**
 * 函数描述
 *
 * @param {string} p1 参数1的说明
 * @param {string} p2 参数2的说明，比较长
 *     那就换行了.
 * @param {number=} p3 参数3的说明（可选）
 * @return {Object} 返回值描述
 */
function foo(p1, p2, p3) {
    var p3 = p3 || 10;
    return {
        p1: p1,
        p2: p2,
        p3: p3
    };
}
```   
## 文件注释
文件注释用于告诉不熟悉这段代码的读者这个文件中包含哪些东西。 应该提供文件的大体内容, 它的作者, 依赖关系和兼容性信息。如下:   
```
/**
 * @fileoverview Description of file, its uses and information
 * about its dependencies.
 * @author user@meizu.com (Firstname Lastname)
 * Copyright 2015 Meizu Inc. All Rights Reserved.
 */
```

