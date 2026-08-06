1. 位置传参（参数顺序）、关键字传参（键等于值，无顺序）二者混用时，关键字参数在位置参数之后
2. 默认参数（缺省参数）放在正常参数之后，可在传参时被修改
3. 传参时每个参数都要传递。
4. 不定长参数：二者混用时，先位置传参后关键字传参
	1. 基于位置传参：不定长位置参数`def calc_data(*args)`args可以接受多个值，形成元组类型的数据。（点奶茶这一主要的数据）
	2. 基于关键字传参：不定长关键字参数`def calc_data(**kwargs)`kwargs可以接受多个值，形成字典类型的数据。通过kwargs.get（）获取键对应的值。（点完后加冰，加糖的选项）
![](assets/Python必要笔记（从函数继续）/file-20260805125056041.png)
5. 传递的参数可以是函数类型的
```python
def add (a,b):
	return a+b
def substract (a,b):
	return a-b
def calc (x,y,oper):
	return oper(x,y)
print(calc(x,y,add))
```
6. 匿名函数/命名函数
```python
a = lambda 参数列表 : 函数体
a()
-------------------------------------------
def 函数名(参数列表):
	函数体
	return
a = 函数名(参数列表)
```
