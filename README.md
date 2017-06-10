# js-prototype-chain
###  JavaScript 中，万物皆对象！但对象也是有区别的。分为普通对象和函数对象，Object ，Function 是JS自带的函数对象。下面举例说明

<br>```function f1(){};
<br>```var f2 = function(){};
<br>```var f3 = new Function('str','console.log(str)');

<br>```var o3 = new f1();
<br>```var o1 = {};
<br>```var o2 =new Object();

<br>```console.log(typeof Object); //function
<br>```console.log(typeof Function); //function
<br>```console.log(typeof o1); //object
<br>```console.log(typeof o2); //object
<br>```console.log(typeof o3); //object
<br>```console.log(typeof f1); //function
<br>```console.log(typeof f2); //function
<br>```console.log(typeof f3); //function 

 
  在上面的例子中 o1 o2 o3 为普通对象，f1 f2 f3 为函数对象。怎么区分，其实很简单，凡是通过 new Function() 创建的对象都是函数对象，
  其他的都是普通对象。f1,f2,归根结底都是通过 new Function()的方式进行创建的。Function Object 也都是通过 New Function()创建的。
