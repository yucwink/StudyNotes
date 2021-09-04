# 一、js基础

## 1. 数据类型

js的数据类型分为两类：

- 简单数据类型（Number,String,Boolean,Undefined,Null)
- 复杂数据类型（object）

### 1.1 Number

1. 二进制（0b)，八进制（0），十六进制（0x）
2. 数字型又最大值和最小值。
   - 最大值：Number.MAX_VALUE， 1.7976931348623157e+308
   - 最小值：Number.MAX_VALUE,   5e-32

3. 数字型的三个特殊值
   - infinity，代表无穷大，大于任何值
   - -infinity，代表无穷小，小于任何值
   - NaN, Not a number，代表一个非数值

4. isNaN()  可以用来判断一个变量是否为非数字的类型，或者返回true或者false

### 1.2 String

JavaScript 的字符串是不可变的（immutable），String 类定义的方法都不能改变字符串的内容，都是返回全新的字符串，而不是修改原字符串

1. 转义符

   \n 换行符    \\ \斜杠   \t tab缩进    \b 空格

2. 字符串方法

   - .length 返回字符串长度

   - 字符串+任何类型 = 拼接之后的字符串

   - charAt()  charCodeAt()  返回指定位置的字符和Unicode编码

   - indexOf() lastIndexOf()   形参：某个字符串  返回：传入字符串在该字符串中的位置

   - replace(regexp/substr, replacement)   用一些字符替换另一些字符，或替换一个与正则表达式匹配的子串。

   - 截取字符串

     - slice(start，end） 返回从start到end的新字符串，可为负数代表从尾部开始算起的位置。新字符串包含start不包含end
     - substring(start, end)  返回从start到end的新字符串，不能为负数
     - substr(start, length)   返回从start开始长度为length的子字符串，可为负数

   - split (separator,howmany)   separator字符串或正则表达式，从该指定的地方分割字符串  [howmany]返回的数组的最大长度

     该操作和Array.join( ) 执行的操作是相反的

   - toLowerCase() toUpperCase()  返回一个新字符串，转换为大写和小写

### 1.3 Boolean 

1. 有两个值 ture(真）和 false (假)
2. 布尔型和数字型相加的时候，true的值为1 false的值为0
3. undefiend，null，0，NaN, '' (空字符串)  转化为布尔值时为false

### 1.4 Undefined

1. 变量被声明了但是没有赋值会有一个默认值undefined

### 1.5 null

1. 一个变量给null值，里面存的值为空

### 1.6 获取变量类型

​	typeof 变量名

### 1.7 数据类型转换

1. 转换为字符串类型 String()强制转换   toString()     加号拼接字符串隐形转换
2. 转换为数字类型 Number()    parseInt()
3. 转换为布尔型 Boolean()

## 2.编程语言，标记语言

### 编程语言

有很强的逻辑和行为能力，有很多if else  while等具有逻辑性和具体行为能力的指令，是主动的

- 机器语言
- 汇编语言  与机器语言实质相同，直接对硬件进行操作。
- 高级语言
  - 解释型语言 ：在运行时时进行及时解释，并立即执行
  - 编译型语言：在代码执行前进行编译，生成中间代码文件

### 标记语言：

（html）不用于向计算机发出指令，是用来被读取的，被动的

## 3.运算符

### 3.1 算数运算符

	- 加减乘除取余
 - 注：
   - 浮点数的最高精度是17位小数，在计算时精度不足，不要直接判断两个浮点数是否相等
   - 除法所得结果不会进行自动取整，会返回浮点数

### 3.2 递增和递减运算符

++num  --num  先自加自减，再返回值

num++ num-- 先返回值，再自加自减少

### 3.3 比较运算符

- ==时会有隐形转换。全等用===

### 3.4 逻辑运算符

逻辑运算符是用来进行布尔值运算的运算符，其返回值也是布尔值。后面开发中经常用于多个条件的判断

- 逻辑与&&  两边都是true，则返回true，否则返回false
- 逻辑或||  两边都是false，则返回false，否则返回true
- 逻辑非！ 取反
- 注：短路运算：当有多个表达式时，左边的表达式值可以确定结果时,就不再继续运算右边的表达式的值
  - 逻辑与 &&
    - 如果第一个表达式的值为真，则返回表达式2   123&&456  //466
    - 如果第一个表达式的值为假，则返回表达式1    0&&456  //0
  - 逻辑或 ||
    - 如果第一个表达式的值为真，则返回表达式1  123&456  //123
    - 如果第一个表达式的值为假，则返回表达式2  0||456  //456

### 3.5 赋值运算符

- =  直接赋值
- +=   -+   *=  /=  %=  运算后再赋值，例如 age+=3    age=age+3

### 3.6 运算符优先级（从高到底）

小括号()         一元运算符++ --        算术运算符先*/%后+-     关系运算符> <    比较运算符== !==     逻辑运算符&& ||    赋值运算符=



## 4. 数组

### 4.1 创建数组

- 利用new  var 数组名 =  new Array()   如果传入的值为一个数，则是数组长度
- 利用数组字面量  var 数组名 = ["1",1,true]

### 4.2 获取数组中的元素

通过索引下标

### 4.3 遍历数组

for

### 4.4 新增删除元素元素

- push()  pop()  在元素尾部增加删除元素，分别返回数组长度和删除的元素

- unshift() shift()  在元素尾部增加删除元素，分别返回数组长度和删除的元素

- 数组.[数组.length] = 新数据



## 5. 函数与this指向

### 5.1 函数的定义方式

- 自定义函数方式（命名函数） function 函数名() { } 
- 函数表达式方式（匿名函数） var fun = function(){}
- var f = new Function(‘a'，’b', 'console.log(a+b)')

### 5.2 函数的参数

- 当形参和实参不匹配时。实参多于形参，只读取到形参个数； 实参少于形参，多的形参定义为undefined
- 当不确定有多少个参数传递时，可以不写形参。使用arguments来获取。arguments实际上是当前函数的一个内置对象。所有函数都内置了该对象。当中存储了传递的所有实参。arguments是一个为数组，可以进行遍历
  - 具有length属性
  - 按索引方式存储数据
  - 不具有数组的push pop方法

### 5.3 函数的调用以及this指向

| 调用方式 | 普通函数 |    对象方法    | 构造函数 |   事件绑定   | 定时器函数 | 立即执行函数 |
| :------: | :------: | :------------: | :------: | :----------: | :--------: | :----------: |
| this指向 |  window  | 该方法所属对象 | 实例对象 | 绑定事件对象 |   window   |    window    |

### 5.4  改变函数内部this指向

1. #### call()

   - 调用函数
   - 第一个参数为this指向的值，后面为参数

 2. #### apply()

    - 调用函数
    - 第一个参数为this指向的值，第二个参数为数组是函数的参数

 3. #### bind()

    - 不会调用函数，只会改变函数，返回改变函数this值之后的新韩淑

call经常用作继承，apply常与数组结合使用，比如借助数学对象实现数组最大值和最小值， bind不调用函数，但是改变this指向，可用于定时器内

## 6.作用域

### 6.1 作用域

- 全局作用域
- 局部作用域（函数作用域）
- 块级作用域（ES6）

变量的作用域：

全局变量：在任何一个地方都可以使用，只有在浏览器关闭时才会被销毁，因此比较占内存

局部变量：旨在函数内部使用，当其所在的代码被执行时，会被初始化

### 6.2 作用域链

只要是代码都一个作用域中，写在函数内部的局部作用域，未写在任何函数内部即在全局作用域中；如果函数中还有函数，那么在这个作用域中就又可以诞生一个作用域；根据在**[内部函数可以访问外部函数变量]**的这种机制，用链式查找决定哪些数据能被内部函数访问，就称作作用域链



## 7.预解析

### 7.1 预解析

``` 
JavaScript 代码是由浏览器中的 JavaScript 解析器来执行的。JavaScript 解析器在运行 JavaScript 代码的时候分为两步：预解析和代码执行。
```

- 预解析：在当前作用域下, JS 代码执行之前，浏览器会默认把带有 var 和 function 声明的变量在内存中进行提前声明或者定义。

- 代码执行： 从上到下执行JS语句。

  **预解析会把变量和函数的声明在代码执行之前执行完成。**

### 7.2 变量预解析

预解析也叫做变量、函数提升。
变量提升（变量预解析）： 变量的声明会被提升到当前作用域的最上面，变量的赋值不会提升。变量提升只提升声明，不提升赋值

### 7.3 函数与解析

### 7.4 函数表达式声明函数问题

函数表达式创建函数，会执行变量提升，此时接收函数的变量名无法正确的调用：   变量为undefiend   执行时会 is not a function



# 二、js高级

## 1.对象与类

### 1.1 创建对象

1. 利用字面量创建对象

   花括号里{ }包含了属性和方法，采用键值对

   ```  js
   var star = {
       name : 'pink',
       age : 18,
       sex : '男',
       sayHi : function(){
           alert('hello');
       }
   };
   ```

2. 利用new Object() 创建对象

   ``` js
   var andy = new Obect();
   andy.name = 'pink';
   andy.age = 18;
   andy.sex = '男';
   andy.sayHi = function(){
       alert('大家好啊~');
   }
   ```

3. 利用构造函数创建对象

   ```  
   function 构造函数名(形参1,形参2,形参3) {
        this.属性名1 = 参数1;
        this.属性名2 = 参数2;
        this.属性名3 = 参数3;
        this.方法名 = 函数体;
   }
   var obj = new 构造函数名(实参1，实参2，实参3)
   ```

   - 构造函数首字母大写

   - 构造函数内部的属性和方法要大写

   - 构造函数不需要return返回结果

   - 当我们创建对象的时候，必须要用new来构造函数

     new构造函数步骤：1.创建空对象，this指向该对象，对该对象属性进行赋值，返回这个对象 

### 1.2 类

- 在 ES6 中新增加了类的概念，可以使用 class 关键字声明一个类，之后以这个类来实例化对象。类抽象了对象的公共部分，它泛指某一大类（class）对象，通过类实例化一个具体的对象

#### 1.2.1 创建类 添加属性和方法

``` js
 // 1. 创建类 class  创建一个类
class Star {
    // 类的共有属性放到 constructor 里面 constructor是 构造器或者构造函数
    constructor(uname, age) {
      this.uname = uname;
      this.age = age;
    }//------------------------------------------->注意,方法与方法之间不需要添加逗号
    sing(song) {
      console.log(this.uname + '唱' + song);
    }
}
// 2. 利用类创建对象 new
var ldh = new Star('刘德华', 18);
console.log(ldh); // Star {uname: "刘德华", age: 18}
ldh.sing('冰雨'); // 刘德华唱冰雨
```

- 注意：
  1. 通过class 关键字创建类, 类名我们还是习惯性定义首字母大写
  2. 类里面有个constructor 函数,可以接受传递过来的参数,同时返回实例对象
  3. constructor 函数 只要 new 生成实例时,就会自动调用这个函数, 如果我们不写这个函数,类也会自动生成这个函数
  4. 多个函数方法之间不需要添加逗号分隔
  5. 生成实例 new 不能省略
  6. 语法规范, 创建类 类名后面不要加小括号,生成实例 类名后面加小括号, 构造函数不需要加function


#### 1.2.2 类的继承

``` js
class Father {
      constructor(surname) {
        this.surname= surname;
      }
      say() {
        console.log('你的姓是' + this.surname);
       }
}

class Son extends Father{  // 这样子类就继承了父类的属性和方法
}
var damao= new Son('刘');
damao.say();      //结果为 你的姓是刘
```

- 子类可以用super关键字访问父类方法

- 注意：

  1. 继承中,如果实例化子类输出一个方法,先看子类有没有这个方法,如果有就先执行子类的
  2. 继承中,如果子类里面没有,就去查找父类有没有这个方法,如果有,就执行父类的这个方法(就近原则)
  3. 如果子类想要继承父类的方法,同时在自己内部扩展自己的方法,利用super 调用父类的构造函数,super 必须在子类this之前调用

  4. 时刻注意this的指向问题,类里面的共有的属性和方法一定要加this使用.
     1. constructor中的this指向的是new出来的实例对象 
     2. 自定义的方法,一般也指向的new出来的实例对象
     3. 绑定事件之后this指向的就是触发事件的事件源

  5. 在 ES6 中类没有变量提升，所以必须先定义类，才能通过类实例化对象

### 1.2 遍历对象

可以使用for...in语句用于对数组或者对象属性进行循环操作

``` 
for (var k in obj) {
    console.log(k);      // 这里的 k 是属性名
    console.log(obj[k]); // 这里的 obj[k] 是属性值
}
```



## 2. 构造函数和原型

### 2.1 静态成员和实例成员

- 实例成员。构造函数内部通过this添加的成员，只能通过实例化的对象来访问
- 静态成员。在构造函数本身上添加的成员，只能通过构造函数访问

### 2.2 构造函数原型对象 prototype

- 每一个构造函数都有一个prototype 属性，指向另一个对象。注意这个prototype就是一个对象，这个对象的所有属性和方法，都会被构造函数所拥有。

- 我们可以把那些不变的方法，直接定义在 prototype 对象上，这样所有对象的实例就可以共享这些方法。

原型是什么？ 一个对象，我们也成为prototype为原型对象

原型的作用是什么？ 共享方法，节约内存空间

### 2.3 对象原型\____proto__\_\_

``` 
对象都会有一个属性 __proto__ 指向构造函数的 prototype 原型对象，之所以我们对象可以使用构造函数 prototype 原型对象的属性和方法，就是因为对象有 __proto__ 原型的存在。
__proto__对象原型和原型对象 prototype 是等价的
__proto__对象原型的意义就在于为对象的查找机制提供一个方向，或者说一条路线，但是它是一个非标准属性，因此实际开发中，不可以使用这个属性，它只是内部指向原型对象 prototype
```

### 2.4 constructor构造函数

``` 
对象原型（ __proto__）和构造函数（prototype）原型对象里面都有一个属性 constructor 属性 ，constructor 我们称为构造函数，因为它指回构造函数本身。
constructor 主要用于记录该对象引用于哪个构造函数，它可以让原型对象重新指向原来的构造函数。
一般情况下，对象的方法都在构造函 数的原型对象中设置。如果有多个对象的方法，我们可以给原型对象采取对象形式赋值，但是这样就会覆盖构造函数原型对象原来的内容，这样修改后的原型对象 constructor  就不再指向当前构造函数了。此时，我们可以在修改后的原型对象中，添加一个 constructor 指向原来的构造函数。
```

### 2.5 原型链

每一个实例对象又有一个\_\___proto__\_\_属性，指向的构造函数的原型对象，构造函数的原型对象也是一个对象，也有\_\___proto__\_\_属性，这样一层一层往上找就形成了原型链。

### 2.6 构造函数实例和原型对象三角关系

1.构造函数的prototype属性指向了构造函数原型对象
2.实例对象是由构造函数创建的,实例对象的\_\___proto\_\_属性指向了构造函数的原型对象
3.构造函数的原型对象的constructor属性指向了构造函数,实例对象的原型的constructor属性也指向了构造函数

### 2.7 原型链和成员的查找机制

任何对象都有原型对象,也就是构造函数的prototype属性,任何原型对象也是一个对象,该对象就有\_\___proto\___\_属性,这样一层一层往上找,就形成了一条链,我们称此为原型链;

``` 
当访问一个对象的属性（包括方法）时，首先查找这个对象自身有没有该属性。
如果没有就查找它的原型（也就是 __proto__指向的 prototype 原型对象）。
如果还没有就查找原型对象的原型（Object的原型对象）。
依此类推一直找到 Object 为止（null）。
__proto__对象原型的意义就在于为对象成员查找机制提供一个方向，或者说一条路线。
```

### 2.8 原型对象中的this指向

1. 在构造函数中,里面this指向的是对象实例 ldh
2. 原型对象函数里面的this 指向的是 实例对象 ldh（与情况1指向的是同一个对象）

### 2.9 通过原型为数组扩展内置方法

``` js
 Array.prototype.sum = function() {
   var sum = 0;
   for (var i = 0; i < this.length; i++) {
   sum += this[i];
   }
   return sum;
 };
 //此时数组对象中已经存在sum()方法了  可以始终 数组.sum()进行数据的求
 // 不能通过Array.prototype = { sum: f } 的方法，这样本来的reverse sort等方法就会不能使用
```

## 3. 继承

ES6之前没有extends继承，我们可以通过**构造函数+原型对象** 模拟实现继承，被称为组合继承

利用构造函数继承父类型属性，利用原型对象继承父类型方法

### 3.1 call

1. 调用这个函数     2.并且修改函数运行时的this指向  参数1是this要指向的对象 参数2，3...是函数的参数

``` js
 function fn(x, y) {
     console.log(this);
     console.log(x + y);
}
  var o = {
  	name: 'andy'
  };
  fn.call(o, 1, 2);//调用了函数此时的this指向了对象o,  this输出为对象o
```

### 3.2子构造函数继承父构造函数中的属性

1. 先定义一个父构造函数
2. 再定义一个子构造函数
3. 子构造函数继承父构造函数的属性(使用call方法)

```js
 // 1. 父构造函数
 function Father(uname, age) {
   // this 指向父构造函数的对象实例
   this.uname = uname;
   this.age = age;
 }
  // 2 .子构造函数 
function Son(uname, age, score) {
  // this 指向子构造函数的对象实例
  3.使用call方式实现子继承父的属性
  Father.call(this, uname, age);
  this.score = score;
}
var son = new Son('刘德华', 18, 100);
console.log(son);
```

### 3.3借用原型 对象继承方法

``` js
// 1. 父构造函数
function Father(uname, age) {
  // this 指向父构造函数的对象实例
  this.uname = uname;
  this.age = age;
}
Father.prototype.money = function() {
  console.log(100000);
 };
 // 2 .子构造函数 
  function Son(uname, age, score) {
      // this 指向子构造函数的对象实例
      Father.call(this, uname, age);
      this.score = score;
  }
// Son.prototype = Father.prototype;  这样直接赋值会有问题,如果修改了子原型对象,父原型对象也会跟着一起变化
  Son.prototype = new Father();
  // 如果利用对象的形式修改了原型对象,别忘了利用constructor 指回原来的构造函数
  Son.prototype.constructor = Son;
  // 这个是子构造函数专门的方法
  Son.prototype.exam = function() {
    console.log('孩子要考试');

  }
  var son = new Son('刘德华', 18, 100);
  console.log(son);
```

## 4.ES5新增方法

### 4.1数组

forEach(), map(), filter(), some(), every() 

- forEach遍历数组

  ```js
   arr.forEach(function(value, index, array) {
         //参数一是:数组元素
         //参数二是:数组元素的索引
         //参数三是:当前的数组
   })
    //相当于数组遍历的 for循环 没有返回值
  ```

  forEach里面的return不会终止迭代

- filter过滤数组

  ``` js
   var arr = [12, 66, 4, 88, 3, 7];
    var newArr = arr.filter(function(value, index,array) {
    	 //参数一是:数组元素
       //参数二是:数组元素的索引
       //参数三是:当前的数组
       return value >= 20;
    });
    console.log(newArr);//[66,88] //返回值是一个新数组
  ```

- some查找数组中是否有满足条件的元素

  ``` js
  some 查找数组中是否有满足条件的元素 
   var arr = [10, 30, 4];
   var flag = arr.some(function(value,index,array) {
      //参数一是:数组元素
       //参数二是:数组元素的索引
       //参数三是:当前的数组
       return value < 3;
    });
  console.log(flag);//false返回值是布尔值,只要查找到满足条件的一个元素就立马终止循环
  ```

  找到元素后就不会再检查后续的元素

### 4.2字符串

- trim()方法去除字符串两端的空格

  ``` js
  var str = '   hello   '
  console.log(str.trim()）  //hello 去除两端空格
  var str1 = '   he l l o   '
  console.log(str.trim()）  //he l l o  去除两端空格
  ```

  

### 4.3 对象

- Object.keys(对象) 获取到当前对象中的属性名 ，返回值是一个数组

  ```js
   var obj = {
       id: 1,
       pname: '小米',
       price: 1999,
       num: 2000
  };
  var result = Object.keys(obj)
  console.log(result)//[id，pname,price,num]
  ```

- Object.defineProperty设置或修改对象中的属性

  ```js
  Object.defineProperty(对象，修改或新增的属性名，{
  		value:修改或新增的属性的值,
  		writable:true/false,//如果值为false 不允许修改这个属性值
  		enumerable: false,//enumerable 如果值为false 则不允许遍历
          configurable: false  //configurable 如果为false 则不允许删除这个属性 属性是否可以被删除或是否可以再次修改特性
  })	
  ```

  

## 5. 严格模式的变化

### 5.1. 开启严格模式

1. 为脚本开启严格模式

   "use strict"放在script标签中

   (function(){"use strict"})()

2. 为函数开启

## 5.2 变化

1. 严格模式不能使用未声明变量
2. 不允许删除变量
3. 全局作用域下函数的this是undefined，函数的参数名要唯一
4. 构造函数不加new调用this指向的是undefined，给他赋值则会报错
5. 定时器指向的还是window

## 6 高阶函数



## 7.闭包

### 7.1 什么是闭包

闭包（closure）指有权访问另一个函数作用域中变量的函数。简单理解就是 ，一个作用域可以访问另外一个函数内部的局部变量。

### 7.2 闭包的作用

作用：延伸变量的作用范围。

### 5.4闭包的案例

1. 利用闭包的方式得到当前li 的索引号

```js
for (var i = 0; i < lis.length; i++) {
// 利用for循环创建了4个立即执行函数
// 立即执行函数也成为小闭包因为立即执行函数里面的任何一个函数都可以使用它的i这变量
(function(i) {
    lis[i].onclick = function() {
      console.log(i);
    }
 })(i);
}
```

2. 闭包应用-3秒钟之后,打印所有li元素的内容

```js
 for (var i = 0; i < lis.length; i++) {
   (function(i) {
     setTimeout(function() {
     console.log(lis[i].innerHTML);
     }, 3000)
   })(i);
}
```

3. 闭包应用-计算打车价格 

``` js
/*需求分析
打车起步价13(3公里内),  之后每多一公里增加 5块钱.  用户输入公里数就可以计算打车价格
如果有拥堵情况,总价格多收取10块钱拥堵费*/

 var car = (function() {
     var start = 13; // 起步价  局部变量
     var total = 0; // 总价  局部变量
     return {
       // 正常的总价
       price: function(n) {
         if (n <= 3) {
           total = start;
         } else {
           total = start + (n - 3) * 5
         }
         return total;
       },
       // 拥堵之后的费用
       yd: function(flag) {
         return flag ? total + 10 : total;
       }
	}
 })();
console.log(car.price(5)); // 23
console.log(car.yd(true)); // 33
```



## 7.ES6语法

### 7.1 let const var 的区别

- 使用 var 声明的变量，其作用域为该语句所在的函数内，且存在变量提升现象
- 使用 let 声明的变量，其作用域为该语句所在的代码块内，不存在变量提升
- 使用 const 声明的是常量，在后面出现的代码中不能再修改该常量的值

### 7.2 解构赋值

#### 数组解构

```javascript
 let [a, b, c] = [1, 2, 3];
 console.log(a)//1
 console.log(b)//2
 console.log(c)//3
//如果解构不成功，变量的值为undefined
```

#### 对象解构

``` js
 let person = { name: 'zhangsan', age: 20 }; 
 let { name, age } = person;
 console.log(name); // 'zhangsan' 
 console.log(age); // 20

 let {name: myName, age: myAge} = person; // myName myAge 属于别名
 console.log(myName); // 'zhangsan' 
 console.log(myAge); // 20

```

#### 小结

- 解构赋值就是把数据结构分解，然后给变量进行赋值
- 如果结构不成功，变量跟数值个数不匹配的时候，变量的值为undefined
- 数组解构用中括号包裹，多个变量用逗号隔开，对象解构用花括号包裹，多个变量用逗号隔开
- 利用解构赋值能够让我们方便的去取对象中的属性跟方法

### 7.3 箭头函数

() => {} //()：代表是函数； =>：必须要的符号，指向哪一个代码块；{}：函数体

```js
() => {} //()：代表是函数； =>：必须要的符号，指向哪一个代码块；{}：函数体
const fn = () => {}//代表把一个函数赋值给fn
```



函数体中只有一句代码，且代码的执行结果就是返回值，可以省略大括号 如果形参只有一个，可以省略小括号

#### 小结

- 箭头函数中不绑定this，zxxx箭头函数中的this指向是它所定义的位置，可以简单理解成，定义箭头函数中的作用域的this指向谁，它就指向谁
- 箭头函数的优点在于解决了this执行环境所造成的一些问题。比如：解决了匿名函数this指向的问题（匿名函数的执行环境具有全局性），包括setTimeout和setInterval中使用this所造成的问题

#### 面试题

### 7.4 剩余参数

剩余参数语法允许我们将一个不定数量的参数表示为一个数组，不定参数定义方式，这种方式很方便的去声明不知道参数情况下的一个函数

```javascript
function sum (first, ...args) {
     console.log(first); // 10
     console.log(args); // [20, 30] 
 }
 sum(10, 20, 30)

```

#### 剩余参数和解构配合使用

```js
let students = ['wangwu', 'zhangsan', 'lisi'];
let [s1, ...s2] = students; 
console.log(s1);  // 'wangwu' 
console.log(s2);  // ['zhangsan', 'lisi']

```

### 7.5 ES6 的内置对象扩展

#### 7.5.1Array 的扩展方法（★★）

##### 扩展运算符（展开语法）

扩展运算符可以将数组或者对象转为用逗号分隔的参数序列

```javascript
 let ary = [1, 2, 3];
 ...ary  // 1, 2, 3
 console.log(...ary);    // 1 2 3,相当于下面的代码
 console.log(1,2,3);
```

扩展运算符可以应用于合并数组

```javascript
// 方法一 
 let ary1 = [1, 2, 3];
 let ary2 = [3, 4, 5];
 let ary3 = [...ary1, ...ary2];
 // 方法二 
 ary1.push(...ary2);
```

将类数组或可遍历对象转换为真正的数组

```javascript
let oDivs = document.getElementsByTagName('div'); 
oDivs = [...oDivs];
```

#### 7.5.2 构造函数方法：Array.from()

将伪数组或可遍历对象转换为真正的数组

```javascript
//定义一个集合
let arrayLike = {
    '0': 'a',
    '1': 'b',
    '2': 'c',
    length: 3
}; 
//转成数组
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']
```

方法还可以接受第二个参数，作用类似于数组的map方法，用来对每个元素进行处理，将处理后的值放入返回的数组

```javascript
 let arrayLike = { 
     "0": 1,
     "1": 2,
     "length": 2
 }
 let newAry = Array.from(arrayLike, item => item *2)//[2,4]

```

注意：如果是对象，那么属性需要写对应的索引

实例方法：find()

用于找出第一个符合条件的数组成员，如果没有找到返回undefined

```javascript
let ary = [{
     id: 1,
     name: '张三'
 }, { 
     id: 2,
     name: '李四'
 }]; 
 let target = ary.find((item, index) => item.id == 2);//找数组里面符合条件的值，当数组中元素id等于2的查找出来，注意，只会匹配第一个

```

实例方法：findIndex()

用于找出第一个符合条件的数组成员的位置，如果没有找到返回-1

```javascript
let ary = [1, 5, 10, 15];
let index = ary.findIndex((value, index) => value > 9); 
console.log(index); // 2
```

实例方法：includes()

判断某个数组是否包含给定的值，返回布尔值。

```javascript
[1, 2, 3].includes(2) // true 
[1, 2, 3].includes(4) // false

```

#### 7.5.3 String 的扩展方法

模板字符串（★★★）

ES6新增的创建字符串的方式，使用反引号定义

```javascript
let name = `zhangsan`;

```

模板字符串中可以解析变量

```javascript
let name = '张三'; 
let sayHello = `hello,my name is ${name}`; // hello, my name is zhangsan
```

模板字符串中可以换行

```javascript
 let result = { 
     name: 'zhangsan', 
     age: 20,
     sex: '男' 
 } 
 let html = ` <div>
     <span>${result.name}</span>
     <span>${result.age}</span>
     <span>${result.sex}</span>
 </div> `;

```

在模板字符串中可以调用函数

```javascript
const sayHello = function () { 
    return '哈哈哈哈 追不到我吧 我就是这么强大';
 }; 
 let greet = `${sayHello()} 哈哈哈哈`;
 console.log(greet); // 哈哈哈哈 追不到我吧 我就是这么强大 哈哈哈哈

```

实例方法：startsWith() 和 endsWith()

- startsWith()：表示参数字符串是否在原字符串的头部，返回布尔值
- endsWith()：表示参数字符串是否在原字符串的尾部，返回布尔值

```javascript
let str = 'Hello world!';
str.startsWith('Hello') // true 
str.endsWith('!')       // true

```

实例方法：repeat()

repeat方法表示将原字符串重复n次，返回一个新字符串

```javascript
'x'.repeat(3)      // "xxx" 
'hello'.repeat(2)  // "hellohello"
```

#### 7.5.4 Set 数据结构（★★）

ES6 提供了新的数据结构  Set。它类似于数组，但是成员的值都是唯一的，没有重复的值。

Set本身是一个构造函数，用来生成  Set  数据结构

```javascript
const s = new Set();
```

Set函数可以接受一个数组作为参数，用来初始化。

```javascript
const set = new Set([1, 2, 3, 4, 4]);//{1, 2, 3, 4}

```

#### 实例方法

- add(value)：添加某个值，返回 Set 结构本身
- delete(value)：删除某个值，返回一个布尔值，表示删除是否成功
- has(value)：返回一个布尔值，表示该值是否为 Set 的成员
- clear()：清除所有成员，没有返回值

```javascript
 const s = new Set();
 s.add(1).add(2).add(3); // 向 set 结构中添加值 
 s.delete(2)             // 删除 set 结构中的2值   
 s.has(1)                // 表示 set 结构中是否有1这个值 返回布尔值 
 s.clear()               // 清除 set 结构中的所有值
 //注意：删除的是元素的值，不是代表的索引
```

#### 遍历

Set 结构的实例与数组一样，也拥有forEach方法，用于对每个成员执行某种操作，没有返回值。

```javascript
s.forEach(value => console.log(value))

```

