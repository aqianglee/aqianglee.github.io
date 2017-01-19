---
layout: article
tags: php
---
&emsp;&emsp;本文为php学习笔记，在本章中讲记录php嵌入到html中的方法，php中注释的方法，php中变量类型与变量声明以及流程控制等基本php语法。

### 嵌入php代码到html

&emsp;&emsp;嵌入php代码到html中有多种方法，具体如下：

```
<?
    echo "Hello World!";
?>
<br>
<?php
    echo "Hello World!"
?><br>
<?= "Hello World!"; ?>
<br>
<script language="php">
     echo "Hello World!"
</script><br>
```
&emsp;&emsp;以上四种方法都可以嵌入php代码到html中，并输入Hello World!字符串。

### php中的注释
&emsp;&emsp;在php中注释的方式也是多种多样的。有类似与c，c++那样的注释，也有类似与bash中那样的注释。

```
<?php
# 这是一行注释
// 这也是一行注释
/*
    这里都
      是
    注释
*/
# 下面才是代码
printf("测试注释");
?>    
```

### 向浏览器打印信息

&emsp;&emsp;php有很多可以打印消息到浏览器的方法。echo，print，printf等都可以打印消息到浏览器中。它们的用发大致相同,但也有一点区别。如下：

&emsp;&emsp;echo可以输出多条信息到浏览器，它接受参数是字符串，也可以是字符串数组。如果是字符串数组，逐个输出字符串。

&emsp;&emsp;print只能输出字符串。功能最小

&emsp;&emsp;printf不仅可以输出字符串，而且可以在字符串中设置占位符，并在后面的参数中给出，最后格式化成完整的字符串输出。类似c语言中的printf。

&emsp;&emsp;sprintf和printf相同，但是它将结果以返回值的形式保存在变量中，而不是输出到浏览器。

```
<?php
    echo "Hello World<br>";
    print "Hello World<br>";
    print("Hello World<br>");
    printf("Hello World<br>");

    echo "this is message1<br>", "this is message2<br>", "this is message3<br>", "this is message4<br>", "this is message5<br>";
    printf("there are %d messages<br>", 3);
?>

result:
Hello World
Hello World
Hello World
Hello World
this is message1
this is message2
this is message3
this is message4
this is message5
there are 3 messages
```
### php支持的数据类型
&emsp;&emsp;php支持的数据类型分为标量类型和复合数据类型。标量类型就是基本数据类型，包括布尔型，整型，浮点型，字符串。而复合数据类型包括数组和对象。

&emsp;&emsp;布尔类型可以赋值true，false或这数字非0即真。打印时，true会打印1，false打印0。如：
```
$result = true; //true
$result = false;//false
$result = 3;    //true
$result = -2;   //true
$result = 0;    //false
```
&emsp;&emsp;整数类型支持8进制，10进制，16进制。
```
$num = 15//10进制
$num = 0386//8进制
$num = 0xB6A4//16进制
```
&emsp;&emsp;浮点数就是小数，字符串也无特殊地方。

&emsp;&emsp;可以使用gettype函数来查看数据的类型，同时也可以使用settype函数修改类型，可以设置的数据类型有：integer,array,string,float,boolean,null,object共7种。
```
<?php
    function newLine() {
        echo("<br>");
    }
    $number = 3;
    echo gettype($number);
    newLine();
    echo $number;
    newLine();
    $str = "3";
    echo gettype($str);
    echo("<br>");
    echo("change number to boolean");
    newLine();
    settype($number, boolean);
    echo $number;
    newLine();
    $result = true;
    echo $result;
    newLine();
?>
result:
integer
3
string
change number to boolean
1
1
```
&emsp;&emsp;另外有is_array(), is_integer(), is_float(), is_boolean(), is_string(), is_resource(), is_null(), is_object()这8个函数来判定一个变量师傅为某种类型。

&emsp;&emsp;变量在实际运算环境种，会根据情况进行自动转换，规则合c差不多，php对变量类型的依赖不是很强，申明变量是连变量类型都不需要写，系统自动根据赋值内容推荐一种变量类型赋值给该变量，同过getype可以获取到变量类型。

### 变量
&emsp;&emsp;截至目前示例代码种已经有不少变量的申明了，但是还没有讲解变量申明的规则，变量必须以“$”开头来表示它是一个变量。和c不同的是，不需要变量类型。只需变量名，并赋值即可。变量名合法性与c相同。
