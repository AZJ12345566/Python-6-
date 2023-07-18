# Python-6-
Python学习笔记(6)
# p23 运算符_赋值运算符
a=3+4
print(a)
#从右到左运算
#支持链式赋值:a=b=c=20
a=b=c=20
print(a,id(a))
print(b,id(b))
print(c,id(c))
#这里输出的标识也相同(内存)

#支持参数赋值
a=20
a+=30
print(a)
#输出50
a-=10
print(a) #输出40
a*=2
print(a) #输出80
a/=3
print(a) #输出为26.6666的死循环
a//=2
print(a) #输出为13.0

#支持系列解包赋值
a,b,c=20,30,40
#要求左右相等
print(a,b,c) #输出为20，30，40

print(--------------交换两个变量的值----------------)
a,b=10,20
print('交换之前:'a，b)
#交换
a,b=b,a
print('交换之后:'a,b)



# p24 运算符_比较运算符
#是对变量或表达式的结果进行大小，真假的比较，结果是bull类型
a,b=10,20
print('a>b吗?',a>b) #false
print('a<b吗?',a<b) #true
print('a<=b吗?',a<=b) #true
print('a>=b吗?',a>=b) #false
print('a==b吗?', a==b) #false
print('a!=b吗?',a!=b) #true

'''一个=为赋值运算符，==称为比较运算符
一个变量有三个部分组成，标识，类型，值
==比较的是值还是标识呢?比较的是值
比较对象的标识使用 is
'''
a=10
b=10
print(a==b) #true  说明a与b的value相等
print(a is b) #true 说明a与b的id标识相等
#这里指向的都是同一块内存空间

lst1=[11,22,33,44]
lst2=[11,22,33,44]
print(lst1==lst2) # value-->true
print(lst1 is lst2) #id-->false
print(id(lst1))
print(id(lst2))
#这种就是值相等但指向不同的内存空间的例子
print(a is not b) #false a的id与b的id是相等的
print(lst1 is not lst2) #true 



# p25 运算符_布尔运算符
a,b=1,2
print('---------------------and 就是C语言的&'-------------)
print(a==1 and b==2) #true      True and True-->True
print(a==1 and b<2) #false      True and false-->false
print(a!1 and b==2) #false      False and True-->False
print(a!=1 and b@=2) #false     False and False-->False

print('---------------------or 就是C语言的|'-------------)
print(a==1 or b==2) #True or True-->True
print(a==1 or b<2)  #True or False-->True
print(a!=1 or b==2) #False or True-->True
print(a!=1 or b!=2) #False or False-->False

print('---------------not 就是C语言的按位取反～----------------')
f=True
f2=False
print(not f)
print(not f2)
#这里输出为False   True

print('---------------in与not in----------------')
s='helloworld'
print('w' in s)
print('k' in s)
print('w' not in s)
print('k' not in s)
