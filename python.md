### 基本方法

#### 字母转unicode

```python
#字母转Unicode
ord('a')

#unicode转字母
chr(unicode)
```

**输出a~z**

```python
for i in range(0,26):
    print(chr(ord('a')+i))
```

#### 大小写转换



### 列表

### 字典（哈希）

#### 基本用法

```python
# 新建字典
dict{}

# 初始化字典为空字典
for i in range(0,25)
	dict[char(ord('a')+i)] = None

# 由键获取值
dict.get('a')

# 删除键值对
dict.pop("a")

# 以列表返回一个字典所有的键
dict.keys()

# 遍历字典
dict.items() #字典变为键值对的元组，可遍历

dict = {}
for i in range(0,25):
    dict[chr(ord('a')+i)] = i
for k,v in dict.items():
    print(k+":"+str(v))
    
# 输出a:0
#    b:1
#    c:2
#    d:3
#    e:4
```



#### Leetcode：242.：

**输入两个单词看是否是相同字母的不同排列组合**

```python
dict_a = {}
dict_b = {}
tag = 0
for i in range(0,26):
    dict_a[chr(ord('a')+i)] = 0
    dict_b[chr(ord('a') + i)] = 0
aaa = input()
bbb = input()
for i in aaa:
    dict_a[i] += 1
for i in bbb:
    dict_b[i] +=1
for i in range(0,25):
    if dict_a[chr(ord('a') + i)] != dict_b[chr(ord('a') + i)]:
        print("false")
        tag = 1
        break
if tag == 0:
    print("true")



```

#### Leetcode：1.两数之和

**输入列表（如[1,2,3,4]），再输入目标值（如6），看是列表中哪两个数字之和**

```python
# 思路：哈希，建是列表所有的两两数字和，值是那两个数，比如{6:[2,4],},为2和4的和为6，由答案找过程
print("input num:")
num = input()
list = []
dict = {}
print("input the list:")
for i in range(0, int(num)):
    aaa = input()
    list.append(int(aaa))
list = sorted(list)
for i in range(0, len(list)):
    for j in range(i+1, len(list)):
        dict[list[i]+list[j]] = [str(list[i]),str(list[j])]
print("input_the_sum:")
sum = input()
print(dict[int(sum)])

```



### 集合

#### 基本用法

```python
# 将列表转化为集合
aaa = [1,1,2,2,3]
set(aaa)

# 创建空集合
aaa = {}
aaa.add( 1 )
aaa.add("hello") # 可以添加以一个集合
aaa.discard("hello") # 删除元素
```



#### Leetcode：349. 两个数组的交集

```python
dict_a = {}
dict_b = {}
both_have = []
for i in range(0,10):
    dict_a[i] = 0
    dict_b[i] = 0
aaa = input()
bbb = input()
for i in aaa:
    dict_a[int(i)] += 1
for i in bbb:
    dict_b[int(i)] += 1
for i in range(0, 10):
    if (dict_a[i] != 0) and (dict_b[i] != 0):
        both_have.append(i)
both_have = sorted((both_have))
for i in both_have:
    print(i)

```



### 正则化

### 读写文件

### 面向对象