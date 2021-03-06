[TOC]

JavaScript对象表示法（JavaScript Object Notation，简称JSON）是一种轻量级的数据交换格式。它基于JavaScript的对象字面量表示法，那时JavaScript最精华的部分之一。尽管只是JavaScript的一个子集，但它与语言无关。所有以现代编程语言编写的程序，都可以用它来交换数据。它是一种文本格式，所以可以被人和机器阅读。它易于实现且易于使用。

## JSON语法

JSON有6中类型的值：对象、数组、字符串、数字、布尔值和特殊值null。空白（空格符、制表符、回车符和换行符）可被插到任何值的前后。这使得JSON文本能更容易被人阅读。为了减少传输和存储的成本，空白可以省略。】

JSON对象是一个容纳“名/值”对的无序集合。名字可以是任意字符串，值可以是任意类型的JSON值，包括数组和对象，JSON对象可以被无限层嵌套，但一般来说保持器结构的相对扁平是最高效的。大多数语言都有容易映射为JSON对象的数据类型。比如对象，结构，字典，哈希表，属性列表或关联数组

JSON数组是一个值的有序序列，其值可以是任何类型的JSON值，包括数组和对象，大多数语言都有容易映射为JSON数组的数据类型，比如数组，向量，列表或序列

JSON字符串被包围在一对双引号之间。\字符被用于转义，JSON字符允许/字符被转义，所以JSON可以嵌入HTML的\<script>标签之中。除非是\</script>标签，否则HTML不允许使用</字符串序列，但JSON可以使用<\/，它能产生同样的结果切不会与HTML混淆：

作者在这里所指的问题是：

```html
<script type="text/javascript">JSON={"foo": "</script>"}</script>
```

如上代码在浏览器中执行会导致脚本错误，加上\字符串进行转义即可

```html
<script type="text/javascript">JSON={"foo": "<\/script>"}</script>
```

JSON数字和JavaScript数字相似，整数的首位不允许是0，因为一些语言用它来标示八进制数。这种基数的混乱在数据交换中是不可取的。数字可以是整数、实数或科学计数

就是这样，这就是JSON的全部。JSON的设计目标是成为一个极简的、轻便的和文本式的JavaScript子集。实现互通所需要的共识越少，互通就越容易实现。

