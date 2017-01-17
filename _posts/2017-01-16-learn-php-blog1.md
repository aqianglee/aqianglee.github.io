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

&emsp;&emsp;php有很多可以打印消息到浏览器的方法。echo，print，printf等都可以打印消息到浏览器中。它们的用发大致相同，如下：

```

```
