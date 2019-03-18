

```python
##list 
```


```python
list=["apple", "banana", "cherry"]
```


```python
print(list)#显示
```

    ['apple', 'banana', 'cherry']
    


```python
print(list[1])#通过索引访问
```

    banana
    


```python
print(list[-1])#通过索引逆向访问
```

    cherry
    


```python
print(list[0:2])#通过切片访问
```

    ['apple', 'banana']
    


```python
# 增 
```


```python
list.append("orange") #方法append 在列表末尾增加元素
```


```python
list.insert(0,"pineapple")#方法insert 在特定位置插入元素
```


```python
#删
```


```python
del list[0]# del 语句删除特定位置的元素
```


```python
list.remove("banana")#remove方法删除特定元素
```


```python
list.pop()#pop方法默认删除末尾元素，可加索引指定，删除的值可返回
```




    'cherry'




```python
list.clear()#清空列表
```


```python
#查
```


```python
list.index("apple")#查找apple在list中的索引
```


```python
print(list[2])
```


```python
print("apple" in list)#成员测试
```

    True
    


```python
#改
```


```python
list[1]="blackcurrant"#修改特殊索引对应的值
```


```python
#两个列表间
```


```python
list2=["watermelon","pear"]
```


```python
list.extend(list2)#把list2追加到list末尾
```


```python
list3=list+list2#列表间用加号连接
```


```python
list4 = list.copy()#把list复制给list4
```


```python
list==list4#比较
```




    True




```python
##set
```


```python
set = {"apple", "banana", "cherry"}
```


```python
print(set)#显示
```

    {'banana', 'apple', 'cherry'}
    


```python
for x in set:#遍历
    print(x)
```

    banana
    apple
    cherry
    


```python
#增
```


```python
set.add("orange")#方法add将一个项目添加到集合中
```


```python
set.update(["orange", "mango", "grapes"])#方法update将多个项目添加到集合中
```


```python
#删
```


```python
set.remove("banana")#用方法remove删除特定元素，若项目不存在则会出错
```


```python
set.discard("banana")#用方法discard删除特定元素，若项目不存在也不会出错
```


```python
set.pop()#删除最后一个元素
```


```python
set.clear()#清空集合
```


```python
del set#删除集合
```


```python
#查
```


```python
#集合没有索引，不能用索引来访问元素
```


```python
"banana" in set#成员测试
```




    True




```python
#集合间操作
```


```python
set1 = set.copy()#复制
```


```python
set2 = {"baixiangguo","boluo","banana"}
```


```python
set3=set.union(set2)#交集
```


```python
set4= set.difference(set2)#返回一个新集合,返回set中与set2不同的元素，即set-set2
```


```python
set.difference(set2)#删除set中两个集合的公共元素,返回修改了的set
```


```python
set5=set.intersection(set2)#返回set和set2的交集
```


```python
z = set.isdisjoint(set2)#返回set和set2没有交集的真值
```


```python
##dic
```


```python
thisdict ={
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

```


```python
print(thisdict)#显示
```

    {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
    


```python
x= thisdict["model"]#获取model的值
#x=thisdict.get("model")
print(x)
```

    Mustang
    


```python
for x in thisdict:#遍历字典
    print(x)
    print(thisdict[x])
```


```python
for x in thisdict.values():#遍历字典的值
    print(x)
```


```python
for x, y in thisdict.items():#遍历所有键值
    print(x, y)
```


```python
#增
```


```python
thisdict["color"] = "red"
```


```python
#删
```


```python
thisdict.pop("model")#pop()方法删除具有指定键名的项
```


```python
thisdict.popitem()#popitem()方法删除最后插入的项目
```


```python
del thisdict["model"]#del关键字删除指定键名称的键值对
```


```python
del thisdict#完全删除整个字典
```


```python
thisdict.clear()#清空字典
```


```python
#改
```


```python
thisdict["year"] = 2018
```


```python
#查
```


```python
"model" in thisdict#model是否是字典的键
```


```python
#字典间操作
```


```python
thatdict=thisdict.copy()#复制
```


```python
thisdict==thatdict#判断
```


```python
##list set tuple dic 间转换
```


```python
thislist = list(("apple", "banana", "cherry"))#tuple->list
```


```python
thistuple = tuple(["apple", "banana", "cherry"])#list->tuple
```


```python
thistuple = tuple({"apple", "banana", "cherry"})#set->tuple
```


```python
#tuple->dict
x = ('key1', 'key2', 'key3')#创建一个包含3个键的字典，全部值为0
y = 0
thisdict = dict.fromkeys(x, y)
```


```python
#list->dict
x = ['key1', 'key2', 'key3']#创建一个包含3个键的字典，全部值为0
y = 0
thisdict = dict.fromkeys(x, y)
```


```python
#set->dict
x = ('key1', 'key2', 'key3')#创建一个包含3个键的字典，全部值为0
y = 0
thisdict = dict.fromkeys(x, y)
```
