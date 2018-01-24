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
                                                



























