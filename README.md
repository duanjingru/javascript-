# JavaScript基础 

[TOC]

- [ ] 第一天：JavaScript的介绍及基本语法变量 运算符
- [ ] 第二天：JavaScript的流程控制：分支语句 循环 循环结构
- [ ] 第三天：数组
- [ ] 第四天：函数
- [ ] 第五天：内置对象
- [ ] 第六天：内置对象及一些方法

## js介绍

### 1 js是什么

JavaScript是一种运行在客户端的脚本语言 不需要编译
是一门解释性语言
是一门动态类型的语言
是一门基于对象的语言
是一门弱类型的语言

//编译语言 需要把代码翻译成计算机所认知的二进制语言，才能够执行 c语言
 脚本语言：不需要编译 直接执行
 常见的脚本语言：sql cmd 

js---liveScript----JavaScript

1. NetScape在最初将其脚本语言命名为LiveScript，后来Netscape在于Sun合作后将改名为JavaScript
2. JavaScript最初受Java启发而开始设计的，目的之一就是看上去像Java 因此语法上有类似之处，一些名称和命名规范也借自Java
3. JavaScript与Java名称上的近似，是当时Netscape为了营销考虑与sun微系统达成协议的结果。
4. JavaJavaScript的关系就像张雨生和张雨的关系 只是名字很像
5. JavaScript的解释器被称为JavaScript引擎，为浏览器的一部分，广泛用于客户端的脚本语言，最早HTML（标准通用标记语言下的一个应用）网页上使用，用来给html网页增加动态功能

### 2 JavaScript html css

  html提供网页的结构 提供网页的内容
  css用来美化页面
  JavaScript用来控制网页的内容 给网页增加动态的效果

### 3 JavaScript现在的意义

原来===》解决用户和浏览器之间的交互的问题
现在===》 

1. 网页特效
2. 服务端开发（node.js）
3. 命令行工具（node.js）
4. 桌面程序（ELectron）
5. app（Cordova）
6. 控制硬件-物联网（Ruff）
7. 游戏开发（cocos2d-js）	

### 4 js的组成

  JavaScript 简称JavaScript
  JavaScript分三个部分：
  ECMA Script标准----JavaScript的基本的语法 
  DOM------Document Object Model 文档对象模型
  BOM------Browser object Model 浏览器对象模型

### 5 javascript要注意的问题

![1567997011153](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1567997011153.png)

![1567997041684](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1567997041684.png)



## 变量

![1567998199061](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1567998199061.png)

变量声明（有var 有变量名字 没有值）

变量初始化 （有var 有变量名字 有值）

变量的作用：用来操作数据的 可以存储 可以读取

变量的声明：没用赋值

### 1 什么是变量

变量是计算机内存中存储数据的标识符，根据变量名称可以获取到内存中存储的数据

### 2 为什么要使用变量

使用变量可以方便的获取或者修改内存中的数据

### 3 基本代码规范

![1567998964245](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1567998964245.png)

### 4 变量名要注意的问题

1. 变量的名字要有意义
2. 变量名有一定的规范 一般以字母 $符号 下划线开头 中间或者后面可以有$符号 字母 数字
3. 变量名一般都为小写的
4. 变量名如果是多个单词 第一个单词的首字母是小写的 后边的所有单词的首字母都是大写的 这种命名方式为：驼峰命名法
5. 不能使用关键字 
6. 区分大小写

### 5 注释

1. 注释是解释代码的含义 给其他程序员看的
2. 注释的方式 
3. 单行注释// 一般用在一行代码上边
4. 多行注释 /**/ 一般是用在函数或者一段代码上边
5. 代码中如果没用注释 不规范



## 数据类型

> ​	js中的数据类型有那些？
>
> 基本数据类型 number string Boolean null undefined 
>
> 引用数据类型 object 数组 函数

1. number 数字类型 整数和小数

2. string字符串类型 值一般用单引号或者双引号括起来

3. Boolean：布尔类型 值只有两个 true 1 真 男 false 0 假 女

4. null：空类型 值只有一个：null 一个对象指向为空了 此时可以赋值为null

5. undefined：未定义 值只有一个undefined 

   ​	什么情况下结果是undefined 

   - 变量声明了 没有赋值 结果是undefined
   - 函数没有明确的返回值 如果接受了 结果也是undefined 
   - 如果一个变量的结果是undefined 和一个数字进行计算 结果NaN不是一个数字也没有意义

> 判断数据类型 typeof



### 1 number

#### 进制

二进制 八进制 十进制 十六进制

```javascript
var num = 10 //十进制

var num = 012 //八进制

var num3 = 0x123//十六进制
```

#### 数字范围

数字类型有范围 最大值和最小值

```javascript
Number.MAX_VALUE//数字的最大值

Number.MIN_VALUE//数字的最小值

数值范围 正无极 infinity 
负无极 -infinity 
数值范围检测 isFinite 

非数值 NaN 非数值检测 isNaN
```

不要用小数验证小数

![1568011880971](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1568011880971.png)

不要用NaN验证NaN

![1568012087030](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1568012087030.png)

如何验证这个结果是不是NaN 应该使用isNaN()

### 2 string

- 字符串可以使用单引号，也可以使用双引号

- 字符串的长度如何获取 str.length

- html中的转义符 
  $$
  <     &lt;
  >     &gt;
  空格   &nbsp;
  $$

- 字符串拼接 使用+可以把字符串放在一起形成一个字符串（*<u>只要有一个是字符串类型的 其他的是数字，那么结果也是拼接不是相加</u>*）

- 隐式转换

  浏览器帮助我们自动把字符串类型转换成了数字类型

  ![1568013066869](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1568013066869.png)

### 3 boolean

布尔类型 的值有两个 一个true 一个false

### 4 null 和 undefined

```
1. undefined表示一个声明了没有赋值的变量、变量只声明的时候默认是undefined
```

2. null表示一个空、变量的值如果想为null必须手动这是

### 5 对象 

```
var dog ={name:'spot',beed:'dalmatinan'};
```

### 6 数组

```
数组 var arry = ['ffr','free','ferfe']
```

### 7 函数 

```
函数 function add(a,b){return a+b}
```



## 类型转换

### 1 显式数据类型转换

```
Number()
ParseInt() 
ParseFloat() 
String(),
toString(),
Boolean()
```

- 所有其他数据类型都可以转换为bool类型

  ```javascript
  Boolean() Boolean(a）
  ```

- 其它数据类型转变为string 

  ​	如果变量有意义调用toSring()转换

  ​	如果变量没有意义使用String()转换

  ```javascript
  a.toString() 
  toString('2')//二进制  
  string(a) //可以转变null undefined
  ```

- 其它数据类型转变为number 

  ```javascript
    Number(a) 
    Number(undefined) = NaN
    Number('123') = 123
    Number('123.4') = 123.4
    Number('1+2.3') = NaN
    Number('+12.3')=12.3
    Number('0xa')=10
    Number('010')=10 //不会被当做八进制处理
    Number('123ab') = NaN //包含其他字符
    Number('')=0 //空字符转化为零
  
  parseInt() null undefined boolean 转化为NaN
  
  //如果转换的值是Number
  parseInt(10);       //10 如果是整数值，原样输出    
  parseInt(10.3);     //10 如果是小数，舍去小数点一级后面的内容
  
  //如果转换的值是string
  parseInt("123");     //123；如果仅包含数值，转换为对应的数值
  parseInt("234.1");  //234；小数点后面的数值省略    
  parseInt("+12.1");  //12； 首位为符号位，其余为为数值，转换为整数   
  parseInt("1+2.3");  //1； 符号位出现在其他位置，保留符号位前面的数值  
  parseInt("0xa");    //10； 如果仅包含十六进制格式，转为为对应的十进制的值
  parseInt("010");    //10； 【注意！】不会当做八进制被解析，结果为10
  parseInt("");   //NaN；空字符串被转换为NaN
  parseInt("1+2.3");  //1;如果首位为数值，依次向后解析，找到连续的数值，直到遇到第一个非数值的，将之前获取的数值转换为Number返回              
  parseInt("123ac");  //123;
  parseInt(“10”，2)//将其他进制的字符串转换为10进制。2
  
  parseFloat(10);     //10 如果是整数值，原样输出    
  parseFloat(10.1);             //10.1 如果是小数，保留小数点，但是如果是10.0结果为10
  
  //如果转换的值是string
  parseFloat("123");   //123；如果仅包含数值，转换为对应的数值
  parseFloat("234.1");    //234.1；保留小数点后面的数值  
    parseFloat("+12.1");    //12； 首位为符号位，其余为为数值，转换为整数   
  parseFloat(“1+2.3”);    //1；符号位出现在其他位置，保留符号位前的数值    
    parseFloat(“0xa”);      //0； 不会当做十六进制来解析。
    parseFloat("010");  //10； 【注意！】不会当做八进制被解析，结果为10
    parseFloat(""); //NaN；空字符串被转换为NaN
    parseFloat("1+2.3");    //1;如果首位为数值，依次向后解析，找到连续的数值，直到遇到第一个非数值的，将之前获取的数值转换为Number返回              
    parseFloat("123ac");//123;
  ```

### 2 隐式数据类型转换 + - > < 

- 如果不是字符串或对象 使用number 方法转换类型
- 如果有一个字符串 为字符串拼接 
- 如果有对象 对象重写了valueOf返回值为valueOf的返回值 对象
- 只重写了toString返回值为toString的返回值
- 三目运算 a=b>c?b:c

### 3 运算符

 ![1568015036582](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1568015036582.png)

- 关系运算符 > < >= <=  == === != !==
- 关系运算表达式 由关系运算符链接起来的表达式
- 关系运算表达式的结果是布尔类型
- 逻辑运算符 && || ！
- 逻辑运算表达式 由逻辑运算符链接起来的表达式
- ![1568015549321](C:\Users\86173\AppData\Roaming\Typora\typora-user-images\1568015549321.png)

### 4 字面量

​	把一个值直接赋值给一个变量
