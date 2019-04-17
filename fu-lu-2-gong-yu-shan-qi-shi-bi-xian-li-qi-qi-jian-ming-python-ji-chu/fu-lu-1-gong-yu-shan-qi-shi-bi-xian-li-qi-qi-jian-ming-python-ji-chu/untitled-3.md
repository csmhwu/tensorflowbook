# 2.19 循环嵌套（多重循环）

这里有一个非常经典的例子——九九乘法表：

![&#x56FE;2-118](blob:https://minghuiwu.gitbook.io/6ae21523-3a7d-4ff4-adb8-06fbfe51cfe9)

for i in range\(1,10\)就说明它实际上有9个元素，会被执行9次。第一次会把1赋值给i，第二次把2赋值给i，一直到9。

在它循环体语句中的第一条语句依旧是for循环，此时形成了一个循环嵌套，它的循环变量是j，它的上限是i+1，而这个i就是外层循环中的循环变量i。当i等于1时，它的range就是（1，2），也就是说下面的循环体语句被执行一遍。

当执行完里面的循环后，还有一句“print（）”，看似没有做任何的输出，但是它起到了一个换行的作用。然后再开始i=2时的循环，这时的内循环将会被执行两次。依此类推，最终打印出一个完整的九九乘法表。



## &gt; 示例代码

{% code-tabs %}
{% code-tabs-item title="1.py" %}
```python
# 9*9乘法口诀表

for i in range(1, 10):
    for j in range(1, i + 1):
        result = j * i
        print('%s x %s = %-5s' % (j, i, result), end='' )
    print()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

