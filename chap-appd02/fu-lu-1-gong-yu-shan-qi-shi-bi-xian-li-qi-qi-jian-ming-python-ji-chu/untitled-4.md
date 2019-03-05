# 2.16 Python的行

Python中没有强制的语句终止字符。

Python语句中一般以新行（换行）作为语句的结束符。

下图中，我们命名了三个名称非常长的变量并赋了初值，然后做了一个三个变量的相加，但是这条语句写在同一行中会非常长，不方便看也不美观。

![&#x56FE;2-96](blob:https://minghuiwu.gitbook.io/f36586ff-ed45-49b0-88ed-0cc712a87bdb)

但是直接把一条长语句从中间断开成多行是不可行的（第一行的加号后面有换行符，默认这条语句已经结束了，但是实际上这是一条不完整的语句）：

![&#x56FE;2-97](blob:https://minghuiwu.gitbook.io/2e601027-92da-4aed-8217-eeebb161d90e)

如果想要不报错，可以使用反斜杠“\”把一行的语句分为多行显示（这个反斜杠就起到了多行之间的连接作用，相当于这条语句写在了很长的一行）：

![&#x56FE;2-98](blob:https://minghuiwu.gitbook.io/d86b27ca-a793-478a-bc1d-187540b0f596)

语句中包含“\[\]”，“{}”，“\(\)”，中间换行就不需要使用多行连接符：

![&#x56FE;2-99](blob:https://minghuiwu.gitbook.io/11d60d10-ea55-4f8a-903d-0892d3013f03)



## &gt; 示例代码

{% code-tabs %}
{% code-tabs-item title="1.py" %}
```python
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable1 = 1
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable2 = 2
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable3 = 3

#这一条语句写在一行太长了，不方便看也不美观
plusResult = thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable1 +thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable2 +thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable3

print(plusResult)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="2.py" %}
```python
#这样直接分成多行可是不行，要报错的
plusResult = thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable1 +
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable2 +
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable3

print(plusResult)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="3.py" %}
```python
#这样就对了可以使用斜杠（ \）将一行的语句分为多行显示
plusResult = thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable1 +\
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable2 +\
thisIsaVeryLongVariableNameSoCantWriteInOneLineVariable3

print(plusResult)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="4.py" %}
```php
days = ('Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday', 'Saturday', 'Sunday')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

