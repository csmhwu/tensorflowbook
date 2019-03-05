# 2.17 流程控制

任何一门语言（当然也包括Python），它的程序结构都可以归纳为三种基本结构：顺序、条件（选择、分支）、循环。

![&#x56FE;2-100](blob:https://minghuiwu.gitbook.io/967dde83-6292-4b69-82fc-fc1c2064463a)

#### 

#### &gt; 条件语句

条件语句是用if这个关键词来标识的。

![&#x56FE;2-101](blob:https://minghuiwu.gitbook.io/1215a792-d923-40b6-acbf-e43610dd8086)

在Python里，代码块是通过缩进来指示的。

缩进代表一个代码块的开始，逆缩进则表示一个代码块的结束。

在if语句中，条件表达式后面会以冒号“：”字符来表示声明的结束，具体满足条件要执行的语句块就在后面以一个缩进开始跟进。

比如下图这个语句，第一次输入的体重为100，满足了条件，输出了print中的语句。而第二次输入的体重为70，不满足条件，不会执行冒号后面的语句：

![&#x56FE;2-102](blob:https://minghuiwu.gitbook.io/2243fc54-c91f-4509-912a-d73070cc9694)

如果在python中不严格遵守缩进的格式会报错：

![&#x56FE;2-103](../../.gitbook/assets/image%20%28100%29.png)

图中第二行多缩进了几个空格就提示了缩进错误，因为两条串行的语句不能在不同的缩进层次。

当条件不满足的时候，我们也有语句块需要执行的话，就要用到if else语句：

![&#x56FE;2-104](blob:https://minghuiwu.gitbook.io/05031ef2-5b80-4a7c-aaed-d1e1fb4369f8)

我们把刚才的例子做了一个扩展，这样当if中的条件不满足时，它将会执行else后面的语句块：

![&#x56FE;2-105](blob:https://minghuiwu.gitbook.io/9e2b791f-dcfe-4e56-b117-f0b94ee994e9)

有的时候一个if else语句可能还不足以说明情况，我们就需要用到else if语句：

![&#x56FE;2-106](blob:https://minghuiwu.gitbook.io/7d5aa8a5-351e-4d61-946e-274bfd2773b7)

我们来看一个计算BMI指数的例子：

![&#x56FE;2-107](../../.gitbook/assets/image%20%2894%29.png)

![&#x56FE;2-108](../../.gitbook/assets/image%20%28137%29.png)

![&#x56FE;2-109](../../.gitbook/assets/image%20%28167%29.png)

通过else if语句，我们完成了有三个分支选项的程序。如果情况更加复杂的话，我们也可以嵌套更多的else if语句。



#### &gt; 循环语句

Python提供了while循环和for循环。

循环语句允许执行一条语句或者语句块多次。

#### 

#### while循环语句：

![&#x56FE;2-110](blob:https://minghuiwu.gitbook.io/8a2aef40-3998-4cb9-8d86-95eac1a03b53)

下面我们来看一个具体的实例：

![&#x56FE;2-111](blob:https://minghuiwu.gitbook.io/9f73fb3f-f735-464a-8233-1b69ed200239)

这个程序中的count相当于一个计数工具，去统计6总共出现的次数**。**

在这个while循环中，我们通过对10取余的方法来逐位判断它是否等于6，如果相等，count就加一，每判断完一次就把末位数字除掉，然后在剩下的数字中继续统计6的个数，直到所有的数字都被判断完毕，这时num=0，不满足循环条件，程序结束。

#### 

#### for循环语句：

![&#x56FE;2-112](blob:https://minghuiwu.gitbook.io/4032814b-c1ee-4ebd-9d54-8fa0f754aa48)

图中的序列可以是一个列表也可以是一个集合。

它本质上就是把这个序列里面的每一个元素提取出来赋给循环变量，当这个序列被遍历完，也就是每一个元素都赋给循环变量然后去执行循环体，才会执行下一条语句。

刚刚用while循环实现的例子我们也可以用for循环来编写：

![&#x56FE;2-113](blob:https://minghuiwu.gitbook.io/fb832cb6-25ab-45c5-b9ce-e9c17b0aedd8)

图中的digit是一个循环变量，序列是转换成字符串后的2的100次方**。**

我们前面提过，字符串就是一个特殊的列表，每个字符串的元素都相当于列表中的一项，它执行的时候就是把列表里的每一项都赋值给digit，如果digit等于字符串6，count就加一。当这个循环结束的时候，也就意味着2的100次方这个长整数的每一位都去做了一遍这个if的测试，得到的结果跟while循环的结果是一致的。

在讲for循环的时候，还有一个用法，就是用for和range来枚举列表中的元素。

通过下图我们可以看到，它从0开始总共输出了10个数字（不包括10本身）：

![&#x56FE;2-114](blob:https://minghuiwu.gitbook.io/6b80567f-36cb-48dd-b430-9f00f9b8dd7b)

还有一种做法是指定上限和下限的区间（同样不包括10）：

![&#x56FE;2-115](blob:https://minghuiwu.gitbook.io/c69f616e-a556-41b6-beb7-7777d4a42053)



## &gt; 示例代码

{% code-tabs %}
{% code-tabs-item title="1.py" %}
```python
print("请输入体重（kg）：")
weight = float(input())

if weight > 90:
    print("胖子，该减肥啦！！！")
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="2.py" %}
```python
print("请输入体重（kg）：")
weight = float(input())

if weight > 90:
    print("胖子，该减肥啦！！！")
else:
    print("小样，身材保持的不错嘛！")
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="3.py" %}
```python
# 计算BMI指数

print("请输入体重（kg）：")
weight = float(input())
print("请输入身高（m）：")
height = float(input())

BMI = weight / height**2

if BMI < 20:
    print("你的BMI指数是%.2f,太轻了哟！" %BMI)
elif BMI > 25:
    print("你的BMI指数是%.2f,太重了哟！" %BMI)
else:
    print("你的BMI指数是%.2f,非常正常，请保持！" %BMI)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="4.py" %}
```python
# 统计6出现在2的100次方中的次数:
    
num = 2**100
print(num)

count = 0

while num > 0:
    if num % 10 == 6:
        count = count + 1
    num = num // 10

print(count)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="5.py" %}
```python
# 统计6出现在2的100次方中的次数:

num = 2**100
print(num)
count = 0
for digit in str(num):
    if digit == "6":
        count = count + 1

print(count)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="6.py" %}
```python
for i in range(10):
    print(i)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="7.py" %}
```python
for x in range(1,10):
    print(x)            #结果不包含最后的10
```
{% endcode-tabs-item %}
{% endcode-tabs %}

