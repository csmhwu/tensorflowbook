# 2.20 break语句

Break语句用在while和for循环中，用来终止循环语句，即循环条件没有False或者序列还没有被完全递归完也会停止执行循环语句。

我们来看下面这个例子：

![&#x56FE;2-119](blob:https://minghuiwu.gitbook.io/b13c1854-f90c-4ba7-8c2e-74e7a4ebbff5)

2的100次方中其实是包含了多个9的，如果我们只是想找到第一个9，那么找到第一个之后后面就没有必要找下去了，所以我们就有必要把循环提前终止掉。

上图中的pos是一个记录位置的值，初始化为0。然后我们逐位判断，如果这位数字等于9就break，也就是提前跳出循环，这时pos所指向的位置就是当前数字9的位置。



如果有多重循环的话，break语句将停止执行的仅仅是本层的循环，并不是跳出整个的循环。

下图是求2到100间素数的例子：

![&#x56FE;2-120](blob:https://minghuiwu.gitbook.io/40acefc1-dd5f-4c59-8447-8e0dbd45d21f)

我们设了一个标记位flag，初始化为0。

如果i%j等于0，说明i能够整除j，i并不是素数，这时把标记位置为1并break退出循环，因为已经找到了能被它整除的数，就说明它不可能是素数了。然后我们再来判断flag，如果flag等于0，就说明没有任何一个数字可以被它整除，那么它就是一个素数。



## &gt; 示例代码

{% code-tabs %}
{% code-tabs-item title="1.py" %}
```python
# 统计第1个9在2的100次方中出现的位置:

num = 2**100
pos = 0
for digit in str(num):
    pos = pos + 1
    if digit == "9":
        break        
print("2**100 is: %d \nthe first posion of 9 is Pos.%d" %(num,pos))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="2.py" %}
```python
#求2到100之间的素数

i = 2
while(i < 100):
    flag = 0
    j = 2
    while(j <= (i/j)):
        if i%j==0: 
            flag = 1
            break
        j = j + 1
    if (flag == 0) : 
        print (i, " 是素数")
    i = i + 1
```
{% endcode-tabs-item %}
{% endcode-tabs %}

