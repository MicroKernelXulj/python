# python：

常量/变量
        常量： 一旦赋值，就不可再改变换句话说，就是不能对它重新赋值。Python不存在常量
        字面常量：一个单独出现的量，未赋值给任何变量或常量
        变量： 是一个名字，在赋值符号的左边，这个名字可以指代赋值符号右边的内容
i=3

类型系统
        Python是强类型语言
        Python是动态类型语言
        强类型： 指不同类型之间不能相互计算： 运算的时候会做类型检查
        **动态类型**： 变量可以重新赋值为其他类型

运算符
        算术运算符
        算术运算符只能对int和float运算

比较运算符
        比较运算的返回值都是bool类型

逻辑运算符
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

赋值运算符
        顺序结构
                从上到下 一行一行执行
                        i = 3
                        print(i)
                        i += 5
                        print(i)


        分支结构
                单分支
                        开始
                        if 条件:
                            操作
                        结束
                                a = 5
                                if a < 10:
                                    print('a less than 10')
                                print(a)

                双分支
                        开始
                        if 条件:
                            操作1
                        else:
                           操作2
                        结束

                                 a = 5
                                 if a < 10:
                                     print('a less than 10')
                                 else:
                                     print('a not less than 10')
                                 print(a)

                通过结构嵌套可以实现多分支
                         a = 50
                         if a < 10:
                             print('a < 10')
                         elif a < 20:
                             print('10 <= a < 20')
                         else:
                             print('a >= 20')

                    多分支
                            分支结构永远只有一个或者0个分支会被执行
                            条件只能是bool类型或者可以隐式转化为bool类型


循环结构
        while 循环
                    开始
                    while 条件:
                        操作
                    结束
                                i = 0
                                while i < 10:
                                    print(i)
                                    i += 1
                    一定要有某种机制修改调制使其退出循环，通常是在循环体里修改条件
        for in
                    开始
                    for 元素 in 可迭代对象:
                        操作
                    结束
                                for i in range(0, 10):
                                    print(i)
                    for in 循环里永远不要修改可迭代对象
        提前终止
                    for i in range(0, 10):
                        print(i)
                        if i % 2 != 0:
                            print('find it')
                            break
        跳过
                    for i in range(0, 10):
                        print(i)
                        if i % 2 != 0:
                            continue
                        print('i is {}, i+1 is {}'.format(i, i + 1))

        continue 用于跳过循环体剩下的部分
                    for i in range(0, 5):
                        for j in range(0, 10):
                            if j > 5:
                                break
                            print('i is {}, j is {}'.format(i, j))

                    for i in range(0, 5):
                        for j in range(0, 10):
                            if j != 5:
                                continue
                            print('i is {}, j is {}'.format(i, j))
         break 和 continue只针对最近的一层
         break和continue只能用在循环里

        else 子句
                for x in range(0, 10):
                    pass
                else:
                    print('ok')

                for x in range(0, 10):
                    break
                else:
                    print('ok')

                 for x in range(0, 10):
                     continue
                 else:
                     print('ok')
        当循环没有提前退出时，会执行else子句


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

count 方法返回值在列表里出现的次数
        def count(lst, value):
            c = 0
            for x in lst:
                if x == value:
                    c += 1
            return c
        通过索引访问元素
        index方法根据值返回第一个索引
        count方法返回元素在列表里的个数
        index和count的时间复杂度是O(n) 线性复杂度 效率与数据规模线性相关

#### 修改 ####
        lst[2] = 5  # 修改列表的元素直接使用下标操作取出元素并对其赋值
        修改元素有且只有这一种方法
        对超出范围的索引修改元素，会抛出IndexError

### 增加 ###
        显然无法使用索引操作
            lst.append(9) # append 原地修改list， 返回结果是None
            lst.insert(1, 11) # insert 原地修改list， 返回None
        insert 当索引超出范围时
                索引是负数 会在第0个元素前插入
                索引是正数 会在最后一个元素后插入
                append的时间复杂度是O(1) 常数时间 效率和数据的规模无关
                insert的时间复杂度是0(n) 线性时间 效率和数据规模线性相关

    lst.extend([1, 2, 3]) # 原地修改 返回None
            append操作单个元素
            extend操作可迭代对象
    lst + ['a', 'b', 'c']  # 不修改list本身， 返回一个新的list  list 的连接操作

### 删除 ###
            lst = [1, 2, 3, 2, 4, 3, 5, 3, 4]
            lst.remove(1) # 原地修改 返回None  根据值删除元素
            lst.remove(2) # 从左到右，删除第一个
            lst.remove(10) # 当值不存在时， 抛出ValueError
            lst.pop() # 返回并删除最后一个元素
            lst.pop(1) # 返回并删除索引所在位置的元素
            lst.pop(100) # 当索引不存在时， 抛出IndexError

            pop不传递index参数 时间复杂度是 O(1)
            pop传递index参数 时间复杂度是 O(n)
            pop 根据索引删除元素 并且会返回删除的元素
            remove 根据值删除元素， 返回None

            lst.clear() # 删除所有元素

### 其他操作 ###
        求list长度
                len(lst)
                lst = list(range(4))
                len(lst)

        反转
                lst.reverse() # 原地修改，返回None 翻转列表

        排序    L.sort(key=None, reverse=False)
                lst.sort() # 原地修改， 返回None
                lst.sort(reverse=True)

### 复制 ###
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
                t.index(2)
                index方法和list表现一致
                t.count(10)
                count 方法和list表现一致

            命名元组
                t = ('comyn', 18)
            from collections import namedtuple
            User = namedtuple('_User', ['name', 'age'])
            me = User('comyn', 18)
            me.name


##### 字符串 #####
                字符串是集合类型

                        s = 'hello python'
                        s = "hello python"
                        s = '''hello python'''
                        s = """hello python"""
                前两种完全一样 后两种完全一样
                        s = '''hello python
                        i like python'''
                三引号可以定义多行字符串
                单/双引号只能定义单行字符串

        转义
                s = 'i like \npython'
                s = 'i\'m comyn'
                path = 'C:\\windows\\nt\\system32'
                path = r'C:\windows\nt\system32' # 加r前缀代表此字符串是自然字符串， 不会转义

### 下标操作 ###
                        s = "hello python"
                        s[3]
                        type(s[4])
                        s[4] = 'C' # 字符串是不可变的

                字符串是可迭代对象
                        s = "hello python"
                        for c in s:
                            print(c)
                        list(s)

###字符串的操作###
       join
                lst = ['i',  'am', 'comyn']
                ' '.join(lst) # join是字符串的方法，参数是内容为字符串的可迭代对象， 接收者是分隔符
                ','.join(lst)
        分割
                            split   rsplit   splitlines  partition   rpartition
            split()
                        s = 'i love python'
                        s.split() # split 默认使用空格分割
                        'i          love python'.split() # 多个空格当成一个空格处理
                        'i     love python'.split(' ') # 当指定了以空格为分隔符时， 每个空格都处理
                        s.split(maxsplit=1)
                        'i i i i i i i i'.split(maxsplit=2) # split 从左往右分割字符串， maxsplit参数表示分割多少次， 默认值为-1， 表示分割所有分割符
                        s.split('o')
                        s.split('lo') # 分割符可以是任意字符串
            rsplit()
                        rsplit 是split从右往左的版本
                        'i i i i i i'.rsplit(maxsplit=1)
                        'i i i i i i'.rsplit()
            当不是用maxsplit参数时， split和rsplit表现形式一样， 但是split效率高于rsplit
            splitlines()
                        s = '''i am comyn
                        i love python'''
                        s.splitlines() # 按行分割， 并且返回结果不带换行符
                        s.splitlines(True) # 按行分割， 并且返回结果带换行符
                        'i am comyn'.partition(' ') # 总是返回一个三元组， 它按传入的分隔符分割一次， 得到 head， tail ， 返回结果是 head, sep, tail
            rpartition 是partition从右往左的版本

        转换
                        s = 'test'
                        s.upper()
                        s.upper().lower()
                        s.title()
                        s.capitalize()
                        'i love python'.title()
                        'i love python'.capitalize()
                        s.center(80)
                        s.zfill(80)
                        s.casefold()
                        'Test TTset'.casefold() # 不同的平台有不同的表现形式， 但是同一平台下，表现形式相同， 通常用来忽略大小写时的比较
                        s.swapcase()
                        'Test'.swapcase()
                        '\t'.expandtabs(4)

        修改
                    s.replace     s.strip       s.lstrip     s.rstrip      s.center     s.ljust       s.rjust

                    s = 'i love python'
                    s.replace('love', 'give up') # 返回新字符串，使用new替换old
                    s = 'i very very love python'
                    s.replace('very', 'not') # 有多少个替换多少个
                    s.replace('very', 'not', 1) # 可选的count参数，指定替换多少次
                只能从前往后替换

                    s = '    hahaha haha    '
                    s.strip() # strip 移除字符串前后的空格
                    s = '\n \r \t haha haha \t \n \r'
                    s.strip() # strip 移除字符串前后的空白
                    s = '#####haha ### haha ###'
                    s.strip('#') # 可以指定移除的字符
                    s = '{{ haha haha }}'
                    s.strip('{} ') # 可以指定移除多个字符
                    s.lstrip('{} ') # lstrip 表现和strip一样， 但是只处理左端
                    s.rstrip('{} ') # rstrip 表现和strip一样， 但只处理右端

                    s = 'test'
                    s.ljust(10) # 原串在左边
                    s.rjust(10) # 原串在右边
                    s.center(10) # 原串在中间

                    s.center(10, '#') # 可以指定填充字符
                    s.ljust(10, '#')
                    s.center(10, '**') # 填充字符串长度只能为1
                    s.center(3) # 如果宽度小于等于原串长度 不做任何操作
                    s.center(11)
                    s.center(11, '#')


        查找
                    s.find   s.rfind   s.index   s.rindex      s.count

                    s = 'i love python'
                    s.find('love') # 从左往右查找， 找到第一个子串love， 返回子串首字母的索引
                    s.find('love1') # 当子串不存在的时候， 返回-1
                    s.find('love1') # 当子串不存在的时候， 返回-1
                    s = 'i very very love python'
                    s.find('very')
                    s.find('very', 3) # start 参数指定从哪里开始查找
                    s.find('very', 3, 10) # end 参数指定到哪里结束查找, end 不包含

            s.rfind('very') # rfind 是find从右往左的版本
                    s.rfind('very', 8) # start和stop意义一样， 事实上， 是先根据start和stop截取字符串，再查找

                    s.index('very')
                    s.index('very', 3)
                    s.index('very', 8) # index 查找， 子串不存在时抛出ValueError
                    s.find('very', 8) # find 查找， 子串不存在时返回-1
                    s.rindex('very') # rindex 是index从右往左的版本

                    s.count('very')
                    s.count('hahah')
                    s.count('very', 3)
                    list(enumerate(s))

        判断
                    s.startswith      s.endswith        s.is*

                    s = 'i very very love python'
                    s.startswith('i very') # 判断字符串是否以某个前缀开始， 返回结果是bool
                    s.startswith('abc')
                    s.startswith('very', 2) # start 参数表示的是从索引start处开始比较
                    s.startswith('very', 2, 5) # end 参数表示从索引end处停止比较， end不包含
                    s.endswith('python') # 判断字符串是否以某个后缀结尾， 返回bool
                    list(enumerate(s))
                    s.endswith('python', 17) # start 参数表示从索引start处开始比较
                    s.endswith('python', 0, 22) # end参数表示到索引end为止， 不包含end

                    s.isalnum()
                    'a'.isalnum()
                            字母或者下划线开头
                            仅包含字母数字和下划线

                    'a'.isidentifier()
                    '34a'.isidentifier()
                    'class'.isidentifier()


###解构与封装####
        解构
                    lst = [1, 2]
                    first, second = lst # 解构
                    print(first, second)
              按照元素顺序，把线性结构的元素赋值给变量
              线性结构是一个有序数据元素的集合。
              常用的线性结构有：线性表，栈，队列，双队列，数组，串。

        封装
                    t = 1, 2
                    type(t)  ##tuple
              定义一个元组，可以省略小括号
              封装出来的一定是元组

        解构的变化
                    lst = list(range(1000))
                    head, *mid, tail = lst

        加星号
                    head, *tail = lst
            加星号可以匹配其他所有元素
                    *head, tail = lst
                    first, sceond, *other = lst
            左边只有一个加星号的变量
                    head, *m1, *m2 = lst   ###报错
            左右有多个加星号的变量
                    v1, v2, v3, v4, v5, v6, v7 = lst  ###报错
            左边变量数超过右边元素个数的时候

    左边变量数小于右边元素元素个数，且左边没有加星号的变量
            元素按照顺序赋值给变量
            变量和元素必须匹配
            加星号变量，可以接受任意个数的元素
            加星号的变量不能单独出现

                    head, *_, tail = lst
            Python的一个惯例， 使用单个下划线 _ 表示丢弃该变量
            单个下划线也是Python合法的标识符， 但是如果不是要丢弃一个变量，通常不要用单个下划线表示一个有意义的变量

                    lst = [1, (2, 3), 5]
                    _, (_, val), *_ = lst
            解构是支持多层次的
                    _, (*_, tail), *_ = lst
                    _, _, tail, *_ = lst
            非常复杂的数据结构，多层嵌套的线性结构的时候，可以用解构快速提取其中的值

                    key, _, value = 'env = prod'.partition('=')
            没有解构，我们也可以活下来， 但是有了解构， 生活很美好
            解构这个特性，被很多的语言借鉴


####集合####
            数学意义上的集合
            没有重复元素

        定义与初始化
                    s = set()
                    s = {1, 2, 3}
                    s = set(range(3))

        增加
                    s.add(3) # 和列表类似， 增加单个元素， 原地修改   append
                    s.add(3) # 增加已存在的元素，什么也不做
                    s.update(range(4, 7)) # 和列表类似， 附加一个可迭代对象， 原地修改 extend
                    s.update(range(4, 9)) # 对于已经存在的元素， 什么也不做

        删除
                    s.remove(0)
                    s.remove(10) # 删除不存在的元素时， 抛出KeyError
                    s.pop()
                    s.clear()
                    s.pop() # 当集合为空时， 抛出KeyError

                    s = set(range(10))
                    s.discard(3)
                    s.discard(10)  # discard 删除不存在的元素的时候， 什么也不做

        remove 删除给定的元素， 元素不存在抛出KeyError
        discard 删除给定的元素， 元素不存在，什么也不做
        pop 随机删除一个元素并返回， 集合为空，抛出KeyError
        clear 清空集合

        修改
                    集合不能修改单个元素

        查找
                    集合不能通过索引
                    集合没有访问单个元素的方法
                    集合不是线性结构， 集合元素没有顺序

                    s = {1, 2, 3, 4, 5, 65, 67, 87}
                    s.pop()

####成员运算符####
                    in           not in
        用于判断一个元素是否在容器中
                     3 in [1, 2, 3, 4]
                     'love' in 'i love python'
                     3 in {1, 2, 3, 4}
        集合的成员运算和其他线性结构的时间复杂度不同

                    lst = list(range(1000000))
                    s = set(range(1000000))

                    %%timeit
                    -1 in lst

                    %%timeit
                    -1 in s
         做成员运算的时候 集合的效率远高于列表
                    lst2 = list(range(100))
                    %%timeit
                    -1 in lst2
        做成员运算时 列表的效率和列表的规模有关

                    s2 = set(range(100))
                    %%timeit
                    -1 in s2
        做成员运算时 集合的效率和集合的规模无关
                    成员运算：          集合 O(1)               列表(线性结构) O(n)


#####集合运算#####
                    s1 = {1, 2, 3}
                    s2 = {2, 3, 4}
                    s1.intersection(s2) # 交集
        存在集合A和B， 对于集合C， 如果C的每个元素既是A的元素，又是B的元素， 并且A和B所有相同的元素都在C找到， 那么C是A和B的交集

                    s2.intersection(s1) # 不修改原来的两个集合， 返回新的集合
                    s1.intersection_update(s2) # _update版本， 原地修改， 返回None， 等效于  s1 = s1.intersection(s2)
                    s2 & s1 # set 重载按位与运算符为 求交集运算 等效于 s2.intersection(s2)
                    s1.difference(s2) # 差集
         集合A和B， 当集合C的元素仅存在A中，但不存在B中， 并且A中存在B中不存在的元素全部存在C中， 那么C是A和B的差集
                    s2.difference(s1)  # 差集没有交换律
                    s1.difference_update(s2) # _update 版本原地修改， 返回None， 相当于  s1 = s1.difference(s2)
                    s1 - s2 # set 重载了运算符 - 执行差集计算，相当于  s1.difference(s2)
                    s1.symmetric_difference(s2) # 对称差集
                    如果把两个集合 A和B看成是一个全集，对称差集是交集的补集
                    s2.symmetric_difference(s1) # 对成差集具有交换律
                    s1.symmetric_difference_update(s2)# 原地修改，返回None 相当于  s1 = s1.symmetric_difference(s2)
                    s1 ^ s2 # set 重载了异或应算符， 执行对称差集运算，相当于 s1.symmetric_difference(s2)
                    s1.union(s2) # 并集
                    s1.update(s2) # 这就是并集的update版本
                    s1 + s2 # 集合并没有重载加法运算符
                    s1 | s2 # set重载了按位或运算符，用于并集计算

集合相关的判断
                    s1 = {1, 2, 3, 4}
                    s2 = {2, 3}
                    集合A里的所有元素都能在集合B里找到， 哪个A是B的子集， B是A的超集
                    s2.issubset(s1) # 判断s2 是否是s1的子集
                    s1.issubset(s2)
                    s1.issuperset(s2) # 判断 s1 是否s2的超集
                    s1.issubset(s1)
                    s1.issuperset(s1)

                    def issubset(s1, s2):
                        for x in s1:
                            if x not in s2:
                                return False
                        return True


                    def issuperset(s1, s2):
                        for x in s2:
                            if x not in s1:
                                return False
                        return True


                    s1.isdisjoint(s2)  # 判断两个集合是否有交集， 如果有交集返回False， 没有交集返回True
                    s3.isdisjoint(s4)
                    s3 = {1, 2}
                    s4 = {3, 4}

####集合的用法####

           有一个api， 它要有认证， 并且有一定权限才可以访问，例如 要求满足权限 A,B， C中任意一项， 有一个用户具有权限 B， C， D， 那么此用户是否有权限访问此API
           有一个任务列表， 存储全部的任务， 有一个列表， 存储已经完成的任务， 找出未完成的任务

####集合的限制####
                            {'a', 'b', 'c'}
                            {1, 2, 3}
                            {1, 'b'}
                            {[1, 2, 3], [2, 2, 3]} # list 不能是集合的元素
                            {bytearray(b'abc')} # bytearray 不能是集合的元素
                            {{3}} # set 不能是集合的元素
                            {(1, 2)} # 元组可以作为集合的元素
                            {b'abc'} # bytes 可以作为集合的元素

            可变类型不能成为集合的元素


            集合元素必须可hash
                       hash(b'abc')
                       hash(1)
                       hash([1, 2,3])   ####报错####
            目前我们所知道的所有的可变类型都是不可hash的， 所有的不可变类型都是可hash



#####字典#####
            字典是一种key-value结构
                        d = {}
                        d = dict()
                        d = {'a': 1, 'b': 2}
                        d = dict([('a', 1), ('b', 2)]) # 可迭代对象的元素必须是一个二元组， 二元组的第0个元素为字典的key， 第1元素为字典的value
                        d = dict({'a': 1, 'b': 3}) # 可以接受一个字典
                        d = dict.fromkeys(range(5)) # 传入的可迭代元素为key， 值为None
                        d = dict.fromkeys(range(5), 'abc') # 传入的可迭代对象的元素为key， 值为abc

            增加/修改
                        d['a'] = 1 # 可以直接使用key作为下标， 对某个不存在的下标赋值，会增加kv对
                        d.update([('c', 3), ('p', 0)]) # update 穿入参数和dict一样
                        d.update({'r': 3, 'd': 3 }) # update 通常用于合并字典
                        d.update([('r', 2), ('d', 2)])

            删除
                        d.pop(0) # pop 方法用于从字典删除一个key， 并返回其value
                        d.pop(0) # 当删除不存在的key的时候， 会抛出KeyError
                        d.pop(0, 'default') # 当删除不存在的key， 并且指定了默认值时， 不会抛出KeyError， 并且返回默认值
                        d.pop(1, 'default') # 有没有default， 是在key不存在的时候才有所区别
                        d.popitem() # popitem **随机** 返回并删除一个kv对的二元组
                        d.clear() # clear 方法清空一个字典
                        d.popitem() # 对空字典popitem， 将抛出KeyError
             访问
                        单个元素的访问
                        d['d'] # 通过key访问value
                        d['c'] # 当key不存在的时候抛出KeyErorr
                        d.get('d') # get方法通过key访问value
                        d.get('c') # get方法访问不存在的key的时候返回None
                        d.get('c', 'default') # 事实上get方法访问不存在的key的时候， 返回默认值， 默认值默认为None

                        d.setdefault('c', 'default')
                        d.setdefault('d', 'default')
                        def setdefault(d, k,default=None):
                            value = d.get(k, default)
                            d[k] = value
                            return value


             字典的遍历
                        字典的元素是成对出现的
                        for x in d:
                            print(x)
                        直接用for in 遍历字典， 遍历的是字典的key
                        d.values() # values 返回一个可迭代对象， 元素是字典的所有value

                        for v in d.values():
                            print(v)
                         d.items() # items 方法返回一个可迭代对象， 元素是字典的所有(k, v)对

                         for x in d.items():
                             print(x)

                         for k, v in d.items():
                             print(k, v)

                          d.keys() # keys 方法返回一个可迭代对象， 元素是字典所有的key
             keys， values， items 返回的都类似生成器, 它并不会复制一份内存
             Python2对应的函数返回的是列表， 会复制一份内存

             字典的限制
                            字典的key不能重复
                            字典的key需要可hash
                            d = {}
                            d[[1, 2, 3]] = 3    ###会报错
                            d[(1, 2, 3)] = 3
                            d[0] = [1, 2, 3]
                            d[0]

              默认字典
                            from collections import defaultdict
                            d1 = {}
                            d2 = defaultdict(list)
                            d1['a']     ###报错
                            d2['a']
                     default初始化的时候， 需要传入一个函数， 这个函数也叫工厂函数，
                     当我们使用下标访问访问一个key的时候， 如果这个key不存在，
                     defaultdict会自动调用初始化时传入的函数， 生成一个对象作为这个key的value

                            d = {}
                            for k in range(10):
                                for v in range(10):
                                    if k not in d.keys():
                                        d[k] = []
                                    d[k].append(v)


                            from collections import defaultdict
                            d = defaultdict(list)
                            for k in range(10):
                                for v in range(10):
                                    d[k].append(v)

              有序字典
                            from collections import OrderedDict
                            d = OrderedDict()
                            d[0] = 3
                            for k, v in d.items():
                                print(k, v)
                     有序字典，会保持插入顺序

                            def f():
                                print('f is called')
                                return 'a'

                            d = defaultdict(f)
                            d['yyy']

                type()   判断对象类型

            列表转换为字典：
                例1：
                    aaa=['a','b','c','d']
                    bbb=[1,2,3,4]
                    ccc=dict(zip(aaa,bbb))

                例2：
                    aaa=['a','b','c','d']
                    bbb=[1,2,3,4]
                    print({aaa[i]:bbb[i] for i in range(len(aaa))})

                例3：
                    aaa=['a','b','c','d']
                    bbb=[1,2,3,4]
                    ccc={}
                    for i in range(len(aaa)):
                        ccc.setdefault(aaa[i],bbb[i])


函数
            函数是Python里组织代码的最小单元

             函数定义
                                def add(x, y):     # 函数定义 def 表示定义一个函数， 紧接着是函数名 函数名后面用一对小括号列出参数列表，参数列表后面使用一个冒号开始函数体
                                    print(x + y)   # 函数体是正常的Python语句，可以包含任意结构
                                    return  x + y  # return 语句表示函数的返回值
                        函数有输入(参数)和输出(返回值)的代码单元， 把输入转化为输出

            函数的调用
                      定义函数的时候,并不会执行函数体，　当调用函数的时候，才会执行其中的语句块
                                add(3, 5)  # 函数使用函数名来调用， 函数名后紧跟一对小括号，小括号里传入函数定义时要求的参数
                                add(3, 4, 5) # 传入参数必须和函数定义时的参数相匹配， 如果不匹配，会抛出TypeError

                                def add(x, y):
                                    ret = x + y
                                    print('{} + {} = {}'.format(x, y, ret))
                                    return ret
                                add(3, 5) # 参数按照定义的顺序传入  这样的传参方法叫做位置参数
                                add(y=3, x=5) # 参数按照定义时的变量名传递， 这样的传参方法叫做关键字参数，关键字参数和顺序无关
                                add(3, y=5) # 位置参数和关键字参数可以混合使用
                                add(x=3, 5) # 当位置参数和关键字参数混合使用时， 位置参数必须在前面， 否则会抛出语法错误

            参数
                   参数默认值
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

            可变参数
                                def sum(*lst):  # 参数前加一个星号， 表示这个参数是可变的， 也就是可以接受任意多个参数, 这些参数将构成一个元组， 此时只能通过位置参数传参
                                    print(type(lst))
                                    ret = 0
                                    for x in lst:
                                        ret += x
                                    return ret
                                sum(1, 2, 3)

                                def connect(**kwargs): # 参数前加两个星号， 表示这个参数是可变的，可以接受任意多个参数， 这些参数构成一个字典，此时只能通过关键字参数传参
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

            参数解构
                                def add(x, y):
                                    ret = x + y
                                    print('{} + {} = {}'.format(x, y, ret))
                                    return ret
                                add(1, 2)
                                add(x=1, y=2)
                                add(1, y=2)
                                t = [1, 2]
                                add(t[0], t[1])
                                add(*t) # 位置参数解构  加一个星号， 可以把可迭代对象解构成位置参数
                                add(*range(2))
                       参数解构发生在函数调用时， 可变参数发生函数定义的时候
                                d = {'x': 1, 'y':2}
                                add(**d) # 关键字参数解构， 加两个星号， 可以把字典解构成关键字参数

                        参数解构的两种形式
                                一个星号 解构的对象：可迭代对象 解构的结果：位置参数
                                两个星号 解构的对象：字典 解构的结果：关键字参数

                                def sum(*args):
                                    ret = 0
                                    for x in args:
                                        ret += x
                                    return ret
                                sum(*range(10))
                        可变参数和参数解构并不冲突

                                def fn(**kwargs):
                                    print(kwargs)
                                fn(**{'a-b':1})
                        关键字参数解构， key必须是str

            keyword-only 参数
                                def fn(*, x):  # *号之后的参数只能通过关键字参数传递，叫做 keyword-only 参数
                                    print(x)

                                fn(x=3)
                                fn(1)         #####报错

                        可变位置参数之后的参数也是keyword-only参数

                                def fn(x, *, y):
                                    print(x)
                                    print(y)
                                fn(1, y=2)

                                def fn(x=1, *, y=5):
                                    print(x)
                                    print(y)

                                def fn(*, x=1, y=5):
                                    print(x)
                                    print(y)

                                def fn(x=1, *, y):
                                    print(x)
                                    print(y)

                        keyword-only 参数可以有默认值
                        keyword-only 参数可以和默认参数一起出现，不管它有没有默认值， 不管默认参数是不是keyword-only参数
                        通常的用法， keyword-only参数都有默认值

                                def fn(*args):
                                    print(args)
                                fn(*{1, 2, 3})

            函数返回值
                                def add(x, y):
                                    return x+y
                                add(1,2)

                                def add(x, y):
                                    return x + y  # return 语句除了返回值之外，还会结束函数， return之后的语句将不会被执行
                                    print('haha')
                                add(1,3)

                                def guess(x):  # 一个函数可以有多个return语句， 执行到哪个return由哪个return返回结果并结束函数
                                    if x > 3:
                                        return '> 3'
                                    return '<= 3'
                                guess(3)
                                guess(5)

                                def fn(x):
                                    for i in range(x):
                                        if i > 3:
                                            return i   # 函数中 return可以提前结束循环
                                    else:
                                        print('not bigger than 3')
                                fn(10)

                                def fn(): # 当函数没有return语句的时候，返回None
                                    pass
                                ret = fn()
                                type(ret)

                                def fn(): # 当函数需要返回读个值时， 可以用封装把返回值封装成一个元组
                                    return 3, 5
                                ret = fn()
                                type(ret)
                                x, y = fn() # 可以通过解构获取多返回值

                                def fn():
                                    return None

                                def fn():  # return None 可以简写为 return， 通常用于结束函数
                                    return
                                fn()

            函数嵌套
                                def outter():
                                    def inner():
                                        print('inner')
                                    print('outter')
                                    inner()
                                 outter()

                     函数可以嵌套定义

            作用域：函数是Python的最小作用域
                     作用域是一个变量的可见范围叫做这个变量的作用域
                                x = 1  # x 定义在全局作用域中
                                def inc(): # 函数内部是一个局部作用域，不能直接只用全局作用域的变量
                                    x += 1
                     全局作用域 局部作用域
                                def fn(): # 变量的作用域为定义此变量的作用域
                                    xx = 1
                                    print(xx)
                      变量的作用域为变量定义同级的作用域

                                def fn(): # 上级作用域对下级作用域是只读可见
                                    xx = 1
                                    print(xx)
                                    def inner():
                                        xx = 2  # 赋值即定义， 在下级作用域里面， 重新定义了xx
                                    inner()
                                    print(xx)
                      不同作用域变量不可见， 但是下级作用域可以对上级作用域的变量只读可见

            全局变量
                                xx = 1
                                def fn():
                                    global xx # global 可以提升变量作用域为全局变量
                                    xx += 1

                                def fn():
                                    global yy # 不管有没有定义都可以提升
                                    yy = 3

                                def fn():
                                    global zz # 提升只是标记，并没有定义变量， 还需要在某处定义变量

                                def fn():
                                    global zz  # global 的提升只对本作用域有用, 如果要在其他非全局作用域使用，也需要做同样的提升
                                    zz = 3
                                    print(zz)

                                def fn2():
                                    global zz
                                    zz += 1
                                    print(zz)
                        除非你清楚的知道global会带来什么，并且明确的知道，非global不行， 否则不要使用global

                                def counter(): # 闭包 函数已经结束，但是函数内部部分变量的引用还存在， python的闭包可以用可变容器实现， 这是也是Python2唯一的方式
                                    c = [0]
                                    def inc():
                                        c[0] += 1 # c[0] = c[0] + 1
                                        return c[0]
                                    return inc
                                f = counter()
                                f()

            nonlocal 关键字
                                def counter():
                                    x = 0
                                    def inc():
                                        nonlocal x  # nonlocal 关键字用于标记一个变量由他的上级作用域定义， 通过nonlocal标记的变量， 可读可写
                                        x += 1
                                        return x
                                    return inc
                                f = counter()

                                def fn():
                                    nonlocal xxxx  # 如果上级没有定义此变量的话，会抛出语法错误

                                def fn(x=[]):
                                    x.append(1)
                                    print(x)

                                def fn(xxyy=[]):
                                    xxyy.append(1)
                                    print(xxyy)
                    函数也是对象， 参数是函数对象的属性，所以函数参数的作用域伴随函数整个生命周期
                    对于定义在全局作用域里面的函数：
                                重新定义
                                del 删除
                                程序结束退出
                    对于局部作用域：
                                重新定义
                                del
                                上级作用域被销毁
                    当使用可变类型作为默认值参数默认值时，需要特别注意
                                def fn(x=0, y=0):
                                    x = 3   # 赋值即定义
                                    y = 3   # 赋值即定义
                                fn.__defaults__


                    使用不可变类型作为默认值
                    函数体内不改变默认值

                                def fn(lst=None):
                                    if lst is None:
                                        lst = []
                                #     else:
                                #         lst = lst[:]
                                    lst.append(3) # 如果传入的参数是非None， 那么改变了传入参数
                                    print(lst)
                                fn.__defaults__

                                def fn(lst=[]):
                                    lst = lst[:] # 影子拷贝
                                    lst.append(x) # 无论如何不传入参数
                                    print(lst)
                    通常如果使用一个可变类型作为默认参数时， 会使用None来代替
                                def counter():
                                    global x1
                                    x1 = 0
                                    def inc():
                                        global x1
                                        x1 += 1
                                        return x1
                                    return inc
                                f = counter()
                                f()

            函数的执行流程
                    main # 全局作用域 f1() # 开启 f2() f3() f4() f5() main
                    当调用函数的时候， 解释器会把当前现场压栈，然后开始执行被调函数， 被调函数执行完成，解释器弹出当前栈顶，恢复现场

            递归函数
                                fib(n) = 1 if n = 0
                                fib(n) = 1 if n = 1
                                fib(n) = fib(n-1) + fib(n-2)

                                def fib(n):
                                    if n == 0:
                                        return 1
                                    if n == 1:
                                        return 1
                                    return fib(n-1) + fib(n-2)
                                fib(4)
                     函数体内调用自身
                     递归函数必须要有退出条件
                     为了保护解释器， Python对最大递归深度有限制
                     尽量避免使用递归

###高阶函数###

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

