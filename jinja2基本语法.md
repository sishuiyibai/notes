### 基本用法
> #### 一. jinja2中，存在3中语法：
> 1. 控制结构:{% %}
> 2. 变量取值: {{ }}
> 3. 注释: {# #}
> 简单栗子：

>     {# 这是注释 #}
>     {% for file in filenames %}
>     ...
>     {% endfor %}
> #### 二. jinja2变量
> jinja2模版中使用{{}}占位符表示一个变量。支持python所有的数据类型如列表，字段，对象...
> 简单栗子:

>      <p>this is a dicectory:{{ mydict['key']}}</p>
> ### 三. jinja2中的过滤器
> 可将过滤器看作jinja2内置的函数和字符串处理函数，可对变量进行修改。
> 常用的过滤器：

![jinja2](images/2018-10-27 14-39-24 jinja2常用过滤器.png,"常用过滤器")
> 简单栗子：

>     {{ 'abc' | captialize }}
>     {{ 'abc' | upper }}
>     ...
> ### 四. jinja2的控制结构
> if语句：

>      {% if a %}
>      do something
>      {% elif b %}
>      do something
>      {% else %}
>      do something
>      {% endif %}
> for语句(jinja2中不存在while循环)：

>     <ul>
>     {% for user in users %}
>     <li><{{ user.username | title }}/li>
>     {% endfor %}
>     </ul>

> for 循环中，jinja2还提供了一些特殊变量，用于获取当前的遍历状态:
> ![jinja2](images/2018-10-27 15-40-50 for语句特殊变量,"for语句特殊变量")
>  ### 五. jinja2中的宏定义
> 宏定义的一个关键字是macro,后面跟其宏的名称和参数等
> 简单栗子：

>     {% macro input(name,age=30) %} # 参数age默认值为30
>     <input type='text' name="{{name}}" value="{{age}}" >
>     {% endmarco %}
> 调用方法:

>     <p>{{ input('daxin') }}</p>
>     <p>{{ input('daxin', age=20) }}</p>
> ### 六. jinja2的继承和Super函数
> 利用block关键字表示其包涵的内容可以进行修改。
> 简单栗子：

>      <!DOCTYPE html>
>      <html lang="en">
>      <head>
>          {% block head %}
>          <link rel="stylesheet" href="style.css"/>
>          <title>{% block title %}
>          {% endblock %} - My Webpage</title>
>          {% endblock %}
>       </head>
>       <body>
>       <div id="content">{% block content %}{% endblock %}</div>
>       <div id="footer">
>       {% block  footer %}
>       <script>This is javascript code </script>
>       {% endblock %}
>       </div>
>       </body>
>       </html>

>此处定义四处block,即：head,title,content,footer,继承和变量替换：

>     {% extend "base.html" %}
>     {% block title %}mytitle{% endblock %}
>     {% block head %}
>     {# 拥于获取原有信息 #}
>     {{ super() }}
>     <style type='text/css'>
>     .important {color: #FFFFFF}
>     </style>
>     {% endblock %}
>     super()函数用于获取block块中定义的原来的内容
>
