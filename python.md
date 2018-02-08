            Helloword：

            ##常量/变量##
                    常量： 一旦赋值，就不可再改变换句话说，就是不能对它重新赋值。Python不存在常量
                    字面常量：一个单独出现的量，未赋值给任何变量或常量
                    变量： 是一个名字，在赋值符号的左边，这个名字可以指代赋值符号右边的内容
                    i=3

            ##类型系统##
                    Python是强类型语言
                    Python是动态类型语言
                    强类型： 指不同类型之间不能相互计算： 运算的时候会做类型检查
                    **动态类型**： 变量可以重新赋值为其他类型
            ##数据类型##
                    6中标准的数据类型：
                            数字(Number),字符串(String),列表(List),元祖(Tuple),集合(Sets),字典(Dictionary)
                    3中不同的数值类型：
                            整型(int),浮点型(float),复数(complex)
                                    整型：int通常被称为整型或整数,正负整数。整数没有限制大小，通常当做long型使用
                                    浮点型：整数部分和小数部分组合，也可以使用科学计数法表示
                                            Python3默认为小数10/3
                                    复数：实数部分和虚数部分组合
                    数据类型转换：
                            对数据内置的的类型进行转换，只需要将数据类型作为函数名即可
                                    int(x)      将x转换为一个整数
                                    fload(x)    将x转换为浮点数
                                    complex(x)  将x转换为复数，实数部分为x，虚数部分为0
                                    complex(x,y)将x转换为复数，实数部分为x，虚数部分为y，x和y是数字表达式


                    常量：PI：数学常量pi(圆周率)
                         E：数学常量e，即自然数

            ##运算符##
                    Python支持以下8中运算符：
                            算术运算符，比较运算符，赋值运算符，逻辑运算符，位运算符，成员运算符，身份运算符，运算符优先级

                    算术运算符
                    算术运算符只能对int和float运算

            ##比较运算符##
                    比较运算的返回值都是bool类型

            ##逻辑运算符##
                    逻辑运算符的操作数都是bool类型或者可以隐式转化成bool类型的类型, 返回值都是bool类型

            短路操作：
                    从左到右执行，当已经有结果的时候，将停止计算，提前返回
                    短路运算符就是我们常用的“&&”、“||”，一般称为“条件操作”
                    “&&”运算符检查第一个表达式是否返回“false”，如果是“false”则结果必为“false”，不再检查其他内容。
                    “||”运算符检查第一个表达式是否返回“true”，如果是“true”则结果必为“true”，不再检查其他内容。

                    运算符的优先级
                            算术运算 > 比较运算 > 逻辑运算
                            可以通过括号改变优先级
                            拿不准或者表达式比较复杂的时候，使用括号来决定优先级
                    ()  >   **  >   *   =   /   >   +   =   -   >   比较运算    >   逻辑运算
            赋值运算符

            ###通用序列操作###
                    数学上，序列是被排成一列的对象（或事件）
                    Python中所有的序列都可以进行一些特定操作：
                            索引(indexing),分片(slicing),序列相加(adding),乘法(mulyiplying)
                            成员资格,长度,最小值和最大值

                    ###索引###
                            序列是python中最基本的数据结构，序列中每个元素都有一个数字代表他的位置(索引)
                            索引从0开始，依次递增
                    ###分片###
                            索引是用来对单个元素的访问，使用分片可以对一定范围内的元素进行访问
                            分片通过冒号相隔的两个索引实现

                                lst[8]
                                lst[0:8]
                                lst[12:-1]
                                lst[-7:-1]
                            从左往右切片， 所以start要小于end
                                lst[12:3]
                            如果start 大于end， 将得到一个空列表
                                lst[-40: 100]
                            start 超出索引范围从0开始，end 超出索引范围到len(lst) 结束
                                lst[-40: 100]
                                lst[5:2:-1]
                            当step为负数的时候， 从后往前数， 此时 start应该大于end， 否则会返回空列表
                                lst[::-1]
                                lst[1::3]
                                lst[::2][::-1]
                                lst[-2::-2]
                                t[::-1]
                            lst[3:5] = [1, 2, 3]  替换相应索引对应的数据，如果值个数大于索引个数则添加，索引个数大于值个数，则报错
                                对切片赋值，会替换切片原来的元素
                                lst[3:8:2] = ['x', 'y', 'z']
                    ###序列相加###
                            使用加号可以进行序列的连接操作
                                [1,2,3]+[4,5,6]
                                ['a','b','c']+['d','e','f']

                    ###序列相乘###
                            使用*乘以一个序列会生成一个被重复*次的新的序列。用来创建一个重复的序列
                                'hello'*5       [7]*3
                            空列表可以使用两个中括号表示：[]
                            如果创建一个占用10个或更多元素的空间，却不包括任何有用内容的列表
                            可以使用Node.例如：sq=[None]*5
                            序列乘法做一些重复操作,空列表和None初始化操作
                    ###成员资格###
                            检查一个值是否在序列中，可以用in运算符，in检验某个条件是否为真，并返回检验结果
                            检验结果为真返回True，结果为假返回False，也叫布尔运算符
                                "h" in "hello"

                    ###长度，最小值，最大值###
                            len函数返回序列长度(序列中元素的个数)
                            max函数和min函数返回序列中最大和最小的元素
                                a='hello'
                                len(a)
                                max(a)
                                min(a)
            #####  列表： #######
                    列表是一个序列，用于顺序的存储数据
                    定义与初始化
                            lst = list()  # 使用list函数定义空列表
                            lst = []  # 使用中括号定义空列表
                            lst = [1, 2, 3] # 使用中括号定义带初始值的列表
                            lst = list(range(1, 10)) # 使用list函数把可迭代对象转化为列表
                    通常 在定义列表的时候，使用中括号， 在转化可迭代对象为列表时用list函数

                    访问列表元素
                             lst[0]  # 通过下标访问，下标从0开始
                             lst[10] # 当下标超出范围时， 会抛出 IndexError
                             lst[-1] # 负数索引从右边开始，索引从-1开始
                             lst[-11] # 负数索引超出范围，也会抛出IndexError

                             lst.index(4)  # 通过值查找索引
                             lst.index(2) # index 方法返回查找到的第一个索引
                             lst.index(2, 2) # start 参数指定从哪个索引开始查找,前面的第一个2是具体要查的列表内元素，
                                                     第二个2是指从第二个索引处往后查找，得出的结果也是索引位置。
                             lst.index(2, 2, 3) # end 参数指定到哪个索引结束， 并且不包含该索引 当值不存在该范围的时候，会抛出ValueError

                             start 和stop可以为负数， 但是总是从左往右查找
                             凡是stop比start小， 总是抛出ValueError

                             通过索引访问元素

                                    arts=input("请输入您的文章：")
                                    ooo=input("请输入您要替换的文字：")
                                    uuu=input("请输入你替换后的文字：")
                                    bbb=list(arts)
                                    counts=arts.count(ooo)
                                    lens=len(ooo)
                                    if lens == 1 :
                                        for i in range(counts):
                                            nums=bbb.index(ooo)
                                            bbb[nums]=uuu
                                            ccc=[]
                                            for i in bbb:
                                                for j in list(i):
                                                    ccc.append(j)
                                            for g in ccc:
                                                munss=ccc.count(g)
                                    else:
                                        print("Too long")


                    #### 修改 ####
                            lst[2] = 5  # 修改列表的元素直接使用下标操作取出元素并对其赋值
                            修改元素有且只有这一种方法
                            对超出范围的索引修改元素，会抛出IndexError

                        lst + ['a', 'b', 'c']  # 不修改list本身， 返回一个新的list  list 的连接操作


                    ###分片赋值###
                            分片赋值是列表强大的特性：
                            list函数可直接将字符串转换为列表，适用于所有类型的序列
                                    a="hi,I'm bob"
                                    b=list(a)
                                    b[3:3]="jeny"
                            任意位置插入元素不替换原元素
                    ###嵌套列表###
                            aa=['a','b','c']
                            bb=['d','e','f']
                            cc=[aa,bb]

                    ###列表方法###
                            对象.方法(参数)
                            1:append
                            2:count
                                    count 方法返回值在列表里出现的次数
                                    def count(lst, value):
                                        c = 0
                                        for x in lst:
                                            if x == value:
                                                c += 1
                                        return c

                            3:extend
                                    lst.extend([1, 2, 3]) # 原地修改 返回None
                                    append操作单个元素
                                    extend操作可迭代对象
                            4:index
                                    index方法根据值返回第一个索引
                                     count方法返回元素在列表里的个数
                                     index和count的时间复杂度是O(n) 线性复杂度 效率与数据规模线性相关

                            5:insert
                                    lst.append(9) # append 原地修改list， 返回结果是None
                                    lst.insert(1, 11) # insert 原地修改list， 返回None
                                    insert 当索引超出范围时
                                            索引是负数 会在第0个元素前插入
                                            索引是正数 会在最后一个元素后插入
                                            append的时间复杂度是O(1) 常数时间 效率和数据的规模无关
                                            insert的时间复杂度是0(n) 线性时间 效率和数据规模线性相关

                            6:pop
                                    pop 随机删除一个元素并返回， 集合为空，抛出KeyError
                                    lst.pop() # 返回并删除最后一个元素
                                    lst.pop(1) # 返回并删除索引所在位置的元素
                                    lst.pop(100) # 当索引不存在时， 抛出IndexError

                                    pop不传递index参数 时间复杂度是 O(1)
                                    pop传递index参数 时间复杂度是 O(n)
                                    pop 根据索引删除元素 并且会返回删除的元素
                            7:remove
                                    remove 删除给定的元素， 元素不存在抛出KeyError
                                    s.remove(0)
                                    s.remove(10) # 删除不存在的元素时， 抛出KeyError
                                    lst = [1, 2, 3, 2, 4, 3, 5, 3, 4]
                                    lst.remove(1) # 原地修改 返回None  根据值删除元素
                                    lst.remove(2) # 从左到右，删除第一个
                                    lst.remove(10) # 当值不存在时， 抛出ValueError
                                    remove 根据值删除元素， 返回None

                            8:reverse
                                    反向列表中的元素
                                    lst.reverse() # 原地修改，返回None 翻转列表
                            9:sort
                                    对原列表进行排序，若指定参数，即使用指定方法进行排序
                                    sort方法有两个可选参数，即key，reverse
                                    L.sort(key=None, reverse=False)
                                    lst.sort() # 原地修改， 返回None
                                    lst.sort(reverse=True)

                            10:clear
                                    clear 清空集合
                                    lst.clear() # 删除所有元素
                            11:copy
                                    lst = list(range(3))
                                    lst2 = lst
                                    赋值操作是传递是引用 也叫浅拷贝
                                        lst2 = lst.copy() # 影子拷贝

                                            def copy(lst):
                                                tmp = []
                                                for i in lst:
                                                    tmp.append(i)
                                                return tmp
                                    赋值操作，对可变对象是引用传递， 对不可变对象是值传递

                                    import copy
                                    lst2 = copy.deepcopy(lst)


                    ### 元组 ###
                            定义和初始化
                                    t = tuple()
                                    t = ()
                                    t = tuple(range(3))
                             元组是不可变的

                            ###查询###
                                下标操作
                                            t[0]
                                            t[-1]
                                            t[0] = 5 # 元组是不可变的
                            ###修改###
                                元组连接：（'a','b')+('c','d')
                            ###删除###
                                del删除整个元组
                                aaa=('a','b')
                                del aaa
                            ###索引，截取###
                                aa=('a','b','c')
                                aa[2]
                                aa[-2]
                                aa[1:]
                            ###内置函数###
                                len(),max(),min(),tuple()
                                t.index(2)
                                index方法和list表现一致
                                t.count(10)
                                count 方法和list表现一致
                            一般保证代码安全性，能用元组的尽量用元组
                            aa=('a','b',[1,2,3])
                            aa[2][2]=6
            ###字符串###
                    ###字符串的基本操作###
                            字符串是python中最常用的数据类型。所有标准序列操作(如索引,分片,成员资格,求长度,取最小值,最大值等)对于字符串同样适用
                            字符串是不可变的无法做分片复制
                            Python中的转义符：
                                    \在行尾时       续行符
                                    \n              换行
                                    \r              回车
                                    \e              转义
                                    \000            空
                    ###字符串格式化###
                            %f  :格式化浮点数
                            %s  :格式化字符串
                            %d  :格式化整数

                            ###字符串格式化符号###：
                                    print('hello,%s'%'word')
                                    print('小数点为：%2f'%3.14)
                                    print('百分号为：%s'%'%')
                                    print("hello,%s,i'm %d years old,i have $%010.2f"%('bob',3,21.98))
                                    填位符号：-,+,0
                               %字符：标记转换说明开始
                               转换标志(可选):    -表示对齐
                                                +表示在转换值之前加上正负号
                                                ""表示在正数之前保留空格
                                                0表示转换值位数不够时用0填充
                                    print('圆周率PI值为：%010.2f'%3.141593)

                            ###字符串格式化元组###
                                    print("hello {},you have {} yuan ".format('joy',4))

                                    指定参数：
                                    print("hello {name},you have {number} yuan ".format(name='joe',number=3))

                                    aaa=[1,2,3,4,5,6,7,8]
                                    print("hello {name},you have {number} yuan ".format(name='joe',number=aaa[4]))

                                    h1=lambda x,y: print("hello {name},you have {number} yuan".format(name=x,number=y))
                                    h1("joy",7)

                                    print("hello,%(name)s,you have %(number)s yuan"%{"name":"joey","number":3})

                            ###字符串方法###：
                                    ###find方法###
                                            find()方法用于检测字符串中是否包含子字符串str，可以指定范围内检测beg(开始)和end(结束)
                                            str.find(str,beg=-,end=len(string))

                                            s = 'i love python'
                                            s.find('love') # 从左往右查找， 找到第一个子串love， 返回子串首字母的索引
                                            s.find('love1') # 当子串不存在的时候， 返回-1
                                            s = 'i very very love python'
                                            s.find('very')
                                            s.find('very', 3) # start 参数指定从哪里开始查找
                                            s.find('very', 3, 10) # end 参数指定到哪里结束查找, end 不包含


                                    ###join()方法###
                                            join将序列中的元素以指定字符连接成一个新字符串

                                            lst = ['i',  'am', 'comyn']
                                            ' '.join(lst) # join是字符串的方法，参数是内容为字符串的可迭代对象， 接收者是分隔符
                                            ','.join(lst)

                                    ###lower()方法###
                                            lower()方法将字符串中所有大写字符转换为小写字符
                                            str1 = "THIS IS STRING EXAMPLE....WOW!!!";
                                            str1.lower()    --->   this is string example....wow!!!

                                    ###upper()方法###
                                            upper()方法将字符串中的小写字母转换为大写字母
                                            str = "this is string example....wow!!!";
                                            str.upper()    ---> "THIS IS STRING EXAMPLE....WOW!!!"
                                    ###swapcase()方法###
                                            swapcase()方法用于对字符串的大小写字母进行转换，大写转小写小写转大写
                                            str = "THIS is STRING example....wow!!!";
                                            str.swapcase()    ---> "this IS string EXAMPLE....WOW!!!"
                                    ###replace()方法###只能从前往后替换
                                            str.replace(old,new[,max]
                                            s = 'i love python'
                                            s.replace('love', 'give up') # 返回新字符串，使用new替换old
                                            s = 'i very very love python'
                                            s.replace('very', 'not') # 有多少个替换多少个
                                            s.replace('very', 'not', 1) # 可选的count参数，指定替换多少次
            ###集合###
                    元素是唯一的 元素是无序的
                            s = {} # 不能这么定义空集合
                            s = set(1,2,3)  或者   s = {1,2,3}

                            1：增加集合元素
                                    add
                                    s.add(4)   给具体的值
                                    当add一个已经存在的元素时， 不会发生任何改变
                                    update
                                    s.update([3,4,5,6])

                                    list set bytearray dict 是不可hash的，所以不能作为set的元素，通常来说，内置类型，
                                                            不可变类型是可hash的，可变类型是不可hash的

                                    a = bytearray(3)

                            2：删除
                                    remove
                                    discard
                                    pop
                                    clear

                                    s = {1,2,3,4}
                                    s.remove(2)    删除具体的值
                                    s.discard(2)
                                    remove 删除不存在的元素会抛出KeyError， discard删除不存在的元素不会发生任何事情

                                    pop返回的元素是无序的 空集合pop的时，抛出KeyError异常

                                    修改和查找
                                    没有一个方法可以直接的修改集合中的某个具体元素
                                    因为没有一个方法，可以定位其中某个具体元素
                                    for x in set('magedu'): # 集合是可迭代对象
                                        print(x)
                                        'm' in set('magedu')  # 集合可以用成员运算法  线性结构的成员运算，时间复杂度是 O(n) 集合的成员运算，时间复杂度是O(1)
                                        O(1)
                                        常数复杂度
                                        O(logn)
                                        对数复杂度
                                        O(n)
                                        线性复杂度
                                        O(n ^ 2)
                                        平方复杂度
                                        O(n ^ 3)
                                        O(2 ^ n)
                                        指数复杂度
                                        O(n!) 阶乘复杂度

                            3：集合的集合运算
                                    union
                                    intersection
                                    difference
                                    symmetric_difference

                                    a = {1, 2, 3}
                                    b = {2, 3, 4}
                                    a.union(b) # 并集   --->   {1, 2, 3, 4}
                                    a.intersection(b) # 交集   --->   {2, 3}   --- a & b
                                    a.difference(b) # 差集   --->   {1}  --->   a - b
                                    b.difference(a) # 差集   --->   {4}  --->   b - a
                                    a.symmetric_difference(b) # 对称差集   --->   {1,4}

                                    a.intersection_update(b)   --->   a   {2,3}
                                    没有 union_update
                                    update版本的集合运算 原地修改集合，返回值为None

                                    a.issuperset(b)    --->   true       超集
                                    b.issubset(a)   --->   true   子集

                                    isdisjoint 判断两个集合是否不相交

                                    a.isdisjoint(b)   --->  False
                                    a.isdisjoint({5, 6})   --->   True
                                    元素需要唯一而对顺序没有需求
                                    我们需要集合运算时
            ###字典的使用###
                    ###创建和使用字典###
                            d={key1:value1,key2:value2}
                            键唯一，值可不唯一
                    ###dict函数###
                            使用dict()函数通过其他映射(如其他字典)或键/值序列对建立字典
                                    aaa=[("a",1),("b",2)]
                                    dict(aaa)
                            dict()函数将序列转换为字典
                            dict()函数可以通过关键字参数创建字典：
                                    student=dict(name1='jeny',name2='bob')
                    ###字典的基本操作###
                            修改，删除等操作
                            ###修改字典###
                                    添加新内容：增加新键值对，修改或删除已有键值对
                                            student={'name1':'bob','name2':'jeny'}
                                            student['name2']='charry'
                                            print('My name is %(name1)s'%student)
                                            student['name3']='anny'
                            ###删除字典###
                                    此处的删除是显示删除，显示删除一个字典用del命令
                                            student={'name1':'bob','name2':'jeny','name3':'anny'}
                                            del student['name1']
                                            del student
                                    d.pop(0) # pop 方法用于从字典删除一个key， 并返回其value
                                    d.pop(0) # 当删除不存在的key的时候， 会抛出KeyError
                                    d.pop(0, 'default') # 当删除不存在的key， 并且指定了默认值时， 不会抛出KeyError， 并且返回默认值
                                    d.pop(1, 'default') # 有没有default， 是在key不存在的时候才有所区别
                                    d.popitem() # popitem **随机** 返回并删除一个kv对的二元组
                                    d.clear() # clear 方法清空一个字典
                                    d.popitem() # 对空字典popitem， 将抛出KeyError
                            ###字典键的特性###
                                    字典值可以没有任何限制的取任何Python对象，既可以是标准对象，
                                            也可以是用户自定义对象，但是键不允许
                                    同一个键不允许出现两次，后面重复出现的键的值会覆盖前面出现过的键
                                    键必须不可变，可以使用数字，字符串或元组充当，不能使用列表
                            ###len()函数###
                                    len(dict)函数用于计算字典元素的个数，即健的总数
                                    student={'name1':'bob','name2':'jeny'}
                                    print('The key numbers is:%d'%len(student))
                            ###type()函数###
                                    type(variable)函数返回输入的变量类型，如果输入变量是字典就返回字典类型
                                            student={'name1':'bob','name2':'jeny'}
                                            type(student)
                    ###字典的格式化字符串###
                            student={'name1':'bob','name2':'jeny'}
                            print('My name is %(name1)s'%student)
                            复习元组的格式化：
                                    students=('bob','jeny')
                                    print("my name is %s,he name is %s"%students)
                            字典和列表的特点：
                                    dict特点：
                                            查找和插入速度极快，不会随着key的增加而变慢
                                            需要占用大量内存，内存浪费
                                    list特点：
                                            查找和插入时间随着元素的增加而增加
                                            占用内存小，内存浪费很少
                                    dict是空间换时间
                    ###字典方法###
                            ###clear()方法###
                                    clear()方法用于删除字典内所有的项
                                    dict.clear()
                                            x={}
                                            y=x
                                            x['key']='value'
                                            x={}
                                    此时y还有值若使用x.clear()，则y也被清空
                            ###copy()方法
                                    copy方法返回一个具有相同键值对的新字典，这个方法叫浅拷贝
                                    与列表相同，浅拷贝会受原变量的影响，而深拷贝则不会
                                    复习列表：
                                             a=[1,2,3]
                                             b=a.copy()
                                             c=a
                                             import copy
                                             d=copy.deepcopy(a)
                                             a.clear()
                                    此时，a和c被清空
                            ###fromkeys()方法###
                                    fromkeys()方法用于创建一个新字典，以序列seq中的元素做字典的键
                                              value为字典所有键对应的初始值
                                    dict.fromkeys(seq[,value]))
                                            此语法中dict代表字典，seq代表字典键值对，value代表可选参数
                                            设置序列(seq)的值，该方法返回结果为列表
                                    name=('anny','bob','cindy')
                                    namber=dict.fromkeys(name)
                                    print('The new dict is %s'%namber)
                                        The new dict is {'anny': None, 'bob': None, 'cindy': None}
                                    namber=dict.fromkeys(name,10)
                                    print('The new dict is %s'%namber)
                                        The new dict is {'anny': 10, 'bob': 10, 'cindy': 10}
                                    对于初始化数据的默认值有用
                            ###get()方法###
                                    get()方法通过key访问value,访问不存在的key的时候返回默认值None
                                            student=dict(name1='jeny',name2='bob')
                                            print("The name1 is %s"%student.get("name1"))
                                    当key不存在时自定义返回值
                                            student=dict(name1='jeny',name2='bob')
                                            print("The name3 is %s"%student.get("name3","No Such User"))
                            ###setdefault方法()
                                    与get方法类似，用于获得与给定键相关联的值，如果键不存在于字典
                                            就会添加键并将值设置为默认值
                                    dict.setdefault(key,default=None)
                                            student=dict(name1='jeny',name2='bob')
                                            print("The name3 is %s"%student.setdefault('name3'))
                                    此时字典已更新并设置name3的值为None
                                            student=dict(name1='jeny',name2='bob')
                                            print("The name4 is %s"%student.setdefault('name4','Joey'))

                            ###key in dict方法###
                                    in操作符用于判断键是否在字典中，存在返回true，不存在返回false
                                            student=dict(name1='jeny',name2='bob')
                                            print("The name1 in student  %s"%('name1' in student))
                            ###items()方法###
                                    items()方法以列表返回可遍历的(键值)元组数据
                                            for x in d.items():
                                                print(x)
                                            for k, v in d.items():
                                                print(k, v)
                                            student.items()
                                                dict_items([('name1', 'jeny'), ('name2', 'bob')])
                            ###keys()方法###
                                    keys()方法以列表方式返回一个可迭代对象， 元素是字典所有的key
                                    keys， values， items 返回的都类似生成器, 它并不会复制一份内存
                            ###values()方法###
                                    d.values() # values 返回一个可迭代对象， 元素是字典的所有value
                            ###update()方法###
                                    dict.update(dict2) 将dict2中的元素更新到dict里面
                                    d.update([('g', 333), ('h', 4444)])    由二元组构成的可迭代对象
                                    d.update(i=555)  关键字参数
                                    update 的参数可以是以下几种情况：
                                            字典
                                            由二元组构成的可迭代对象
                                            关键字参数
                                            update时，如果key相同，会覆盖原来的value



            ###条件，循环其他语句###：
                    ###import语句###
                                    import module[,module2[,...moduleN]]
                                    import math
                                    r=5
                                    print('半径为5的圆的面积为：%2f'%(math.pi*r**2))
                            当使用import的语句时，Python解释器会在他的搜索路径里面搜索，被存储在sys模块的path变量中
                                    import sys
                                    print("The python's path is %s"%sys.path)

                                    from math import pi
                            从模块中导入指定部分到当前命名空间中,而不会全部导入
                                    frommodname import name1[,name2,name3]
                                    import math
                                    print(math.pi)
                                    print(math.sin(1))
                                    print(mathexp(1))
                            ###调用函数###
                                    import math
                                    print(math.pi)
                                    from math import pi
                                    print(pi)
                                    from math import *      ###不建议这样写，不利于代码清晰性
                                    print(pi)
                                    frim math import sin,pi
                            ###为模块取名###     as语句
                                    import math as m
                                    m.pi
                            ###为函数取别名###
                                    from math import pi as p
                                    p
                            ###使用逗号输出###
                                    str1="Hi,Everybody"
                                    str2="My name is bob"
                                    str3="The wether is very god!"
                                    print(str1,str2,str3)
                            以逗号分割多个表达式
                    ###别样的赋值###
                            ###序列解包###
                                    ###定义多个变量###
                                            x,y,z=1,2,3
                                            x,y=y,x     ###交换值
                                    将多个值的序列解开，然后放入变量序列中
                                            nums=1,2,3
                                            x,y,z=nums      ##获得序列解开的值
                                    ###例子###
                                            student={"name1":'anny',"name2":'bob',"name3:'cindy'}
                                            key,value=student.popitem()
                                    序列解包允许函数返回一个以上的值并打包成元组，然后通过复制语句进行访问
                                    序列解包的元素数量必须和放置在赋值符号"="左边的数量完全一致，否者异常
                            ###链式复制###
                                            x=y=z=10
                                    通过多个等式为多个变量赋同一个值，这种方法叫链式复制，同一值赋值多个变量
                            ###增量复制###
                                            x=x+1 ---> x+=1
                                    将表达式放置在赋值运算符(-)的左边，这种写法叫做增量复制
                                            *,/,+,-,%
                                    增量复制除了适用于数值类型，还适用于二元运算符的数据类型
                                            'field'='hello'
                                            'field'+='word'
                                            'field'*=2
                    ###语句块###
                            语句块是一组满足一定条件时执行一次或多次的语句
                            ###条件语句###
                                    ###布尔变量的作用###
                                            布尔变量对应的是布尔值
                                            下面的值在作为布尔表达式时，会被看做假
                                                    False,None,(),"",(),[],{}
                                                    True == False
                                                    True == 1
                                                    False == 0
                                            布尔值True和False属于布尔类型，bool函数转换其他值
                                                    bool('Good idea')
                                                    bool("")
                                                    bool({})
                                                    bool([0])
                                                    bool([1])
                                                    bool('Good idea') == 0
                                                    bool('Good idea') == 1
                                                    aa=[]       ##判断是否为空值
                                                    bool(aa)

                                                    bool([])=bool({})=bool("")=False
                                            所有的值都可以用作布尔值(真假)
                                    ###if语句##
                                            真值可以联合使用
                                                    name1='anny'
                                                    if name1 == 'anny':
                                                        print('true')
                                    ###else子句###
                                            在else后没有判断语句
                                                    name1='anny'
                                                    if name1 == 'anny':
                                                        print('true')
                                                    else:
                                                        print('false')
                                    ###elif子句###
                                            多个判断
                                                    name1=10
                                                    if name1 > 2:
                                                        print('大于2')
                                                    elif name1 < 5:
                                                        print('小于5'))
                                                    else:
                                                        print('等于2或5')
                                    ###嵌套代码块###
                                            num=10
                                            if num%2==0:
                                                if num%3==0:
                                                    print("整除2和3")
                                                elif num%4==0
                                                    print("整数2和4")
                                                else:
                                                    print("可以整除2，但不能整除3和4")
                                            else:
                                                if num%3==0:
                                                    print("整除3，不能整除2")
                                                else:
                                                    print("不能整除2和3")
                                    ###更多操作###
                                            ###is###
                                                同一性运算符：
                                                    x=y=[1,2,3]
                                                    z=[1,2,3]
                                                    x==y     ###True
                                                    x==z     ###True
                                                    x is y   ###True
                                                    x is z   ###False
                                                值相等但不是同一个对象==判断是否值相等,is判断是否为同一对象
                                            ###比较字符串和序列###
                                                    字符串按照字母排列顺序进行比较，其他序列比较的不是字符而是元素的其他类型
                                                    例如：
                                                            [[1,2]<[2,1]
                                                            [2[1,2]]<[2[1,3]]
                                            ###布尔运算符###
                                                    and  or  not  ---> 逻辑运算符
                                                    and运算符连接两个布尔值，两者皆为真时为真，否则为假
                                                    短路逻辑(惰性求值): x and y 如果x为假，则不在进行y的运算
                                                    例如：
                                                            if num <=10 and num >=5:
                                                                print("The num between in 10 and 5 "

                                    ###断言###
                                            在Python有一个与if语句相近的关键字，其工作方式如下伪代码：
                                                    if not condition:
                                                            crash program
                                            在未完善程序之前，无法得知程序哪里会出错，与其在运行时崩溃，
                                                    不如在出现错误条件时就崩溃。
                                            一般来说，可以要求一些条件必须为真。在Python中，assert关键字能实现这种方式
                                            例如：
                                                    x=3
                                                    assert x > 0,"x is not zero or negative"    ###条件为真，正常运行
                                                    assert x%2 == 0,"x is not an even number"   ###条件为假，输出错误信息
                                            这个错误信息也叫异常参数。assert的异常参数是在断言表达式后添加的字符串信息
                                                    用来解释断言并更容易知道问题所在
                                            使用assert断言时，要注意一下几点：
                                                    1：assert断言用来声明某个条件是真的
                                                    2：如果你非常确信所使用的列表中至少有一个元素，想要检验这一点并在他非真时引发一个错误
                                                            那么assert语句应该应用在这种情况下
                                                    3：assert语句失败时，会引发一个AssertionError
                    ###循环###
                            循环语句允许我们多次执行一个语句或语句组
                            ###while循环###
                                    n=1
                                    while n <=100:
                                        print(n)
                                        n+=1
                            ###for循环###
                                    开始
                                    for 元素 in 可迭代对象:
                                       操作
                                    结束
                                    例如：
                                        n=0
                                        fields=['a','b','c']
                                        while n < len(fields):
                                            print("The now fields is fields[n]")
                                            n+=1
                                for in 循环里永远不要修改可迭代对象
                                能用for尽量不要用while

                            ###迭代工具###
                                    在Python中，迭代序列或其他可迭代对象时，可用一下函数
                                    ###并行迭代###
                                            zip函数用来进行并行迭代
                                            例子1：
                                                    aa=[1,2,3]
                                                    bb=['a','b','c']
                                                    for k,v in zip(aa,bb):
                                                        print(" ip is %s,secret is %s"%(k,v))
                                            例子2：
                                                    aa=[1,2,3]
                                                    bb=['a','b','c']
                                                    for k in range(len(aa)):
                                                        print('ip is',aa[k],',secret is',bb[k])
                                            例子3：
                                                    for k,v in zip(range(3),range(5)):
                                                        print(k,v)
                                            zip函数作用于任意数量的序列，短序遍历完成时循环结束
                                    ###翻转和排序迭代###
                                            reversed,sorted函数：可作用于任何序列或可迭代对象，但不是原地修改，而是返回翻转或排序后的版本
                                                    sorted("hello,word")
                                                    list(reversed("hello,word"))
                                            sorted函数返回的是一个列表，reversed返回的是一个可迭代对象
                                    ###跳出循环###
                                                    break,continue语句
                                            ###break###
                                                    终止循环语句，即使没有遍历完
                                                    例子1：
                                                            for i in range(10):
                                                                if i == 5:
                                                                    break
                                                                    print(i)
                                                    例子2：
                                                            i=10
                                                            while i > 5:
                                                                print(i)
                                                                i-=1
                                                                if num == 6:
                                                                    break

                                            ###continue##
                                                    跳过当前循环的剩余语句，执行下一轮循环
                                                    例子1：
                                                            for i in range(5):
                                                                if i == 3:
                                                                    continue
                                                                print(i)
                                                    例子2：
                                                            i=3
                                                            while i >0:
                                                                i-=1
                                                                if i == 2:
                                                                    continue
                                                                print(i)
                                                            i等于3时跳过了下面的print函数，直接进行下一轮循环
                                            ###循环中的else语句###
                                                    1：在while条件语句中使用else
                                                            i=10
                                                            while i > 5:
                                                                print(i)
                                                                i-=2
                                                            else:
                                                                print(i)
                                                    2:在for循环中使用else语句
                                                            a=list(range(5))
                                                            for i in a:
                                                                if i == 6:
                                                                    print(i,"等于3")
                                                                    break
                                                                print(i,"不等于3")
                                                            else:
                                                                print("最后一个数字是",i,"循环结束")
                                                    break 和 continue只针对最近的一层
                                                    break和continue只能用在循环里
                                            ###pass语句###
                                                    Python中的pass是空语句，作用是保持程序结构的完整性
                                                    i=list(range(5))
                                                    if i == 3:
                                                        print(i)
                                                    if i == 4:
                                                        pass ###预留，不做处理

                                                    number=input("Please input your name:")
                                                    aa=list(number)
                                                    lens=len(aa)
                                                    bb=0
                                                    for i in aa:
                                                        bb+=int(i)**lens
                                                    if bb == int(number):
                                                        print(bb)
                                                    else:
                                                        print("error")

                            ###迭代器###
                                    可迭代对象：列表、元组、集合、字典、字符串、bytes、bytearray和生成器 都是可迭代对象
                                    可迭代对象可用于for in表达式, 可以使用成员运算符(in 和not in)

                                    iter 函数把一个可迭代对象、封装成迭代器
                                    r = range(10)
                                    it = iter(r)
                                    迭代器是一种封装
                                    for in 隐式的调用了iter 成员运算符也隐式的调用了iter函数
                                     当迭代器没有下一个元素的时候，next函数会抛出StopIteration异常
                                    next(it, 3)
                                    当有默认值的时候返回默认值
                                    生成器对象同时也是迭代器

                                            it = iter(lst)
                                            it = iter(lst)
                                            lst = [
                                                ['温度', 28, 29, 32, 35, 30, 29, 27],
                                                ['湿度', 30, 35, 45, 50, 39, 35, 30]
                                            ]
                                            for seq in lst:
                                                it = iter(seq)
                                                name = next(it)
                                                print(name)
                                                for x in it:
                                                    print(x)

                                     可迭代对象
                                     迭代器
                                     iter 函数把可迭代对象转化为迭代器
                                     next函数从迭代器里取出元素  迭代器是一类对象



                    ###解析式###


                            ###生成器解析###
                                    生成器解析能做的列表解析都能做，但数据量较大是列表解析比较耗内存
                                    对列表解析来说，只需要简单的把中括号换成小括号就可以了
                                    生成器解析式是按需计算的或者说延迟计算的或者叫惰性求值

                                            [inc(x) for x in range(10)]
                                            g = (inc(x) for x in range(10))
                                            next(g)
                                    生成器是一个返回迭代器的函数，只能用于迭代操作，更简单点理解生成器就是一个迭代器。
                                    在调用生成器运行的过程中，每次遇到 yield 时函数会暂停并保存当前所有的运行信息，返回yield的值。
                                    并在下一次执行 next()方法时从当前位置继续运行。
                                            def gen():
                                               yield 0
                                               g = gen()
                                               type(g)
                                               next(g)

                                            def gen():
                                                while True:
                                                    yield 0
                                                    print('.....')
                                    生成器的定义和函数类似，但是有yield语句
                                    生成执行到yield的时候会暂停， 在此next会从暂停的地方继续执行

                                            def gen(x):
                                                for i in range(x):
                                                    yield x
                                            g = gen(10)
                                            for x in g:
                                                print(x)

                                    yield 弹出值，暂停函数
                                    return返回值， 并且结束函数

                                            def gen(x):
                                                for i in range(10):
                                                    if i == 3:
                                                        return i
                                                    yield i
                                            g = gen(10)
                                            for x in g:
                                                print(x)
                                    当yield和return同时存在时， return的返回值会被忽略，但是return依然可以中断生成器
                                            def gen(x): # 生成器函数  返回值是一个生成器
                                                for i in range(x):
                                                    yield i
                                                return 'ok'
                                            for x in gen(10):
                                                print(x)
                                    协程是用户空间的轻量线程， 跑在一个线程内，由用户空间调度
                                            def gen1():
                                                while True:
                                                    yield 'gen 1'

                                            def gen2(g):
                                                for x in range(10):
                                                    yield 'gen 2'
                                                    print(next(g))
                                            g = gen2(gen1())
                                            next(g)

                                            def g(n):
                                                def factorial():
                                                    ret = 1
                                                    idx = 1
                                                    while True:
                                                        yield ret
                                                        idx += 1
                                                        ret *= idx
                                                gen = factorial()
                                                for _ in range(n-1):
                                                    next(gen)
                                                return next(gen)

                                        使用生成器来替换递归
                                        所有的递归，都可以用生成器替换
                                        生成器可以用来做缓存，会保存线程状态信息
                                            def cache(x):
                                                ret = x + 1
                                                idx = 0
                                                while True:
                                                    yield ret
                                                    idx += 1
                                                    if idx > 5:
                                                        ret = x+1
                                                        idx = 0
                                    py2:
                                            def gen(lst):
                                                for x in lst:
                                                    yield x

                                    py3:
                                            def gen(lst):
                                                yield from lst  # => for x in lst: yield x
                                            g = gen(range(10))
                                            for x in g:
                                                print(x)
                                    个人经典生成器例子:

                                            def aa(a):
                                                for i in range(a):  ###print函数无法返回函数值
                                                    print(i)

                                            def aa(a):
                                                bb=[]
                                                for i in range(a):
                                                    bb.append(i)
                                                return bb       ##使用return函数返回函数值
                                            for j in aa(6):
                                                print(j)
                                            此时，函数在运行中占用的内存会随着参数a的增大而增大，如果要控制内存占用，最好不要用 List

                                            def aa(a):
                                                for i in range(a):
                                                    yield i
                                            for j in aa(6):
                                                print(j)
                                            gg=aa(6)
                                            next(gg)
                                            此时，使用yield语句来控制内存大小
                                    在一个 generator function 中，如果没有 return，则默认执行至函数完毕，
                                    如果在执行过程中 return，则直接抛出 StopIteration 终止迭代。
                            ###yeild from###
                                    允许生成器将其部分操作委托给另一个生成器。这允许将包含的代码段分解并放置在另一个生成器中。
                                    此外，允许子生成器返回一个值，并将该值提供给委托生成器
                                            def g(x):
                                                yield from range(x)
                                    但是，与普通循环不同的是，允许子生成器直接从调用范围接收发送和抛出的值，并将最终值返回给外部生成器




                            ###列表解析### 快速高效生成列表方法
                                    代码变短，可读性强,解析式速度更快

                                    plus_one = []
                                        for x in range(10):
                                            plus_one.append(x+1)

                                    x+1 for x in range(10)

                                    列表解析的一般形式
                                    [expr for item in itratorable]
                                    x+1 for x in range(10)
                                    列表解析返回的是列表， 列表的内容是表达式执行的结果

                                    [x for x in range(10) if x % 2 == 0]
                                    [x for x in range(10) if x % 2 == 0 if x > 1]
                                    [x for x in lst if len(x) > 1 and x.pop(0) % 2 == 0]
                                    [(x, y) for x in range(10) for y in range(10)]


                                    [x for x in range(2) for x in range(3)]
                                    [{x+1:x+2} for x in range(5)]
                                    [(x+1, x+2) for x in range(5)]
                                    列表解析用于对可迭代对象做过滤和转换，返回值是列表
                            ###集合解析###
                                    {x for x in range(10)}
                                    集合解析把列表解析的中括号变成大括号，返回集合
                                    type({x for x in range(10)})
                                    type([x for x in range(10)])

                            ###字典解析###
                                    {str(x):x for x in range(10)}
                                    字典解析也是使用大括号包围，并且需要两个表达式，一个生成key，
                                        一个生成value 两个表达式之间使用冒号分割，返回结果是字典
                                    {str(x):y for x in range(3) for y in range(4)}

                                            ret = {}
                                            for x in range(3):
                                                for y in range(4):
                                                    ret[str(x)] = y

                                     为什么没有元组解析？
                                     元组和列表的操作几乎是一样的，除了不可变
                                            tuple([x for x in range(10)])
                                            list(zip(range(10), range(10)))
                                            {x:y for x, y in zip(range(10), range(10))}
                                            list(zip(range(5), range(10), range(20)))

                                    zip 函数用于合并多个可迭代对象，合并后的长度等于最短的可迭代对象的长度
                                            def r():
                                                for x in range(10):
                                                    pass

                                            from dis import dis
                                            dis(r)




            ###函数###
                    函数是Python里组织代码的最小单元
                    语句：可运行的一个代码单元
                    表达式：值，变量和操作符的组合
                    函数是组织好的，可重复使用的，用来实现单一或相关联功能的代码段
                    ###函数调用###
                            print("hello,word")
                            type('hello')
                            int(12.1)
                            abs(-1)
                        Python内建函数的调用。函数括号中的表达式被称之为函数的参数
                            abs()函数用于求数值的绝对值，只能接受一个参数，若参数类型不对，也会报TypeError
                            函数名是指向一个函数对象的引用，完全可以吧函数名赋值给另一个变量
                                    fun=abs
                                    fun(-1)
                    ###函数定义###
                            自定义函数实现某个功能
                            自定义函数规则：
                                    1：函数代码块以def关键字开头，后接函数标识符名称和圆括号"()"
                                    2：所有传入的参数和自变量都必须放入圆括号中，可以在圆括号中定义参数
                                    3：函数的第一行语句可以选择性使用文档字符串，用于存放函数说明
                                    4：函数内容以冒号开始，并且缩进
                                    5：return[表达式]结束函数，选择性返回一个值给调用方，不带表达式的return相当于返回None
                                            def 函数名(参数列表)：
                                                函数体
                                            def <name>(arg1,arg2...):
                                                <statements>
                                    函数的名字必须以字母开头，包括下划线"_",不能吧python关键字定义为函数名
                                            def hello():
                                                print("hello,word")
                                            hello()
                                            没有return语句，默认返回None

                                    def add(x, y):     # 函数定义 def 表示定义一个函数， 紧接着是函数名 函数名后面用
                                                        一对小括号列出参数列表，参数列表后面使用一个冒号开始函数体
                                            print(x + y)   # 函数体是正常的Python语句，可以包含任意结构
                                            return  x + y  # return 语句表示函数的返回值
                                    函数有输入(参数)和输出(返回值)的代码单元， 把输入转化为输出
                    ###函数的调用###
                            定义函数的时候,并不会执行函数体，　当调用函数的时候，才会执行其中的语句块
                                    add(3, 5)  # 函数使用函数名来调用， 函数名后紧跟一对小括号，小括号里传入函数定义时要求的参数
                                    add(3, 4, 5) # 传入参数必须和函数定义时的参数相匹配， 如果不匹配，会抛出TypeError


                    ###函数的参数###
                            带参数的函数
                            调用函数时可以使用以下参数类型：
                                    1：必须参数(位置参数)
                                    2：关键字参数
                                    3：默认参数
                                    4：可变参数
                                    5：组合参数
                            ###必须参数###
                                    必须参数以正确的顺序传入函数，调用时数量必须和声明时的一样
                                    def add(x, y):
                                        ret = x + y
                                        print('{} + {} = {}'.format(x, y, ret))
                                        return ret
                                        add(3, 5) # 参数按照定义的顺序传入  这样的传参方法叫做位置参数
                            ###关键字参数###
                                    关键字参数和函数调用关系紧密，函数调用使用关键字参数确定传入的参数值
                                    使用关键字参数允许调用函数时参数的顺序与声明不一致
                                        add(y=3, x=5) # 参数按照定义时的变量名传递， 这样的传参方法叫做关键字参数，关键字参数和顺序无关
                                        add(3, y=5) # 位置参数和关键字参数可以混合使用
                                        add(x=3, 5) # 当位置参数和关键字参数混合使用时， 位置参数必须在前面， 否则会抛出语法错误
                            ###默认参数###
                                    调用参数时，如果没有传递参数，则使用默认参数
                                    默认值
                                            def inc(base, x=1):
                                                return base + x
                                            inc(3)
                                            inc(3，2)
                                   参数可以有默认值，当一个参数有默认值时， 调用时如果不传递此参数，会使用默认值
                                            def add(x=0, y):  # 带默认值得参数必须在不带默认值的参数之后
                                                return x + y
                                            def connect(host='127.0.0.1', port=3306, user='root', password='', db='test'):
                                                pass
                                            connect('172.16.0.1', password='abcd')
                                    参数默认值和关键字参数一起使用，会让代码非常简洁
                            ###可变参数###
                                    函数需要处理更多的参数声明时
                                    def sum(*lst):  # 参数前加一个星号， 表示这个参数是可变的， 也就是可以接受任意多个参数,
                                                      这些参数将构成一个元组， 此时只能通过位置参数传参
                                        print(type(lst))
                                        ret = 0
                                        for x in lst:
                                            ret += x
                                        return ret
                                    sum(1, 2, 3)

                                    def connect(**kwargs): # 参数前加两个星号， 表示这个参数是可变的，可以接受任意多个参数，
                                                             这些参数构成一个字典，此时只能通过关键字参数传参
                                        print(type(kwargs))
                                        for k, v in kwargs.items():
                                            print('{} => {}'.format(k, v))
                                    connect(host='127.0.0.1', port=3306)

                                    可变参数两种形式：
                                    位置可变参数 ： 参数名前加一个星号， 构成元组， 传参只能以位置参数的形式
                                    关键字可变参数： 参数名前加两个信号， 构成字典， 传参只能以关键字参数的形式

                                            def fn(*args, **kwargs):
                                                print(args)
                                                print(kwargs)

                                            fn(2, 3, 5, a=4, b=5)
                            ###组合参数###
                                    位置参数，关键字参数，默认参数，可变位置参数，可变关键字参数
                                    位置可变参数和关键字参数可以一起使用
                                            def fn(**kwargs, *args): # 当位置可变参数和关键字可变参数一起使用时， 可变位置参数必须在前面
                                                pass

                                            def fn(x, y, *args, **kwargs):
                                                print(x)
                                                print(y)
                                                print(args)
                                                print(kwargs)

                                            fn(2, 3, 4, 5, 7, a=1, b=2)
                                            fn(2, 3)
                                            fn(2, 3, 4, 5, x=1)   ###报错
                                            fn(2, y=3)

                                     普通参数可以和可变参数一起使用，但是传参的时候必须匹配

                                            def fn(*args, x):
                                                print(args)
                                                print(x)

                                            fn(2, 3, 4)    ###报错
                                            fn(2, 3, x=4)
                                    位置可变参数可以在普通参数之前， 但是在位置可变参数之后的普通参数变成了keyword-only参数

                                            def fn(**kwargs, x):    #####报错
                                                print(kwargs)
                                                print(x)
                                    关键字可变参数不允许在普通参数之前

                                            def fn(x=5, *args):
                                                print(x)
                                                print(args)

                                            fn(1, 2, 3, 4)
                                            fn()

                                            def fn(*args, x=5):
                                                print(args)
                                                print(x)

                                            fn(1, 2, 3, 4)

                                            def fn(x=5, **kwargs):
                                                print(x)
                                                print(kwargs)

                                            fn(a=1, b=2)
                                            fn(3, a=1, b=2)


                                            def fn(**kwargs, x=5):   ####报错
                                                print(kwargs)
                                                print(x)
                                    当默认参数和可变参数一起出现的时候， 默认参数相当于普通参数
                                    通常来说：
                                            默认参数靠后
                                            可变参数靠后
                                            默认参数和可变参数不同时出现

                                            def connect(host='127.0.0.1', port=3306, user='root', password='', db='test', **kwargs):
                                                pass

                                            def connect(**kwargs):
                                                host = kwargs.pop('host', '127.0.0.1')

                            ###形参和实参###
                                    Python函数的两种类型参数：
                                            一种是函数定义里的形参，一种是调用函数时传入的实参
                                            函数名后的参数是形参，函数体中的参数是实参
                                            def names(name1,name2):
                                                print("The name1 is",name1)
                                                print("The name2 is",name2)

                            ###变量的作用域###
                                    python引用变量的顺序： 当前作用域局部变量->外层作用域变量->当前模块中的全局变量->python内置变量
                                    Python最基本的变量作用域：局部变量和全局变量
                                    ###局部变量###
                                            在函数内定义的变量名只能被函数内部引用，不能在函数外引用
                                                    def func1():
                                                        x=100
                                                        print(x)
                                                    prinx(x)
                                            在次函数中x是在函数体中定义的，不能在函数体外被访问
                                    ###全局变量###
                                            在函数外，一段代码最开始复制的变量可以被多个函数引用
                                                    x= 100          ###定义全局变量
                                                    def func():
                                                        x=20        ###定义局部变量
                                                        print(x)    ###打印结果是20
                                                    print(x)        ###打印结果是100
                                            在函数中使用某个变量时，如果变量名既有全局变量又有局部变量，
                                            则在函数体中，默认使用局部变量
                                            若将局部变量变为全局变量，则只需要使用global关键字即可
                                                    num=100
                                                    def fun():
                                                        global num
                                                        num=20
                                                        num+=20
                                                        print(num)
                                                    fun()
                                                    print(num)

                            ###有返回值和无返回值的函数###
                                    使用return和不使用return语句的函数的区别：
                                            函数定义时没有return语句，则默认返回None
                                            def aa(a,b):
                                                print(a+b)
                                            def aaa(a,b):
                                                return a+b
                                            fb=aa(9,8)
                                            fc=aaa(8,9)
                                            print(fc)
                                            print(fb)

                            ###高阶函数###
                                    一个函数就可以接收另一个函数作为参数，这种函数就称之为高阶函数。
                                            def fun1(*args):
                                                def fun2():
                                                    ax=0
                                                    for n in args:
                                                        ax+=n
                                                    return ax
                                                return fun2
                                            此时该函数返回一直计算值，若不想直接返回值，而是返回一个函数
                                                后面需要的时候在调用函数来计算值
                                            在此例中，fun1函数中又定义了fun2函数，并且内部函数fun2可以引用
                                                外部函数fun1的参数和局部变量，当fun1返回fun2时，相关参数
                                                和变量都保存在返回的函数中，称为闭包。fun1每次调用都会返回
                                                一个新的函数，即使传入相同的参数
                                    ###闭包###
                                            如果在一个内部函数里对外部函数(不是在全局作用域)的变量进行引用，
                                            内部函数就称为闭包
                                                def count():
                                                    def f(j):
                                                        def g():
                                                            return j*j
                                                        return g
                                                    fs=[]
                                                    for i in range(1,4):
                                                        fs.append(f(i))
                                                        return fs

                                    def counter(i):
                                                base = i
                                                def inc(x=1):
                                                    nonlocal base
                                                    base += x
                                                    return base
                                                return inc

                                    返回函数或者参数是函数的函数 -- 高阶函数
                                    因为Python中函数是一等对象(first class)
                                    函数也是对象，并且它可以像普通对象一样赋值，作为参数，作为返回值
                                    函数作为返回值： 通常是用于闭包的场景， 需要封装一些变量
                                    函数作为参数：通常用于大多数逻辑固定，少部分逻辑不固定的场景

                                            import datetime
                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                return wrap

                                            def add(x, y):
                                                return x + y

                                            loged_add = logger(add)

                                            loged_add(3, y=5)
                                    函数作为参数，返回值也是函数： 通常用于作为参数函数执行前后需要一些额外操作

                                    装饰器例子：实现函数执行时间展示
                                                语法糖：指计算机语言中添加的某种语法，这种语法对语言的功能并没有影响，但是更方便程序员使用
                                    例子1：直接吧代码写在时间函数里面执行
                                            import time
                                            def foo():
                                                start = time.clock()
                                                [(x,y) for x in range(3000) for y in range(6000,9000)]
                                                end = time.clock()
                                                print('used',end - start)
                                            foo()



                                    例子2：在时间函数里面调用需要执行的函数
                                            import time
                                            def foo():
                                                [(x,y) for x in range(3000) for y in range(6000,9000)]
                                            def timeit(func):
                                                start = time.clock()
                                                func()
                                                end = time.clock()
                                                print('used',end - start)
                                            timeit(foo)         ###返回的是一个值
                                            这样的话，如果foo在N处都被调用了，你就不得不去修改这N处的代码。或者更极端的，
                                            考虑其中某处调用的代码无法修改这个情况，比如：这个函数是你交给别人使用的。

                                    例子3：赋予新函数的名字
                                            import time
                                            def timeit(func):
                                                def warpper():
                                                    start = time.clock()
                                                    func()
                                                    end = time.clock()
                                                    print('used',end - start)
                                                return warpper
                                            def foo():
                                                [(x,y) for x in range(3000) for y in range(6000,9000)]
                                            foo = timeit(foo)       ###返回的是一个函数
                                            foo()

                                    例子4：
                                            import time
                                            def timeit(func):   ###要传入的函数
                                                def warpper():  ###要传入的函数的参数
                                                    start = time.clock()
                                                    func()
                                                    end = time.clock()
                                                    print('used',end - start)
                                                return warpper
                                            @timeit     ##这样写，就不用在多个需要执行函数判断其执行时间的前面加上那么一段代码了
                                            def foo():
                                                [(x,y) for x in range(3000) for y in range(6000,9000)]
                                            foo()
                                            生成器下面所定义的函数是需要将其传入到生成器函数里面执行的
                                            因为foo函数没有参数，所以只需要在timeit函数里面定义参数接受foo这个函数即可，
                                            若需要给foo函数添加参数，则需要在warpper里面也定义参数来接受foo的参数
                                    例子5：

                                            import datetime

                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                return wrap
                                            def add(x, y):
                                                return x + y
                                            loged_add = logger(add)
                                            loged_add(3, y=5)
                                            函数作为参数，返回值也是函数： 通常用于作为参数函数执行前后需要一些额外操作

                                    例子6：
                                            import time
                                            def sleep(x):
                                                time.sleep(x)
                                            logged_sleep = logger(sleep)
                                            logged_sleep(3)
                                            sleep = logger(sleep)
                                            sleep(3)
                                            @logger
                                            def sleep(x):
                                                time.sleep(x)
                                            sleep(3)
                            ###装饰器###
                                    参数是一个函数， 返回值是一个函数的函数，就可以作为装饰器
                                            import datetime
                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                wrap.__name__ = fn.__name__
                                                wrap.__doc__ = fn.__doc__
                                                return wrap

                                            @logger
                                            def sleep(x):
                                                time.sleep(x)

                                            def copy_proprities(src, dst):
                                                dst.__name__ =  src.__name__
                                                dst.__doc__ = src.__doc__

                                            import datetime

                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                copy_proprities(fn, wrap)
                                                return wrap

                                            def copy_proprities(src):
                                                def _copy(dst):
                                                    dst.__name__ =  src.__name__
                                                    dst.__doc__ = src.__doc__
                                                    return dst
                                                return _copy

                                            import datetime

                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                @copy_proprities(fn)
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                return wrap

                                            @logger
                                            def sleep(x):
                                                time.sleep(x)

                            ###柯里化###
                                            import functools
                                            import datetime
                                            def logger(fn): # 函数作为返回值： 封装了fn
                                                @functools.wraps(fn)
                                                def wrap(*args, **kwargs):
                                                    start = datetime.datetime.now()
                                                    ret = fn(*args, **kwargs)
                                                    end = datetime.datetime.now()
                                                    print('call {} took {}'.format(fn.__name__, end-start))
                                                    return ret
                                                return wrap

                                            @logger
                                            def sleep(x):
                                                time.sleep(x)

                                            def logger(s):
                                                def _logger(fn):
                                                    @functools.wraps(fn)
                                                    def wrap(*args, **kwargs):
                                                        start = datetime.datetime.now()
                                                        ret = fn(*args, **kwargs)
                                                        end = datetime.datetime.now(ii)
                                                        if (end-start).total_seconds() > s:
                                                            print('call {} took {}'.format(fn.__name__, end-start))
                                                        return ret
                                                    return wrap
                                                return _logger
                                            @logger(2)
                                            def sleep(x):
                                                time.sleep(x)
                                            sleep(3)
                                    带参数的装饰器： 一个函数， 返回一个不带参数的装饰器

                                            def logger(s, p=lambda name, t: print('call {} took {}'.format(name, t))):

                                                def _logger(fn):

                                                    @functools.wraps(fn)
                                                    def wrap(*args, **kwargs):

                                                        start = datetime.datetime.now()
                                                        ret = fn(*args, **kwargs)
                                                        end = datetime.datetime.now()
                                                        if (end-start).total_seconds() > s:
                                                            p(fn.__name__, end-start)
                                                        return ret
                                                    return wrap
                                                return _logger


                                            @logger(2, p=lambda name, t: None)
                                            def sleep(x):
                                                time.sleep(x)

                                            def logger(s):
                                                def _logger(p=lambda name, t: print('call {} took {}'.format(name, t))):
                                                    def __logger(fn):
                                                        @functools.wraps(fn)
                                                        def wrap(*args, **kwargs):
                                                            start = datetime.datetime.now()
                                                            ret = fn(*args, **kwargs)
                                                            end = datetime.datetime.now()
                                                            if (end-start).total_seconds() > s:
                                                                p(fn.__name__, end-start)
                                                            return ret
                                                        return wrap
                                                    return __logger
                                                return _logger
                                            logger2s = logger(2)
                                            @logger2s()
                                            def sleep(x):
                                                time.sleep(x)
                                            sleep(3)
                                            sleep(1)
                                            sleep = logger2s()(sleep)



                                    装饰器个人经典例子：
                                    例子1：
                                            实现在打印11前还要打印ee
                                            def aa():
                                                print(11)
                                            def aa():
                                                print("ee")
                                                print(11)
                                            aa()

                                            修改了原函数

                                    例子2：
                                            def aa():
                                                print(11)

                                            def cc(args):
                                                def bb():
                                                    print("ee")
                                                    args()
                                                return bb

                                            @cc
                                            def aa():
                                                print(11)
                                            aa()

                                    例子3：
                                            参数：
                                            def auth_arg(func):
                                                def inner(arg):
                                                    print('ok')
                                                    func(arg)
                                                return inner

                                            @auth_arg
                                            def aa(pp):
                                                print(pp)

                                            aa("dd")

                                    例子4：
                                            可变参数：
                                            def auth_arg(func):
                                                def inner(*arg,**args):
                                                    print('ok')
                                                    func(*arg,**args)
                                                return inner

                                            @auth_arg
                                            def aa(*pp,**ppp):
                                                print(pp,ppp)

                                            aa(8,99999,i=99)
                                    例子5：
                                            def user2(us2):
                                                def user3(us3):
                                                    if us2(us3) == 1:
                                                        print("Loging ok")
                                                    else:
                                                        print("Loging error")
                                                return user3
                                            @user2
                                            def user1(us1):
                                                if us1 == "joey":
                                                    return 1
                                                else:
                                                    return 0
                                    
                                    ###递归函数###
                                            如果一个函数在内部调用了自己，则函数就叫递归函数
                                            def g(n):
                                                if n == 0:
                                                    return 1
                                                if n == 1:
                                                    return 1
                                                return n * g(n-1)

                                            递归函数总是涉及到压栈和出栈的过程
                                            递归函数总是压栈，知道遇到退出条件，然后出栈

                                                Python中递归函数有深度限制，可以通过
                                                sys.getrecursionlimit()
                                            得到深度限制，可以通过sys.setrecursionlimit调整递归深度限制
                                            递归函数在Python非常慢，并且有深度限制，所以 因尽量避免使用递归
                                            循环都可以转化为递归，但不是所有递归都可以转化为循环

                                                def g(n):
                                                    ret = 1
                                                    for x in range(1, n + 1):
                                                        ret *= x
                                                    return ret
                                                Python可以完全不使用递归
                                                    mport functools
                                                    functools.wraps
                                                    functools.partial
                                                    def add(x, y):
                                                        return x + y
                                                    add(3, 5)
                                                    new_add = functools.partial(add, y=3)
                                                    new_add(5, y=5)
                                                    partial 函数用于固定函数中一个或者若干个参数
                                                    函数作为参数， 对这个作为参数的函数的参数列表是有限制的
                                                    def cmp(a, b, r):
                                                        if r:
                                                            return a < b
                                                        return a > b
                                                    sort(range(4), functools.partial(cmp, r=True))
                                                    functools.partial(add, x=5)(y=4)

                                                    functools.lru_cache
                                                    import datetime

                                                    def logger(fn): # 函数作为返回值： 封装了fn
                                                        @functools.wraps(fn)
                                                        def wrap(*args, **kwargs):
                                                            start = datetime.datetime.now()
                                                            ret = fn(*args, **kwargs)
                                                            end = datetime.datetime.now()
                                                            print('call {} took {}'.format(fn.__name__, end-start))
                                                            return ret
                                                        return wrap
                                                    import time
                                                    @logger
                                                    @functools.lru_cache(3)
                                                    def sleep(x):
                                                        time.sleep(x)
                                                        return x
                                                    sleep(3)
                            ###匿名函数###
                                            lambda params : expr
                                    只能写在一行上
                                    表达式的结构就是返回值
                                    python 使用 lambda 来创建匿名函数
                                    lambda的主体是一个表达式，而不是一个代码块。仅仅能在lambda表达式中封装有限的逻辑进去
                                    lambda函数拥有自己的命名空间，且不能访问自有参数列表之外或全局命名空间里的参数
                                            lambda [arg1 [,arg2,.....argn]]:expression
                                    # 可写函数说明
                                            sum = lambda arg1, arg2: arg1 + arg2;
                                            sum( 10, 20 )

                                    默认参数：
                                            add = lambda x, y=1: x+ y
                                    可变参数：
                                            f = lambda *x: x
                                    可变关键字参数：
                                            f = lambda **kw: kw
                                    参数槽：
                                            f = lambda x, *, y: x+ y

                                    匿名函数通常和高阶函数配合使用，作为参数传入、或者作为返回值返匿名函数最好不要定义成递归函数
                            ###参数槽###
                                    参数槽
                                    def fn(a, b, c):
                                        print(a, b, c)
                                    fn(1, 2, 3)
                                    fn(a=1, b=2, c=3)

                                    def fn(*, a, b, c):
                                        print(a, b, c)
                                    fn(1, 2, 3)
                                    以上传参会报错
                                    fn(a=1, b=2, c=3)
                                    *之后的参数，必须以关键字参数的形式传递，称之为参数槽

                                    def fn(a, b, *, c):    //整个函数称之为参数槽，*号后面的称之为命名参数，前面的称之为关键字参数
                                        print(a, b, c)
                                    fn(1, 2, c=3)
                                    fn(a=1, b=2, c=3)

                                    参数槽通常和默认参数搭配使用

                                    ef fn(a, b, *):
                                        print(a, b)
                                    以上会报错
                                    *之后必须有参数

                                    def fn(a, b, *, c=1):
                                        print(a, b, c)
                                    fn(1, 2)
                                    fn(1, 2, c=3)
                                    命名参数可以有默认值
                                    def fn(a, b=1, *, c=2):
                                        print(a, b, c)
                                    fn(0)
                                    fn(0, c=3)
                                    非命名参数有默认值时，命名参数可以没有默认值
                                    默认参数应该在每段参数的最后

                                    def fn(a, *args, *, c):
                                        print(a)
                                        print(args)
                                        print(c)
                                    报错
                                    def fn(a, *, **kwargs):
                                        print(a)
                                        print(kwargs)
                                    报错
                                    def fn(a, **kwargs, *, c):
                                        print(a)
                                        print(kwargs)
                                        print(c)
                                    报错
                                    使用参数槽时， 不能使用可变位置参数，可变关键字参数，必须放在命名参数之后
                                    def fn(a, *, c, **kwargs):
                                        print(a, c)
                                        print(kwargs)
                                    fn(1, c=2, b=3, d=4)

                                    def fn(a, *, c, *args, **kwargs):
                                        print(a)
                                        print(c)
                                        print(args)
                                        print(kwargs)
                                    报错
                                    def fn(a, *args, c, **kwargs):
                                        print(a)
                                        print(args)
                                        print(c)
                                        print(kwargs)
                                    fn(0, 1, 2, 3, c=4, d=5)
                                    类型示意 Python 3.5才有
                                    def add(x:int, y:int) -> int:
                                        return x+y
                                    add(1, 2)
                                    类型示意没有任何类型检查，仅仅只是一个示意而已
                                    Python是一种自文档的语言
                                    def add(x, y):
                                        '''
                                        @param x int
                                        @param y int
                                        @return int
                                        '''
                                        return x+y
                                        更清晰的自文档
                                        帮助IDE做检查
                                        可以通过这种机制，做类型检查

                            ###偏函数###
                                    Python的functools模块提供了很多有用的功能，其中一个就是偏函数（Partial function）
                                    通过设定参数的默认值，可以降低函数调用的难度。而偏函数也可以做到这一点。举例如下：
                                    int()函数可以把字符串转换为整数，当仅传入字符串时，int()函数默认按十进制转换：

                                    int('12345')
                                    12345
                                    但int()函数还提供额外的base参数，默认值为10。如果传入base参数，就可以做N进制的转换：

                                    >>> int('12345', base=8)
                                    5349
                                    >>> int('12345', 16)
                                    74565

                                    functools.partial就是帮助我们创建一个偏函数的，不需要我们自己定义int2()，
                                            可以直接使用下面的代码创建一个新的函数int2：

                                    >>> import functools
                                    >>> int2 = functools.partial(int, base=2)
                                    >>> int2('1000000')
                                    64
                                    >>> int2('1010101')
                                    85
                                    简单总结functools.partial的作用就是，把一个函数的某些参数给固定住（也就是设置默认值），
                                        返回一个新的函数，调用这个新函数会更简单。

                                    当函数的参数个数太多，需要简化时，使用functools.partial可以创建一个新的函数，
                                        这个新函数可以固定住原函数的部分参数，从而在调用时更简单。
                                    个人经典例子：
                                        1：
                                            def aa(a,b):
                                                return a+b
                                            aa(2,3)
                                        2：
                                            from functools import partial
                                            def cc(d,e):
                                                return d+e
                                            dd=partial(cc,4)
                                           dd(8)

                    ###面向对象###
                                    面向对象(OOP)是一种程序设计思想，OOP把对象作为程序的基本语言
                                            一个对象包含数据和操作数据的函数
                                    面向对象程序设计吧计算机程序视为一组对象的集合，每个对象都可以接受其他对象发来的消息
                                    并处理这些消息。在Python中，所有数据类型都被视为对象，也可以自定义对象。
                                    自定义对象数据类型就是面向对象中类的概念
                            ###面向对象术语简介：
                                    类： 用来描述具有相同属性和方法的对象的集合。类定义了集合中每个对象共有的属性
                                        和方法。对象是类的实例
                                    类变量(属性)：类变量在整个实例化的对象中是公用的。类变量定义在类中
                                                且在方法之外。类变量通常不作为实例变量的使用。类变量也称作属性
                                    数据成员：类变量或实例变量用于处理类及其实例对象的相关数据
                                    方法重写：如果从父类继承的方法不能满足子类的需求，就可以对其改写，这个过程
                                             称为方法覆盖，也成为方法重写
                                    实例变量：定义在方法中的变量只作用于当前实例的类
                                    多态：对不用类的对象使用同样的操作
                                    封装：对外部世界隐藏对象的工作细节
                                    继承：即一个派生类继承基类的字段和方法。继承允许吧一个派生类的对象作为
                                         一个基类对象对待，以普通类为基础建立专门的类对象
                                    实例化：创建一个类的实例，累的具体对象
                                    方法：类中定义的函数
                                    对象：通过类定义的数据解构实例。对象包括两个数据成员(类变量和实例变量)和方法
                            Python中的类提供了面向对象编程的所有基本方法：
                                    类的继承机制允许多个基类，派生类可以覆盖基类中的任何方法，方法中可以调用基类中的同名方法
                                    对象可以包含任意数量和类型的数据
                            ###类的定义与使用##
                                    实例代码：
                                            class Myclass(object):
                                                i=123
                                                def f(self):
                                                    return 'hello,word'
                                    格式：
                                            class ClassName(object):
                                                <statement-1>
                                                .
                                                .
                                                <statement-N>

                                            Python使用class关键字，class后面紧接着类名，类名通常首字母大写
                                                    紧接着是(boject)，表示该类是从哪个类继承下来的。
                                                    通常，如果没有合适的继承类，就是用object类，这是所有类
                                                    都会继承的类。类包含属性（相当于函数中的语句）和方法（类中
                                                    的方法大体可以理解成函数）
                                            在类中定义方法的形式和函数差不多，但不称为函数，而称为方法
                                                    方法的调用要绑定到特定对象上，而函数不需要
                                    ###类的使用###
                                                    class Myclass(object):
                                                        i=123
                                                        def f(self):
                                                            return 'hello,word'
                                                    use_class = Myclass()
                                                    print('调用类的属性:',use_class.i)
                                                    print('调用类的方法:',use_class.f())

                                                    调用类的属性: 123
                                                    调用类的方法: hello,word
                                            调用类时需要执行以下操作：
                                                        use_class=Myclass()
                                                    这一步叫类的实例化，即创建一个类的实例，此处
                                                        得到的use_class变量称为类的具体对象
                                                    第一行后的use_class.i用于调用类的属性，也叫类变量
                                                    第二行的use_class.f()用于调用类的方法
                                                    在类中定义f()方法时带了一个self参数
                                                    在类中定义方法的要求：
                                                            1：在类中定义方法时，第一个参数必须是self。
                                                                除第一个参数外，类的方法和普通函数没有什么区别，
                                                                可以使用默认参数，可变参数，关键字参数等
                                                    在类中调用方法要求：
                                                            在类中定义方法时，在实例变量上直接调用即可，
                                                                除了self不用传递，其他参数正常传入
                                                    类对象支持两种操作：
                                                            属性引用和实例化。属性引用的标准语法如下：
                                                                obj.name
                                                            语法中obj代表类对象，name代表属性
                                                    个人例子：
                                                            class MyClass(object):
                                                                i="base"
                                                                def f(self):
                                                                    def f1(arge1):
                                                                        if self(arge1) == 1:
                                                                            print("Login Ok")
                                                                        else:
                                                                            print("Login Error")
                                                                    return f1
                                                            use_class1 = MyClass
                                                            @use_class1.f
                                                            def f2(arg2):
                                                                if arg2 == "joey":
                                                                    return 1
                                                                else:
                                                                    return 0
                                                            def f3(f311,f322):
                                                                f333=input("Please Input Your Account:   ")
                                                                if f311 == 'base':
                                                                    f322(f333)
                                                                else:
                                                                    print("Not Base User")
                                                            f3(use_class1.i,f2)
                                    ###深入类###
                                            ###类的构造方法###
                                                    class Myclass(object):
                                                        i=123
                                                        def __init__(self,name):
                                                            self.name=name
                                                        def f(self):
                                                            return 'hello,'self.name
                                                    use_class = Myclass()
                                                    print('调用类的属性:',use_class.i)
                                                    print('调用类的方法:',use_class.f())
                                            从上可以看出，实例化MyClass类时调用了__init_()方法。
                                            在Python中，__init__()方法是一个特殊的方法，在对象实例化的时候会被调用
                                                __init__()的意思是初始化，是initialization的简写。
                                                这个方法的书写方式是：先输入两个下划线，后面紧接着init，再接着两个下划线，
                                                这个方法也叫构造方法。在定义类时，若不显示的定义一个__init__()方法，
                                                则程序默认调用一个无参的__init__方法。如以下代码效果一样
                                                例子1：
                                                    class DefaultInit(object):
                                                        def __init__(self):
                                                            print('类的实例化时执行我，我是__init__方法')
                                                        def show(self):
                                                            print('我是类中定义的方法，需要通过实例化对象调用')
                                                    test=DefaultInit()
                                                    print('类实例化结束')
                                                    test.show

                                                例子2：
                                                    class DefaultInit(object):
                                                        def show(self):
                                                            print('我是类中定义的方法，需要通过实例化对象调用')
                                                    test=DefaultInit()
                                                    print('类实例化结束')
                                                    test.show

                                            在一个类中定义多个构造方法：
                                                例子3：
                                                    class DefaultInit(object):
                                                        def __init__(self):
                                                            print('我是不带参数的init方法')
                                                    DefaultInit()
                                                    print('类实例化结束')
                                                在只有一个__init__方法时，实例化类没有什么顾虑

                                                例子4：
                                                    class DefaultInit(object):
                                                        def __init__(self):
                                                            print('我是不带参数的init方法')
                                                        def __init__(self,param):
                                                            print('我是带一个参数的init方法，参数值为：',param)
                                                    DefaultInit('hello')
                                                    print('类实例化结束')
                                                由执行结果看到，调用的是带一个param参数的构造方法，若把类的实例化语句更改为
                                                        DefaultInit()
                                                    或更改为
                                                        DefaultInit('hello','word')
                                                由执行结果可以看到，实例化类时只能调用带两个占位参数的构造方法，调用其他构造方法会报错

                                                例子5：
                                                        class DefaultInit(object):
                                                            def __init__(self,param):
                                                                print('我是一个带参数的__init__方法，参数值为：',param)
                                                            def __init__(self):
                                                                print('我是不带参数的__init__方法')
                                                        DefaultInit()
                                                        print('类实例化结束')
                                                    由执行结果看到，调用构造方法除了self外，没有其他参数，若把实例化语句更改为
                                                        DefaultInit('hello')
                                                    则会报错，因为在此处实例化类时只能调用带一个占位参数的构造方法，调用其他构造方法会报错

                                                从以上五个例子得知：
                                                        一个类中可以定义多个构造方法，但实例化类时只实例化最后的构造方法，即
                                                            后面的构造方法会覆盖前面的构造方法，并且需要根据最后一个构造方法
                                                            的形式进行实例化，建议一个类中只定义一个构造函数

                                    ###类的访问权限###
                                            在类内部有属性和方法，外部代码可以通过直接调用实例变量的方法操作数据，这样就隐藏了内部的复杂逻辑
                                                例子1：
                                                        class Student(object):
                                                            def __init__(self,name,score):
                                                                self.name=name
                                                                self.score=score
                                                            def info(self):
                                                                print('学生：%s;分数：%s'%(self.name,self.score))
                                                        stu=Student('xiaomeng',95)
                                                        print('修改前分数：',stu.score)
                                                        stu.info()
                                                        stu.score=0
                                                        print('修改后分数：',stu.score)
                                                        stu.info()
                                                在类中定义的非构造方法可以调用类中构造方法实例变量的属性，调用方式
                                                        为self.实例变量属性名，如代码中的self.name和self.score
                                                        可以在类的外部修改内的属性，如果让内部属性不被外部访问，
                                                        可以在属性名称前加两个下划线__.
                                                在Python中，实例的变量名如果以__开头，就会变成私有变量，只有内部可以访问
                                                例子2：
                                                        class Student(object):
                                                            def __init__(self,name,score):
                                                                self.__name=name
                                                                self.__score=score
                                                            def info(self):
                                                                print('学生：%s;分数：%s'%(self.__name,self.__score))
                                                        stu=Student('xiaomeng',95)
                                                        print('修改前分数：',stu._score)
                                                        stu.info()
                                                        stu.score=0
                                                        print('修改后分数：',stu._score)
                                                        stu.info()
                                                此时，会报错，无法从外部访问实例变量的属性__score了，这样的作用：
                                                        确保外部代码不能随意修改对象内部的状态，通过访问限制的保护，代码更安全
                                                        如果外部代码要获取类中的name和score咋办：？
                                                            在Python中，可以为类增加get_attrs方法，获取类中的私有变量
                                                            例如在上面的示例中添加get_score(name的使用方式类同)方法，代码如下：
                                                        lass Student(object):
                                                            def __init__(self,name,score):
                                                                self.__name=name
                                                                self.__score=score
                                                            def info(self):
                                                                print('学生：%s;分数：%s'%(self.__name,self.__score))
                                                            def get_score(self):
                                                                return self._score
                                                        stu=Student('xiaomeng',95)
                                                        print('修改前分数：',stu._score)
                                                        stu.info()
                                                例子3：person的基础属性(init)和附加属性(paoniu)
                                                        class Person(object):
                                                        # 这里就是初始化你将要创建的实例的属性
                                                            def __init__(self,hight,weight,age):
                                                                self.hight = hight
                                                                self.weight = weight
                                                                self.age = age

                                                        # 定义你将要创建的实例所有用的技能
                                                            def paoniu(self):
                                                                print('你拥有泡妞的技能')
                                                例子4：
                                                        class Student(object):
                                                            def __init__(self, name, score):
                                                                self.name = name
                                                                self.score = score

                                                            def get_grade(self):
                                                                if self.score >= 90:
                                                                    return 'A'
                                                                elif self.score >= 60:
                                                                    return 'B'
                                                                else:
                                                                    return 'C'

                                                例子5：
                                                        class Student(object):
                                                            def __init__(self, name, score):
                                                                self.__name = name
                                                                self.__score = score
                                                            def print_score(self):
                                                                print('%s: %s' % (self.__name, self.__score))
                                                        bart = Student('Bart Simpson', 59)
                                                        bart.__name   ###报错
                                                但是如果外部代码要获取name和score可以给Student类增加get_name和get_score这样的方法：
                                                        class Student(object):
                                                            def __init__(self, name, score):
                                                                self.__name = name
                                                                self.__score = score
                                                            def get_name(self):
                                                                return self.__name
                                                            def get_score(self):
                                                                return self.__score

                                                如果又要允许外部代码修改score怎么办？可以再给Student类增加set_score方法：
                                                        class Student(object):
                                                        ...
                                                        def set_score(self, score):
                                                            self.__score = score
                                                使用这种方法原因：因为在方法中，可以对参数做检查，避免传入无效的参数：
                                                        class Student(object):
                                                            ...
                                                            def set_score(self, score):
                                                                if 0 <= score <= 100:
                                                                    self.__score = score
                                                                else:
                                                                    raise ValueError('bad score')

                                                最后注意下面的这种错误写法：
                                                        >>> bart = Student('Bart Simpson', 59)
                                                        >>> bart.get_name()
                                                        'Bart Simpson'
                                                        >>> bart.__name = 'New Name' # 设置__name变量！
                                                        >>> bart.__name
                                                        'New Name'
                                                        表面上看，外部代码“成功”地设置了__name变量，但实际上这个__name
                                                        变量和class内部的__name变量不是一个变量！内部的__name变量已经
                                                        被Python解释器自动改成了_Student__name，而外部代码给bart新增
                                                        了一个__name变量。不信试试：
                                                        >>> bart.get_name() # get_name()内部返回self.__name
                                                        'Bart Simpson'
                                                ###例子6###
                                                            class Myclass(object):
                                                                def __init__(self,name,age):
                                                                    self.__name=name
                                                                    self.__age=age
                                                                def get__age(self):
                                                                    return self.__age
                                                                def info(self):
                                                                    print("my age is",self.__age)
                                                                def set__age(self,age):
                                                                    self.__age=age
                                                            use_class=Myclass('joey',20)
                                                            use_class.info()
                                                            use_class.get__age()
                                                            use_class.set__age(18)
                                                            use_class.get__age()
                                                            use_class.info()
                                    ###继承###
                                            

































