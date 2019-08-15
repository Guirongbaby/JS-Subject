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
  function test1(){
    // 局部变量
    var b = 2;
    console.log(a,b);   //1,2
    function test2(){
      // 局部变量
      var c = 3;
      console.log(a,b,c);  //1,2,3
    }
    test2();
  }
  test1();
```

- 笔试 2

```js
if(typeof(a) && (-true) + (+undefined)+''){
 console.log('通过了！');//  打印 :通过了！
}else{
 console.log('没通过');
}
  console.log(typeof(a));// 打印：'undefined'
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
- 五、 函数类
+ 1
```js
var fn = (
  function test1(){
    return 1;
  },
  function test2(){
    return '2';
  }
)();
var num =  (1,2);

console.log(num); // 2

console.log(typeof(fn)); // string

// 逗号分隔符，返回的永远是最后一个！
```
+ 2
```js
var a = 10;

if(function b(){}){
  a += typeof(b);
}
console.log(a);// '10undefined'
```

+ 3
```js

```

+ 4
```js

```
+ 5
```js

```
+ 6
```js

```
+ 7
```js

```

