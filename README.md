<!-- <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>面试笔试题</title>
</head>
<body>
  <script>
  a = 1;
  function test1(){
    // 局部变量
    var b = 2;
    console.log(a,b);//1,2
    function test2(){
      // 局部变量
      var c = 3;
      console.log(a,b,c);//1,2,3
    }
    test2();
  }
  test1();
  </script>
</html> -->

- 面试-笔试题 1

```js
a = 1;
function test1() {
  // 局部变量
  var b = 2;
  console.log(a, b); //1,2
  function test2() {
    // 局部变量
    var c = 3;
    console.log(a, b, c); //1,2,3
  }
  test2();
}
test1();
```

- 笔试 2

```js
if (typeof a && -true + +undefined + '') {
  console.log('通过了！'); //  打印 :通过了！
} else {
  console.log('没通过');
}
console.log(typeof a); // 打印：'undefined'
```

- 笔试 3

```js
console.log(!!' '+!!''-!!false || '未通过');
// 打印 1
 ———注意:第一个不是空字符串，这里是有空格的！
```

- 笔试 4

```js
window.a || (window.a = '1');
console.log(window.a);

// 括号的优先级最高,先算括号,括号里先进行赋值运算,window.a 为字符串 1
```

- 五、 函数类 之 笔试

* 1

```js
var fn = (function test1() {
  return 1;
},
function test2() {
  return '2';
})();
var num = (1, 2);

console.log(num); // 2

console.log(typeof fn); // string

// 逗号分隔符，返回的永远是最后一个！
```

- 2

```js
var a = 10;

if (function b() {}) {
  a += typeof b;
}
console.log(a); // '10undefined'
```

- 3

```js
var name = 'xiaoming';
name += 10; // 'xiaoming10'

var type = typeof name;
// var type = new String(typeof(name));

if (type.length === 6) {
  type.text = 'string';
  // newString(type).text = 'string';
  // delete
}

console.log(type.text); // undefined
```

- 4

```js
function Test(a, b, c) {
  var d = 1;
  this.a = a;
  this.b = b;
  this.c = c;

  function f() {
    d++;
    console.log(d); // 2 3 2
  }
  this.g = f;
  // return this; -> 闭包
}
var test1 = new Test();
test1.g();
test1.g();
var test2 = new Test();
test2.g();
```

- 5

```js
var x = 1,
  y = (z = 0);
function add(n) {
  // 被覆盖了
  return (n = n + 1);
}
y = add(x);

function add(n) {
  return (n = n + 3);
}
z = add(x);
console.log(x, y, z); // 1 4 4

// 详解：GO {
//   x = 1,
//   y = 0,
//   z = 0,
//   add:function add(n){
//     return n = n + 3
//   }
// }
```

- 6

```js
function foo1(x) {
  console.log(arguments);

  return x;
}
foo1(1, 2, 3, 4, 5); // 输出

function foo2(x) {
  console.log(arguments);
  return x;
}
1, 2, 3, 4, 5; // 不输出  函数声明后面不能跟 执行符号

(function foo3(x) {
  console.log(arguments);
  return x;
})(1, 2, 3, 4, 5); // 输出
```

- 7

```js
function b(x, y, a) {
  // a = 10;
  // console.log(arguments[2]); // 10  arguments是实参

  arguments[2] = 10;
  console.log(a); // 10
}
b(1, 2, 3);
```
