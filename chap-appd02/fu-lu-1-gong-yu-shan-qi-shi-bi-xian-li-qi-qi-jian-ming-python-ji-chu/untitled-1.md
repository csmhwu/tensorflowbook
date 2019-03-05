# 2.21 continue语句

continue语句是用来跳过当前循环的剩余语句，然后提前进行下一轮循环。

比如下面这个例子：

![&#x56FE;2-121](blob:https://minghuiwu.gitbook.io/063bdfa9-9756-4964-bd3e-b4bf9cc92b28)

我们先设了一个变量without9，它的初始值是一个空的字符串。

然后我们逐位判断，如果是9的话，就就会跳过下面的“without9 += digit”这条语句，如果不是9的话，这个without9这个字符串就会加上当前循环变量的数字变成一个新的字符串。因此，当程序结束的时候，得到的就是删除9之后的字符串。



## &gt; 示例代码

{% code-tabs %}
{% code-tabs-item title="1.py" %}
```python
# 求在2的100次方中删除所有的9后的数字:

num = 2**100
without9 = ''
for digit in str(num):
    if digit == "9":
        continue
    without9 += digit
print("2**100 is: %d \nwithout 9 is :%s" %(num,without9))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

