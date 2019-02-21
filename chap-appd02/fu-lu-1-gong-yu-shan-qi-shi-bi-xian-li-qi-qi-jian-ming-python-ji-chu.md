# 附录2 工欲善其事必先利其器：简明Python基础1

![](../.gitbook/assets/image%20%2824%29.png)

通过上图我们可以看到，在IEEE Spectrum 杂志上公布的2018年十大主流的编程语言中，Python排在第一位。它支持的应用类型很多，包括Web、PC桌面以及嵌入式的设备。

Python是一门面向对象编程语言，由荷兰人Guido van Rossum于1989年发明。Python主要发布了两个大的版本，分别是Python2和Python3，它们之间存在一定的差别。Python2和Python3之间有一些不兼容，像最基本的print输出语句也有一个很大的调整。

他们宣布将于2020年1月1日起停止对Python2的支持和维护。因此我们一般以Python3作为学习语言。



### &gt; 简单print用法

print在Python3中是一个函数，所以在使用的时候需要加“（）”，而在Python2中没有“（）”。

Python中是没有强制的语句终止字符的，所以大家不要像C语言一样，习惯性的以“；”结尾。

在Jupyter中，下图中绿框框的部分属于代码的单元，红框圈起来的地方就代表了绿色框的类型是Code。

因此，如果我们需要执行绿框中的语句，只需使用Ctrl+Enter就可以运行当前这条语句。

![](blob:https://minghuiwu.gitbook.io/67d654e2-0251-4dac-aae3-1f1bd779d313)

执行完毕之后，我们可以看到，在前面In的地方出现了一个序号，也就是执行序号。在灰框下面的空白处输出了结果“Hello world！”。![](blob:https://minghuiwu.gitbook.io/cb900fe4-291e-4bd4-9511-55d9fe72855f)

所以，在网页的模式下，我们可以比较好的实现编程和交互。输入输出都可以立马得到结果，这也是我们采用Jupyter来教学的主要原因。



在Python中，print默认输出是换行的，比如下图中，我们编写了两条print语句，可以看到这两条语句之间是有换行的。

![](blob:https://minghuiwu.gitbook.io/e73141ec-be0a-47c9-aa96-7b05a33fb3fe)

如果我们要实现print输出不换行，则需要指定结尾符“end=‘ ’”。这样的话，两条语句之间就没有换行了。

![](blob:https://minghuiwu.gitbook.io/3e1115c0-e1bf-4539-ad69-a4544c3e4fb2)

如果把两条语句放在同一个print中，用逗号分隔开来，得到的也是没有换行的输出，这样就不用像上图中指定结尾符那么麻烦了。

![](blob:https://minghuiwu.gitbook.io/7e94c426-babe-4325-9102-1983ebfe8fd8)

#### 

### &gt; 变量

每个变量在内存中创建，都包括变量的标识、名称和数据这些信息。

每个变量在使用前都必须赋值，赋值号是“=”

在Python中定义变量的时候不需要指明数据类型，所以直接写变量名就可以了，Python语言会自动根据你所赋的值的类型来决定它的数据类型，这也是它和其他程序设计语言的不同。

![](blob:https://minghuiwu.gitbook.io/7c847e8b-5c35-4b65-a241-4032f4992bfc)

如果我们想知道这些变量具体的数据类型，可以用“type（变量名）”来实现。

![](blob:https://minghuiwu.gitbook.io/578214af-4a46-4f86-8dca-b4b2497166fb)

这样我们就可以看到变量int\_a的值为5，数据类型是int。

由于我们现在在Jupyter中，每执行一行语句后面都要新增一个单元输入语句，所以我们可以用Shift+Enter键来执行。这样它就会执行当前的单元并进入下一个单元，如果后面没有的话，就会新增一个单元，也就是下图的样子。

![](blob:https://minghuiwu.gitbook.io/9e84d3d3-bc1a-480f-9eb5-207285ea8c3e)

#### 

### &gt; 标识符

在Python中，标识符由字母、数字、下划线组成。所有标识符可以包括英文、数字以及下划线“\_”，但不能以数字开头。

比如下图中，前两个变量的命名都没有问题，但是第三个变量以数字开头，因此出现了语法错误。

![](blob:https://minghuiwu.gitbook.io/9456cbfb-9fac-48fc-ba8f-fd63ff6296d2)

在Python中是大小写敏感的，也就是说上图中的x\_6和X\_6所指代的并不是同一个变量。如果它们所指代的是同一个变量，那么前一个值6.5就会被后一个值8所覆盖，根据下图我们可以看到它的值并没有被覆盖掉，所以它们是两个不同的变量。

![](blob:https://minghuiwu.gitbook.io/69225106-87fd-4ee6-b593-abd34f1b874a)

在Python3中是直接支持中文符号的，包括标识符名。

![](blob:https://minghuiwu.gitbook.io/384688c8-5e68-457a-9d43-a873ec17f062)

不过呢，在这里还是建议少用中文的变量名，这样局限性比较大，不便于和外国人进行交流。



### &gt; 保留字

所谓的保留字就是有特殊用途的标识。

它们不能用作我们用户自定义的常数、变数或者任何其他标识符名称。

所有Python的关键字只包含小写字母。

下图这张表中包含了Python中所有的保留字，大家在命名的时候要注意避开。

![](blob:https://minghuiwu.gitbook.io/01330b33-0b9d-4c63-b99b-7c15a74fd274)

#### 

### &gt; 数字数据类型

在Python中，数字数据类型用于存储数值。

它支持不同的数字类型：

int（有符号整型）缺省的是十进制的整型，还可以表示为二进制、八进制、十六进制的整型。Python3中不再保留以前有的长整型，统一为int。

float（浮点型）除了传统的写法，还可以用科学计数法表示。

complex（复数）由实数部分和虚数部分构成，可以用a+bj或者complex\(a,b\)表示。复数的实部a和虚部b都是浮点型。

0b、0o、0x分别代表二进制、八进制、十六进制数。

多条语句可以放在一行中，中间用分号“；”隔开来。

![](blob:https://minghuiwu.gitbook.io/82021837-748f-484c-b1f4-625ff7452df2)

我们在上图中定义的时候，分别用了二进制、八进制、十六进制去定义，但是输出的时候默认是以十进制输出，因此得到的结果就是2、8、16。

而且在定义三个变量的时候，我们把三条语句写在了同一行，因此中间需要用分号“；”隔开来。



Python还有一点非常好的地方就是它支持很长的整数。如果有学过C语言的同学就会知道，每一个数据类型它所支持的数据长度是有限的。

通过下图我们可以看到，var1没有损失任何的精确度，而它的类型仍然是int。

![](blob:https://minghuiwu.gitbook.io/8bc90848-2acc-4055-826d-bc94f538238e)



浮点数也有很多种表示方法，可以用科学计数法，也可以用常规的小数来表示。

![](blob:https://minghuiwu.gitbook.io/844a633f-ed87-4be9-a75a-95f49d024abc)



复数用我们刚刚提到过的两种方法都可以来表示，输出后都是以复数形式表示的，可以看到它的数据类型为complex。

![](blob:https://minghuiwu.gitbook.io/3f635e2e-b653-4ea3-9836-2b4612c2f47a)



### &gt; 布尔类型

还有一种特殊的类型是布尔类型，它只有两个值：真或假，也就是True或False。

![](blob:https://minghuiwu.gitbook.io/cb25b24d-1805-493b-92f1-73105f5fd05e)



### &gt; 注释

注释是写给人看的，为了方便程序的理解，可以当作是一个嵌在程序里的文档。对于计算机来说，注释会被忽略掉，不会被执行。在Python中有两种注释方法：

单行注释的话在最前面加上一个“\#”就可以了。

多行注释用三个单引号或者三个双引号把需要注释的话包在其中就可以了。

![](blob:https://minghuiwu.gitbook.io/0b7a158d-eab6-4b21-ba3e-09a5d3142d84)

我们可以看到，被注释掉的语句不会被输出，而且会变成斜体。

![](blob:https://minghuiwu.gitbook.io/47981a06-fbf8-4281-b4a3-aba036059edc)

多行注释可以一次把中间的三条语句都注释掉，因此只输出了头尾两条语句。上图中的单引号也可以改写成双引号，但是要注意前三个引号和后三个引号的类型要一致，否则也会报错。

### 

### &gt; 基本运算

#### &gt; 算数运算

算术运算符包括+，-，\*，/，//，%，\*\*。

以下假设x为10，y为3。

![](blob:https://minghuiwu.gitbook.io/d60a23d4-f6ba-4827-96fd-4e7d3745a6ff)

我们来看两个特殊的例子。

下图中变量a最终是float类型，这是为什么呢？

因为在做运算的时候，它会把运算符两边的数据类型转换成相同的数据类型，这里就是把int型向float型转换，所以最后得到的结果也是float型。

![](blob:https://minghuiwu.gitbook.io/8d5b98dd-4059-48bb-aa0f-c84aaf33ca63)

取余的时候，有些小细节也要注意：结果的符号和除数的符号是一致的。

![](blob:https://minghuiwu.gitbook.io/bf7010bf-ea85-417a-bb63-1bb965ce95d3)



#### &gt; 比较运算

比较运算符包括&gt;，&lt;，==，&lt;&gt;，&gt;=，&lt;=，!=。

比较运算的结果为布尔值，True或者False。

以下假设x为3，y为10。

![](blob:https://minghuiwu.gitbook.io/69ebbbcf-414b-4868-8c6e-e3f1aa9aefb3)

我们来看两个例子。

下图中3 == 3.0是成立的，因为如果把整数3转换成浮点数的3.0，对于值来说是没有损失的。但是3 == “3”就不成立了，因为“3”相当于字符串，字符串和数字是不能相等的。

![](blob:https://minghuiwu.gitbook.io/c2d90c9e-e890-42af-a48b-10dcedcba72f)

下图中涉及到一个先做算术运算还是先做比较运算的问题，我们可以根据结果看到，是先做算术运算的。我们可以得出一个结论：算术运算的优先级比比较运算高。

![](blob:https://minghuiwu.gitbook.io/3becdbe3-43b8-42e7-8ab5-ec26928c7008)



#### &gt; 赋值运算

赋值运算符包括=，+=，-=，\*=，/=，%=，\*\*=，//=。

![](blob:https://minghuiwu.gitbook.io/064ea312-21d6-4842-afb9-d95aa0bc9f2a)

这种写法确实比较简略，但是建议初学者呢，还是写的更加易懂一点，以免混淆。

这里有一个注意点：赋值运算符后面x要看成一个整体。

比如下图这个例子：

![](blob:https://minghuiwu.gitbook.io/42577e00-2a76-4c5d-94cb-37a7127910ae)

它先做了4+3的运算，得到了7，再跟10相乘，最后得到结果为70。

还有一个注意点：赋值的左边一定是一个变量。

如果写成下图的形式就会报错：

![](blob:https://minghuiwu.gitbook.io/a5fde9a4-30c7-4590-9169-e338367cee09)

这时候左边的z - 1是一个表达式，不能把9赋给一个表达式。如果右边是表达式的话就不会有问题。



#### &gt; 逻辑运算

逻辑运算符包括and，or，not。

![](blob:https://minghuiwu.gitbook.io/2692185f-7a34-42a4-a505-e630888bff44)

在逻辑运算中，0视作False，非0的值就视为True。

因此下图中的10就代表了True，结果就返回了y的计算值：20+5，也就是25。

![](blob:https://minghuiwu.gitbook.io/5d4e21f9-f787-46e6-94a3-2e3e5994eb89)

在逻辑运算中，False的值就是0，True的值就是1。

![](blob:https://minghuiwu.gitbook.io/553d7f91-f6de-4d78-880e-bc603e6c2af8)

![](blob:https://minghuiwu.gitbook.io/51f4792f-b23e-4f22-8338-bc915ba98c76)

但是有一点需要注意：在逻辑运算中，非0的值只是视作True，但并不等于True。只有1等于True。

因此，下图中的结果是False，说明5不等于True。

![](blob:https://minghuiwu.gitbook.io/0275f070-5500-4644-83bf-26e06bdff06f)



### &gt; 字符串

字符串可以用双引号引起来也可以用单引号引起来。并且你还能够在通过某一种标示的字符串中使用另外一种标示符（例如“He said ‘hello’.”）。而多行字符串可以通过三个连续的单引号或是双引号来进行标示。

可以看到下图中的三个变量的数据类型都是字符串。

![](blob:https://minghuiwu.gitbook.io/a0337b73-d9b2-44a7-8a28-c9ff9279befe)

如果想要输出的语句本身就带有双引号或单引号的，比如He said “hello”

不能写成下图的样子：

![](blob:https://minghuiwu.gitbook.io/6d4ef0e2-59fd-4a0e-ad4f-6ab3789695da)

因为在Python中，它的字符串是通过双引号来配对的，这样的话hello就不属于任何一对双引号之中，而且hello也不是变量或某个函数，因此出现了语法错误。

正确的写法应该是下面的样子（把里面的双引号改成单引号）：

![](blob:https://minghuiwu.gitbook.io/d7e9cc2e-d1c0-4f6c-9410-e2d12bec8567)

当然，把里外的单、双引号互换也是可以的，这样的话就得到了我们想要的输出。

![](blob:https://minghuiwu.gitbook.io/e88c9dcf-2e7c-4b37-b9cf-8367833fab4d)



在Python中，转义字符是反斜杠“\”，通常是由转义字符后面加上一个字母形成一个特殊的含义，比如“\n”是换行符。

在下图的print语句中只有一个字符串，但是它中间有一个换行符“\n”，所以它的输出是两个字符串。

![](blob:https://minghuiwu.gitbook.io/d663be11-af0a-40ea-924c-c2ffc7f29889)

如果你不想让反斜杠发生转义，可以在字符串前面添加一个“r”，表示原始字符串。

![](blob:https://minghuiwu.gitbook.io/e58ab7fc-f750-40c8-a176-e3d33e14933b)



我们如何来输出多行大段的文字呢？是不是需要许多的换行符呢？

其实答案是否定的，我们可以通过三个连续的单引号或是双引号来进行标示。

![](blob:https://minghuiwu.gitbook.io/7973db6b-a2aa-47c5-8ccf-d2184a7913d5)

由于在第二行和第三行字符串前面有许多的空格，所以输出的时候它也被当成字符原样输出。如果想要保持输出整齐的话，把前面的空格全都去掉就可以了。

![](blob:https://minghuiwu.gitbook.io/02fefff9-c704-4607-a042-3553be06de65)



接下来，我们来讲一下字符串的运算。

字符串可以用“+”进行链接：

![](blob:https://minghuiwu.gitbook.io/26055f80-9993-4730-92ae-f545a4f6a855)

字符串也可以用“\*”进行链接：

![](blob:https://minghuiwu.gitbook.io/2a0eb035-0fbb-4dca-8f8c-b541e9bccce0)

在Python中没有单独的单个字符类型，所以要注意字符串和数字之间的区别：

![](blob:https://minghuiwu.gitbook.io/eac6f907-a975-4d67-b2f9-36b062945006)

![](blob:https://minghuiwu.gitbook.io/1d228943-7018-417e-9ef1-c5a373b2c358)

数字的4+5得到的是9，而字符串的4+5是把这两个字符串连接起来。

![](blob:https://minghuiwu.gitbook.io/bef56e74-d369-434f-86ff-8c2733b6dddd)

如果把一个字符串加上一个数字，那么就会报错，因为这两个类型不能转换。



### &gt; 列表

列表（List）是Python中使用最频繁的数据类型。

列表写在方括号“\[ \]”之间，元素之间用逗号分隔开来。

![](blob:https://minghuiwu.gitbook.io/36f46fa4-ea9e-4f01-9702-e93e6b1c4802)

Python中的列表和传统C语言中的数组是不一样的，列表中元素的类型可以不相同，它支持数字、字符串甚至可以包含列表（即所谓的嵌套）。

![](blob:https://minghuiwu.gitbook.io/5f0d77f2-5ca0-4d09-8cd1-1479df132a6f)

列表元素的访问可以通过索引（下标）和截取（切片）。

列表被截取后返回一个包含所需元素的新列表。

注意：列表下标从0开始，-1表示倒数第一个。下标的访问不要越界（从0到列表长度-1）。

单个列表元素访问的语法格式为：列表名\[下标\]

List1\[0\]就代表了列表中的第一个元素1，List1\[2\]就代表了列表中的第三个元素3：

![](blob:https://minghuiwu.gitbook.io/3141bd16-4783-45e4-802f-8f81d716286c)

List1\[-1\]就代表了列表中的最一个元素6，List1\[-3\]就代表了列表中的倒数第三个元素4：

![](blob:https://minghuiwu.gitbook.io/d789a8f9-f1ac-4f00-a194-4b2c6d90c677)

列表截取的语法格式为：列表名\[头下标:尾下标\]

它会返回一个包含所需内容的新列表但不包括尾下标的那个元素。

List1\[0:3\]就返回了下标为0、1、2的元素：

![](blob:https://minghuiwu.gitbook.io/58fc7e9d-bda1-4eb6-9b9e-022775fc6704)

当然，我们也可以用负数来截取。

List1\[-3:-1\]就返回了倒数第三个和倒数第二元素：

![](blob:https://minghuiwu.gitbook.io/48a6b994-5a5d-4a6b-8ded-24850ffb9611)

在切片的时候，我们还可以设定切片的步长。

List1\[::2\]就表示不限制它的头和尾，但是每隔一个取一个数：

![](blob:https://minghuiwu.gitbook.io/6071caa3-4827-44fe-be26-3bdaa8364768)

接下来我们来看一下有关嵌套列表的访问。

这个时候采取的策略叫做“层层深入”。

比如我们想要访问下图红框这个列表中的元素，我们可以通过list2\[-1\]\[1:\]来获取：

![](blob:https://minghuiwu.gitbook.io/ba9dfa35-8d20-4810-9319-2d5d544cba82)

首先我们找到这个列表的位置是list2\[-1\]，然后再通过切片\[1:\]，获取这个列表中从第二个元素开始的所有元素，也就是9，10，11，12。

字符串是一种特殊的列表，我们可以按照访问列表元素的方法来访问字符串中的元素。

比如下图，我们通过切片的方式访问这个字符串中第三个字符到第五个字符：

![](blob:https://minghuiwu.gitbook.io/639a53e6-e1ab-428a-adc9-fa3420965bbd)



### &gt; 元组

元组（tuple）与列表类似，但它的不同之处在于元组的元素不能修改。

元组写在小括号“（）”里，元素之间用逗号分隔开来。

元组中元素的类型可以不相同，和列表类似，也支持嵌套。

![](blob:https://minghuiwu.gitbook.io/fb600082-fbfe-4682-b322-c2129c13d2d6)

元组的元素访问和截取方式跟列表相同，也可以通过下标来操作：

![](blob:https://minghuiwu.gitbook.io/21476963-468f-4beb-8c32-fec00d8ba436)

注意：元组一旦定义好不能被修改，是只读的，但是列表可以修改。

比如下图中，我们想修改tuple\[1\]的值就会报错，tuple这个对象是不支持直接赋值的：

![](blob:https://minghuiwu.gitbook.io/e4323b83-8883-4d57-9e18-0baa1c2b3e1a)



### &gt; 集合

集合（set）是一个无序且不含重复元素的序列。

集合主要用来进行成员关系测试和删除重复元素。

我们可以使用大括号“{}”或者set\(\)函数来创建集合。

我们可以看到下图中，在集合定义的时候，集合中是有重复元素的，但是它自动去除了重复元素：

![](blob:https://minghuiwu.gitbook.io/8a62ead7-9676-44d0-8e03-418a0aba84eb)

我们也可以使用“in”来判断元素是否在集合中：

![](blob:https://minghuiwu.gitbook.io/7828efa7-852b-4743-8ecd-e2ed5db1a2e2)

集合也有许多的操作：交（&）、并（\|）、差（-）、补（^）

![](blob:https://minghuiwu.gitbook.io/1050965a-0f88-4e53-a463-39e2fe71c912)

![](blob:https://minghuiwu.gitbook.io/2d634bba-2aa3-4833-9f5c-b14d7bc38f8c)

集合的补也可以用两个集合的并集减去两个集合的交集得到。



### &gt; 字典

字典（Dictionary）是一种映射类型，用“{}”标识，它是一个无序的 键（key）：值（value）对 集合。

键（key）必须使用不可变类型。在同一个字典中，键（key）是唯一的。

字典中元素是用过键来存取的。

下图中我们定义了一个有三项值的字典（冒号的前面是键，后面是值），如果我们要去读取字典中某一项的内容，我们需要根据字典的名字以及键去获取。比如下图中我们获取了“height”的值为176：

![](blob:https://minghuiwu.gitbook.io/88568d0a-41e7-4c56-98bc-8bc484dce858)

如果想要修改字典中某项的值，只需要重新赋值就可以了：

![](blob:https://minghuiwu.gitbook.io/580d0e87-2927-4fb0-bb3c-57dba01da337)

如果想要在字典中增加一项，可以通过“字典名\[键名\]=值”的形式增加：

![](blob:https://minghuiwu.gitbook.io/87680925-b56e-4cd4-a1ff-051795d73d2f)

构建一个空的字典可以通过下图的形式：

![](blob:https://minghuiwu.gitbook.io/16ffff7a-26d3-4291-9d85-be999feafc3b)

我们也通过元组序列构造字典：

![](blob:https://minghuiwu.gitbook.io/313b0a23-defa-4b73-afd6-0bc9317aa847)

我们也可以直接在构建元组的时候通过给某一个键赋值的方式来构造字典：

![](blob:https://minghuiwu.gitbook.io/fe2cbafa-d723-485d-88ee-49f203917d42)



字典类型中也有一些内置的函数，例如clear\(\)、keys\(\)、values\(\)

我们可以直接通过“字典名.函数名”的形式来引用：

![](blob:https://minghuiwu.gitbook.io/797675e3-ee80-4fa1-b8c2-5db010ce85dd)



### &gt; print的格式化输出

下图中展示了一些print的字符串格式化符号：

![](blob:https://minghuiwu.gitbook.io/fcbf844e-d94e-452a-99e3-aa8a5b65e626)

除了上述的这些，我们还有一些格式化操作符辅助指令：

![](blob:https://minghuiwu.gitbook.io/3b4490d8-4ee4-432c-9e2b-55a2930caadd)

下面我们来看一些具体的例子：

第一条语句中就是字符A，第二条语句中的虽然我们给出的值是65，但是它会被当成某一个字符的ASCII码，在这里呢，65表示的是大写的A，“%c”代表按照一个字符去输出，因此两条语句输出的值都是A：

![](blob:https://minghuiwu.gitbook.io/719b1dfb-ab80-4703-9bab-f443b81ea73d)

![](blob:https://minghuiwu.gitbook.io/bd6463b4-dc27-45bc-b7d4-ac50954651f2)

![](blob:https://minghuiwu.gitbook.io/13cea369-6956-4b1a-ba72-c992b856399c)

![](blob:https://minghuiwu.gitbook.io/7fd981e8-afc0-4fc1-8339-ef9db0d62579)

单纯的输出八进制或十六进制数我们是看不出来的，因此我们可以在前面格式的部分多加上一个“\#”，这样输出的时候可以更直观的分辨它是八进制、十进制还是十六进制数了。

![](blob:https://minghuiwu.gitbook.io/4a2e4d4e-9bc8-4d0b-8c64-042368cf68ce)

![](blob:https://minghuiwu.gitbook.io/106250c7-2331-4c2e-af0c-42dce55074a0)

“%f”如果没有指定小数点后的精度，它的默认精度是6位的：

![](blob:https://minghuiwu.gitbook.io/33e2f255-4c56-4dfd-81af-853de102c811)

![](blob:https://minghuiwu.gitbook.io/1978d77a-a3c3-40dc-8fc1-72375d497556)

当然还有一种更方便的方法是用“%g”，它会自动根据后面数字的大小决定它到底要输出多少，但是它所能表示的精度也是有限的：

![](blob:https://minghuiwu.gitbook.io/21c0a5a3-7425-4cd4-a98e-385c94138526)

下图的例子中，如果它本身的宽度就大于指定的值，那么就原样输出；如果小于指定的值，就会在前面补上空格（是右对齐的）：

![](blob:https://minghuiwu.gitbook.io/7a038b83-0da9-4bd9-8c70-e33636e2d1bd)

如果想要左对齐就要在前面加上“-”：

![](blob:https://minghuiwu.gitbook.io/7d678268-9199-4f1b-9cb8-d3ce9590fbc9)

如果想要在正数前面显示正号就要在前面加上正号，如果是负数，当然显示的还是负号：

![](blob:https://minghuiwu.gitbook.io/09601610-c9c1-4b76-8f3e-5799ef72a292)

下图中，后面元组中的5就代表了星号所在位置的数，也就是说对pi保留5位小数的精度：

![](blob:https://minghuiwu.gitbook.io/843e83a8-af1d-476f-bce9-f2763e2f1a77)

如果想要通过变量来填充格式控制字符串，那么可以使用运算符（%）和一个元组，在目标字符串中从左至右使用%来指代变量的位置。

比如下图中，元组中的第一个元素填充了%s的位置，而第二个元素填充了%.2f的位置（它的位置和元组中的顺序是一一对应的，如果类型不匹配将会报错）：

![](blob:https://minghuiwu.gitbook.io/dbd1d44f-33e9-48ef-aacb-e50a06f01bb6)

我们也可以使用字典来对应填充：

![](blob:https://minghuiwu.gitbook.io/1fb7e51b-cc4b-479f-b9ce-e674506096d2)



### &gt; 类型转化

数据类型的转换只需要将数据类型作为函数名即可使用。

这些函数返回一个新的对象表示转换的值，比如：int\(\)、float\(\)、str\(\)等等。

下面这个例子中，x原本是一个字符串6，我们通过int\(“6”\)把x的值转换成为int型的6：

![](blob:https://minghuiwu.gitbook.io/4315cc32-6d7f-4c9e-9aca-d7315630b53f)

同理，我们也可以把一个字符串转换成float，把int转换成字符串：

![](blob:https://minghuiwu.gitbook.io/aac40a31-3fb0-4084-8f14-ad13fb5676fb)

但是需要注意字符和数字的转换，字符是不能直接通过int\(\)转换成int型的，否则就会出现下图报错的情况：

![](blob:https://minghuiwu.gitbook.io/f08d9f82-f5ff-462e-81c2-759d368ca774)

字符和数字的转换可以通过ord\(\)和chr\(\)来实现：

![](blob:https://minghuiwu.gitbook.io/873a73a9-8cf8-46a3-ba26-a07a634c60f7)

![](blob:https://minghuiwu.gitbook.io/e5cc0703-fad5-4a7a-97d1-40c25f13e7eb)

我们之前学到过的元组、列表、集合之间也是可以相互转换的：

![](blob:https://minghuiwu.gitbook.io/affd9a4c-12a0-4da9-8ae7-f0eb4fcfe4fd)

当然，元组和字典之间也是可以相互转换的：

![](blob:https://minghuiwu.gitbook.io/9583d392-f550-41b8-bad5-0681c7becb9f)

最后我们来看一个超强的表达式计算（表达式字符串到数值的转换）：

![](blob:https://minghuiwu.gitbook.io/308ef576-5c1e-4323-8c6b-a9e3554a2f88)

通过eval\(\)函数，完成了这个表达式字符串的计算。



