这是一段普通段落。

<table>
    <tr>
        <td>Foo</td>
    </tr>
    <tr>
        <td>Hello</td>
	<td>s</td>
    </tr>
</table>

&amp;&lt;&copy;AT&T;
4 < 5
4 &lt; 5

这是另一   段落

标题一
========
# 标题一
标题二
--------
## 标题二
> 区块引用
> > 区块引用Blockquotes

## 这是一个标题
>
>1.    这是第一行列表项
>2.    这是第二行列表项
>
>给出示例代码：
>
>     import numpy as np

## 列表
>1.    无序列表使用星号/ 加号或者减号作为列表标记:
* Red
* Green
* Blue
+  Red
+  Gree
+  Blue
- Red
- Green
- Blue
>2.    有序列表使用数字接着一个英文句点:
1. Red
2. Green
3. Blue
> 列表项中放进引用,则>需要缩进
	>list item with a blockqute:
	> This is a blockquote.
	> inside a list item.
> 放入代码区,则需要缩进两次,8个空格或2个制表符号
>
* 一个列表项包含一个列表区块:
         
		import numpy as np
1989\. what a great season
## 代码区块:
简单地缩进4个空格或1个制表符号
	
	import numpy as np
    import numpy as np
## 分隔线
一行中用三个以上星号/减号/底线来建立一个分隔线
***
* * *
---
_ _ _ _
## 区段元素
链接：行内式和参考式两种形式
链接文字都是用 [方括号] 来标记
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

链接到同样主机的资源，你可以使用相对路径：

See my [About](/about/) page for details.
参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：
This is [an example][id] reference-style link.
[id]: http://example.com/  "Optional Title Here"

## 强调
arkdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 < em > 标签包围，用两个 * 或 _ 包起来的话，则会被转成 < strong >，例如：

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
## 代码
如果要标记一小段行内代码，你可以用反引号把它包起来:
Use the `printf()` function.
## 图片
行内式的图片语法看起来像是：

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

详细叙述如下：
> 一个惊叹号!
> 接着一个方括号，里面放上图片的替代文字

> 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

## 其它
自动链接
Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用方括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：

<http://example.com/>

反斜杠
Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 <em> 标签），你可以在星号的前面加上反斜杠：

\*literal asterisks\*
Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：

\   反斜线
`   反引号
*   星号
*   _   底线
*   {}  花括号
*   []  方括号
*   ()  括弧
*   #    井字号
*   +   加号
*   -   减号
*   .   英文句点
*   !   惊叹号

