# TryWeexAndMVVM
Learn Weex and MVVM

### 整理一点点简单的前端
##### 标准的HTML的设计目的是提供静态的、纯文本的文档，脚本编程语言能够帮助HTML实现交互功能

##### 所有的HTML文件都有3个文档级标签：\<html>,\<head>,\<body>


* \<head>标签界定HTML文档的头部区域。文档的标题、元信息以及文档的脚本在多数情况下均包含在\<head>节。
* \<body>HTML文档中主要的可视部分包含在\<body>标签内。


##### MIME类型：
多用途互联网邮件扩展类型，即传输内容的分类类型

##### 分区（division）：
与段落有类似之处，用来将相关对象（段落、图片等）组织在一起，通过在分区上应用格式，还可以是组合在一起的对象继承大多数相同的格式，这样就省略了在其中每个对象上分别应用格式的需求

##### 有两类脚本：客户端脚本和服务端脚本

客户端脚本由客户端软件运行，即由用户代理运行。（JavaScript等）

服务端脚本由web服务器运行，通常被称为CGI(Common Gateway Interface)，是服务器端web脚本的第一个接口。（Perl, Python, PHP, Java等）

1、 在文档中包含脚本

要在文档中包含脚本，可将脚本代码写在\<script>标签中。可以在这个标签内包含任意数量的脚本代码，脚本可以包含在文档头或者文档体内，而且可以包含任意多个脚本区，但是在HTML内不能嵌套\<script>标签。

一般来说，应该讲脚本放在文档的头部区域，以便在后面加载的页面内容上使用脚本。

2、 调用外部脚本
如果希望多个文档内使用某些脚本，可以将脚本放在外部文件中，然后使用\<script>标签的src特性指定脚本内容再次文件内查找到。

##### CSS:Cascading Style Sheet 层级样式表

CSS级别1、2、3

* CSS1:定义了基本样式功能、有限的文字支持和有限的定位支持；
* CSS2:添加了声音属性、分页媒介、更好的字体支持和定位支持；
* CSS3:添加了演示样式属性，能够有效的用Web文档形成演示效果。

CSS按照一下方式引用声明的位置：

* 作者来源：文档作者通过\<style>区或者链接表（通过\<link>）包含样式；
* 用户来源：用户（文档的查看者）指定文本样式表；
* 用户代理来源：用户代理制定默认样式表（在不存在其他样式表的时候）。

当一个元素上存在多个样式的时候，CSS标准根据以下规则决定使用哪个样式： 
元素内嵌样式的优先级比前面声明的所有样式都高。

1. 找到对应在此元素上的来自所有来源的所有样式声明；
2. 对于普通声明，作者样式表覆盖用户样式表，后者又覆盖默认样式表。对于！important样式声明，用户样式表覆盖作者样式表，后者又覆盖默认样式表；
3. 较具体的声明比不太具体的声明优先；
4. 最后指定的样式比其他同级样式优先。


##### CSS基本格式：
```
selector {
	property: value(s);
	property: value(s);
	...
}
```
selector是可以用来与HTML文档中的特定元素进行匹配的表达式；

property指定此定义影响的元素属性；

value为属性分配值。



* 按类型匹配元素：普通元素选择器，所有对应对象都适用该定义中的属性-值进行格式化；
* 通用选择器匹配：可以用来和文档中的任意元素匹配，用*表示；
* 按类匹配元素：在样式选择器和对应的元素中使用不同的类，需要在选择器后加.类名，将一个给定的类与多个元素匹配；
* 按标识符匹配元素：根据id特性匹配，使用#+id作为选择器前缀；
* 按特定特性匹配元素：选择器与元素中的任意特性匹配，在选择器的末尾方括号中指定要匹配的特性和值；
* 匹配子元素、后代元素和相邻兄弟元素：根据与其他元素的关系进行匹配。