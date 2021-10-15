# Python 编程

## Chapter 1：变量和简单数据类型

### 1.1 变量

- 变量名只能包含字母、数字和下划线。变量名可以字母或下划线开头，但不能以数字开头。
- 变量名不能包含空格，但可使用下划线来分隔其中的单词。
- 不要将 Python 关键字和函数名用作变量名。
- 变量名应既简短又具有描述性。
- 慎用小写字母 l 和大写字母 O，因为它们可能被人错看成数字 1 和 0。

### 1.2 字符串

#### 1.2.1 使用方法修改字符串大小写

	输入：
	name = "ada lovelace"
	print(name.title())
	
	输出：
	Ada LoveLace

==title()==: 是以首字母大写的方式显示每个单词

另外：

	输入：
	name = "ada lovelace"
	print(name.upper())
	print(name.lower())
	
	输出：
	ADA LOVELACE
	ada lovelace

#### 1.2.2 合并字符串

	first_name = "ada"
	last_name = "lovelace"
	full_name = first_name + " " +last_name
	print("Hello, " + "full_name.title()" + "!")
	
	Hello, Ada LoveLace!

#### 1.2.3 删除空白

	>>>  favorite_language  =  'python  '
	>>>  favorite_language 
	'python  '
	>>>  favorite_language.rstrip() 
	'python'
	>>>  favorite_language 
	'python  '

调用方法 .restrip() 可以删除右端多余的空格，但是是暂时的。

左端使用 .lstrip()。

### ==e.g.==

- **个性化消息：** 将用户的姓名存到一个变量中，并向该用户显示一条消息。显示的消息应非常简单，如“Hello Eric, would you like to learn some Python today?”。

	Usr_name = "Eric"
	print("Hello " + Usr_name + "," +" would you like to learn some Python today?")

- **调整名字的大小写：** 将一个人名存储到一个变量中，再以小写、大写和首字母大写的方式显示这个人名。

	name = "Rory Lu"
	print(name.lower())
	print(name.upper())
	print(name.title())

- **名言：** 找一句你钦佩的名人说的名言，将这个名人的姓名和他的名言打印出来。输出应类似于下面这样（包括引号）：

  Albert Einstein once said, “A person who never made a mistake never tried anything new.”

	name = "Albert Einstein"
	remark = "A person who never made a mistake never tried anything new"
	print(name + " once said," + "\"" + remark + "\"")

- **剔除人名中的空白：** 存储一个人名，并在其开头和末尾都包含一些空白字符。务必至少使用字符组合"\t" 和"\n" 各一次。

  打印这个人名，以显示其开头和末尾的空白。然后，分别使用剔除函数lstrip() 、rstrip() 和strip() 对人名进行处理，并将结果打印出来。

	name = "\tRory\tLu\t"
	print(name)
	print(name.lstrip())
	print(name.rstrip())
	print(name.strip())

### 1.3 数字

#### 1.3.1 整数

用两个乘号表示乘方运算

#### 1.3.2 浮点数

结果包含的小树位数可能是不确定的：

	>>> 0.2+0.1
	0.30000000000000004

#### 1.3.3 **使用函数 str() 避免类型错误**

	age  =  23 
	message = "Happy " + age +"rd Birthday!"
	print(message)



## Chapter 2：列表

### 2.1

索引从 0 开始，而不是从 1 开始。

**Python为访问最后一个列表元素提供了一种特殊语法。通过将索引指定为 -1 ，可让Python返回最后一个列表元素**

### ==e.g.==

- 将一些朋友的姓名存储在一个列表中，并将其命名为 names，依次访问该列表中的每个元素，从而将每个朋友的姓名都打印出来。

	names = ['A', 'B', 'C', 'D', 'E']
	print(*names)

### 2.2 修改、添加和删除元素

#### 2.2.1 修改列表元素

	names = ['A', 'B', 'C', 'D', 'E']
	names[0] = 'F'

#### 2.2.2 添加列表元素

1. 表尾添加元素

	motorcycles  =  ['honda',  'yamaha',  'suzuki'] 
	print(motorcycles)
	
	motorcycles.append('ducati') 
	print(motorcycles)


2. 表中插入元素

   **insert( )** 函数插入元素

	motorcycles = ['honda', 'yamaha', 'suzuki'] 
	print(motorcycles)
	
	motorcycles.insert(0, 'ducati') 
	print(motorcycles)
	


#### 2.2.3 添加列表元素

1. 使用 del 语句

	del motorcycles[x]


2. 使用 pop( )

	A = motorcycle.pop(x)

3. 根据值删除元素

	too_expensive  =  'ducati'
	motorcycles.remove(too_expensive）

### ==e.g.==

- **嘉宾名单** ：如果你可以邀请任何人一起共进晚餐（无论是在世的还是故去的），你会邀请哪些人？请创建一个列表，其中包含至少3个你想邀请的人；然后，使用这个列表打印消息，邀请这些人来与你共进晚餐。

	names = ['A', 'B', 'C']
	print("I wanna invite " + name[x] + "to have dinner with me!")

  

- **修改嘉宾名单** ：你刚得知有位嘉宾无法赴约，因此需要另外邀请一位嘉宾。

	names = ['A', 'B', 'C']
	miss = names.pop(1)
	names[1] = 'D'
	print(*names)

  

### 2.3 组织列表

需要以特定的顺序呈现信息

#### 2.3.1 使用方法 sort( ) 对列表进行永久性排序

	cars  =  ['bmw' , 'audi', 'toyota', 'subaru']
	cars.sort()
	print(*cars, sep = ',')


**按字母倒序排序**

	cars  =  ['bmw' , 'audi', 'toyota', 'subaru']
	cars.sort(reverse = True)
	print(*cars, sep = ',')

#### 2.3.2 使用函数 sort( ) 对列表临时排序

要保留列表元素原来的排列顺序，同时以特定的顺序呈现它们，可使用函数 sorted( ) 

	cars  =  ['bmw' , 'audi', 'toyota', 'subaru']
	print(sorted(cars))
	print(sorted(cars, reverse = True))

#### 2.3.3 倒着打印列表

使用方法 reverse( )

	cars  =  ['bmw' , 'audi', 'toyota', 'subaru']
	cars.reverse()
	print(cars)

#### 2.3.4 确定列表的长度

用函数 len( )

### ==e.g.==

- 放眼世界 ：想出至少5个你渴望去旅游的地方。

  - 将这些地方存储在一个列表中，并确保其中的元素不是按字母顺序排列的。

    ```
    place = ["Paris", "Roma", "Iceland", "Tokyo", "Italy"]
    ```

    

  - 按原始排列顺序打印该列表。不要考虑输出是否整洁的问题，只管打印原始Python列表。

    ```
    print(*place)
    ```

    

  - 使用sorted() 按字母顺序打印这个列表，同时不要修改它。

    ```
    print(*sorted(place))
    ```

    

  - 再次打印该列表，核实排列顺序未变。 

  - 使用reverse() 修改列表元素的排列顺序。打印该列表，核实排列顺序确实变了。

  - 使用reverse() 再次修改列表元素的排列顺序。打印该列表，核实已恢复到原来的排列顺序。

  - 使用sort() 修改该列表，使其元素按字母顺序排列。打印该列表，核实排列顺序确实变了。

  - 使用sort() 修改该列表，使其元素按与字母顺序相反的顺序排列。打印该列表，核实排列顺序确实变了。

## Chapter 3：操作列表

### 3.1 遍历整个列表

使用 `for` 循环来打印列表所有元素：

```
magicians = ['alice', 'david', 'carolina']
for magician in magicians:
	print(magician)
```

#### 3.1.1 在 for 循环中执行更多操作

```
print (magician.title() + ",that was a great trick!")
```

### 3.2 避免缩进错误

### 3.3 创建数字列表

#### 3.3.1 使用函数 `range()`	

```
for value in range(1,5):
	print(value)
```

`range` 让 Python 从指定的第一个只开始，并达到指定的第二值之后停止，因此只打印 1～4。

#### 3.3.2 使用 `range()` 创建数字列表

使用函数 `list()` 将 `range()` 的结果直接转换为列表：

```
numbers = list(range(1,6))
print(numbers)
```

```
[1, 2, 3, 4, 5]
```

打印 1～10 内的偶数：

```
evens = list(range(2,11,2))
print(evens)
```

打印前 10 个整数的乘方：

```
squares = [] %创建空表
for value in range(1,11):
	square = value**2
	squares.append(square)
	% or squares.append(value**2)
	
print(squares)
```

==首先应该考虑的是，编写清晰易懂的代码，等到审核功能时，再考虑使用更高效的方法。==

#### 3.3.3 对数字列表的统计计算

```
digits = [1, 2, 3, 4, 5]
print(min(digits))
print(max(digits))
print(sum(digits))
```

#### 3.3.4 列表解析

```
squares = [value**2 for value in range(1,11)]
print(squares)
```

首先要指定一个列表名，然后指定一个左方括号，并定义一个表达式，用于要生成要储存到列表中的值，接下来编写一个 fo让循环，用于给表达式赋值，最后加上右方括号。

### 3.4 使用列表的一部分

#### 3.4.1 切片 

```
players = ['charles', 'martina', 'michael', 'florence', 'eli']
print(player[0:3])
```

如果没有指定第一个索引，将从列表头开始

如果要输出最后三名，可以使用切片 `player[-3:]`



#### 3.4.2 遍历切片

在 for 循环中使用切片

```
for player in players[:3]:
	print(player.title())
```

#### 3.4.3 复制列表

在不指定任何索引的情况下从列表中提取一个切片：

```
my_foods = ['pizza', 'falafel', 'carrot cake']
friend_foods = my_foods[:]
```

### 3.5 元组

Python 将不能修改的值称为**不可变的**，而不可变的列表被称为**元组**。

#### 3.5.1 定义元组

用圆括号来标识：

```
dimensions = (200, 50)
print(dimension(0))
print(dimension(1))
```

#### 3.5.2 遍历元组中所有的值

```
for dimension in dimensions:
print(dimension)
```

#### 3.5.3 修改元组变量

不能修改元组的元素，但是可以给存储元组的变量赋值：

```
dimenaiona = (400, 100)
```

###  3.6 设置代码格式

#### 3.6.1 格式设置指南

PEP 8

#### 3.6.2 缩进

PEP 8 建议每次缩进都使用 4 个空格。

#### 3.6.3 行长

建议每行不超过 80 字符，注释不超过 72 字符。

#### 3.6.4 空行

将程序的不同部分用空行分开。

## Chapter 4：if 语句

### 4.1 示例

```
cars = ['audi','bmw', 'subaru','toyato']

for car in cars:
	if car == 'bwm':
		print(car.upper())
	else:
		print(car.title())
```

### 4.2 条件测试

#### 4.2.1 检查是否相等

True/False。

#### 4.2.2 检查是否相等时区分大小

#### 4.2.3 检查是否不相等

!=

#### 4.2.4 比较数字

#### 4.2.5 检查多个条件

1. 使用 and 检查多个条件

   ```python
   age_0 >= 21 and age_1 >= 21
   (age_0 >= 21) and (age_1 >= 21)
   ```

2. 使用 or 检查多个条件

   相当于 `||` 。

#### 4.2.6 检查特定值是否包含在列表中

使用关键字 `in` 和 `not in`。

```
if 'mushroom' in request_toppings
```

45.2.7 布尔表达式

布尔表达式的结果要么是 True，要么是 False。

在跟踪状态或程序中程序中重要的条件方面，布尔值提供了一种高效的方式。

### 4.3 if 语句

#### 4.3.1 if-else 语句

#### 4.3.2 if-elif-else 语句

```
age = 12
if :
	print
elif :
	print
else 
	print
```

#### 4.3.3 使用多个 elif 代码块

### 使用 if 语句处理列表

#### 4.4.1 检查特殊元素

```
request_toppings = ['mushrooms', 'green peppers', 'extra cheese']

for request_topping in request_toppings:
	if request_toppings == 'green peppers':
		print("Sorry, we are out of green peppers right now")
	else:
		print("Adding" + request_topping + ".")

print("\nFinished making your pizza!")
```

#### 4.4.2 确定列表不是空的

```
requested_toppings = []

if requested_toppings:
	for request_topping in request_toppings:
		print("Adding" + request_topping + ".")
	print("\nFinished making your pizza!")
else:
	print("Are you sure you want a plain pizza?")
```

#### 4.4.3 使用多个列表

## Chapter 5：字典

### 5.1 一个简单的字典

```
alien_0 = {'color': 'green', 'points': 5}

print(alien_0['color'])
print(alien_0['points'])

green
5
```

### 5.2 使用字典

字典是一系列键-值对，与键相关联的值可以是数字、字符串、列表乃至字典。

#### 5.2.1 访问字典中的值

依次指定字典名和放在方括号内的键

#### 5.2.2 添加键-对值

```
alien_0['x_position'] = '0'
alien_0['y_position'] = '25'
```

#### 5.2.3 创建一个空字典

```python
alien_0 = {}

alien_0['color'] = 'green'
alien_0['points'] = 5
```

#### 5.2.4 修改字典里的值

直接赋值

``` 
alien_0['color'] = 'yellow'
```

#### 5.2.5 删除键-值对

使用 `del` 语句：

```
del alien_0['points']
```

#### 5.2.6 由类似对象组成的字典

```
favorite_languages = {
	'jen': 'python',
	'sarah': c,
	'edward': 'ruby',
	'phil': 'pyhton'
}
print("Sarah's favorite language is " + favorite_language['sarah'].title() + ".")
```

### 5.3 遍历字典

#### 5.3.1 遍历所有的键-值对

```
user_0 = {
	'user_name': 'efermi',
	'first': 'enrico',
	'last': 'fermi',
}

for key, value in user_0.items():
	print("\nKey: " + key)
	print("Value: " + value)
```

for a, b in name.==items( )==

#### 5.3.2 遍历字典中所有键

```
favorite_languages = {
	'jen': 'python',
	'sarah': c,
	'edward': 'ruby',
	'phil': 'pyhton'
}

friends = ['phil', 'sarah']
for name in favorite_languages.keys():
	print(name.title())
	
	if name in friends:
		print("	Hi " + name.title() + ", I see your favorite language is " + favorite_language[name])
```

#### 5.3.3 按顺序遍历字典中的所有键

```
for name in sorted(favorite_languages.keys())
```

#### 5.3.4 遍历字典中的所有值

使用方法 `values` ：

```
for language in favorite_languages.values()
```

但这种情况没有考虑重复，为了剔除重复项，可以使用集合 `set`。

```
for language in set(favorite_language.values())
```

### 5.4 嵌套

将一系列字典存储在列表中，或将列表作为值存储在字典中，称为嵌套。

#### 5.4.1 字典列表

```
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}

aliens = [alien_0, alien_1, alien_2]

for alien in aliens:
	print(alien)
	
for alien_number in range(30)
	new_alien = {'color': 'green', 'points': 5, 'speed': slow}
	aliens.append(new_alien)
	
print("Total number of aliens: " + str(len(aliens)))
```

#### 5.4.2 在字典中存储列表

```
pizza = {
	'crust': 'thick',
	'toppings': ['mushrooms', 'extra cheese'],
}

for topping in pizza['toppings']:	
	print("\t" + topping)
```

#### 5.4.3 在字典中存储字典

```
users = {
	'aeinstein': {
		'first': 'albert',
		'last': 'einstein',
		'location': 'princeton',
	},
	
	'mcurie': {
	'first': 'marie',
	'last': 'curie',
	'location' : 'paris',
	}
	
}

for username, user_info in users.items():
	print("\nUsername: " + username)
	full_name = user_info['first'] + " " + user_info['last']
	location = user_info['location']
```

## Chapter 6 用户输入和 while 循环

### 6.1 函数 `input()` 的工作原理

函数 `input()` 让程序暂停运行，等待用户输入一些文本，获取用户输入后， Python 将其存储在一个变量中，方便用户使用。

```
message = input("Tell me something, and I will repeat it back to you: ")
print(message)
```

#### 6.1.1 编写清晰的程序

#### 6.1.2 使用 `int()` 来获取数值输入

```
>>> age  = input("How old are you? ")
How old are you? 21
>>>age
'21'
```

但此时试图进行数值比较，就会发生错误

```
age = int(age)
>>> age >= 18
True
```

#### 6.1.3 求模运算符

求模运算符 `%` 将两个数相除并返回余数。

#### 6.1.4 在 python 2.7 中获取输入

应使用函数 `raw_input()`。

### 6.2 while 循环简介

while 循环不断地运行，直到指定的条件不满足为止。

#### 6.2.1 使用 while 循环

```
current_number = 1
while current_number <= 5:
	print(current_number)
	current_number += 1
```

#### 6.2.2 让用户选择何时退出

```
prompt = "\nTell me something, and I will repeat it back to you:"
prompt += "\nEnter 'quit' to end the program. "
message = ""
while message != 'quit':
	message = input(prompt)
	print(message)
```

#### 6.2.3 使用标志

```
active = True
while active:
	message = input(prompt)
	
	if message == 'quit':
		active = False
	else:
		print(message)
```

#### 6.2.4 使用 break 退出循环

#### 6.2.5 在循环中使用 continue

```
current_number = 0
while current_number < 10:
	current_number += 1
	if current_number % 2 == 0:
		continue
		
	print(current_number)
```

#### 6.2.6 避免无限循环

### 6.3 使用 while 循环来处理列表和字典

#### 6.3.1 在列表之间移动元素

```
unconfirmed_users = ['alice', 'brian', 'candace']
confirmed_users = []

while unconfirmed_users:
	current_user = unconfirmed_users.pop()
	
	print("Vertifying users: " + current_user.title())
	confirmed_users.append(current_user)
```

#### 6.3.2 删除包含特定值的所有列表元素

```
pets = ['dog', 'cat', 'dog', 'goldfish', 'cat', 'rabbit', 'cat']

while 'cat' in pets:
	pet.remove('cat')
```

#### 6.3.3 使用用户输入来填充字典

```
responses = {}

polling_active = True

while polling_active:
	name = input("\nWhat's your name?")
	response = input("Which mountain would you like to climb today?")
	
	responses[name] = response
	
	repeat = input("Would you like to let another person respond?(yes/no) ")
	if repeat == 'no':
		polling_active = False
```

## Chapter 7：函数

### 7.1 定义函数

```
def greet_user():
	print("Hello")

greet_user()
```

#### 7.1.1

向函数传递信息：

```
def greet_user(username):
	print("Hello, " + username.title() + "!")

greet_user('jesse')
```

#### 7.1.2 实参和形参

`username` 是形参，`'jesse'` 是实参。



### 7.2 传递形参

#### 7.2.1 位置实参

```python
def describe_pet(animal_type, pet_name):
	print("\nI have a " + animal_type + ".")
	("My " + animal_type + "'s name is " + pet_name.title()  + ".")
	
describe_pet('hamster', 'harry')
```

1. 调用函数多次
2. 位置实参的顺序很重要

#### 7.2.2 关键字实参

关键字实参是传递给函数的名称-值对。无需考虑函数调用中的实参顺序，还清楚地指出了函数调用中各个值的用途。

```
describe_pet(animal_type = 'hamster', pet_name = 'harry')
```

#### 7.2.3 默认值

给每个形参指定默认值。

```
def describe_pet(animal_type = 'dog', pet_name):
	print("\nI have a " + animal_type + ".")
	("My " + animal_type + "'s name is " + pet_name.title()  + ".")
	
describe_pet(pet_name = 'harry')
```

#### 7.2.4 等效的函数调用

#### 7.2.5 避免实参错误

### 7.3 返回值

#### 7.3.1 返回简单值

```
def get_formatted_name(first_name, last_name):
	full_name = first_name + " " + last_name
	return full_name.title()

musician = get_formatted_name('jimi', 'henrix')
print(musician)
```

#### 7.3.2 让实参变成可选的

```
def get_formatted_name(first_name, last_name, middle_name = ''):
	if middle_name:
		full_name = first_name + " " + middle_name + " " + last_name
	else:
		full_name = first_name + " " + last_name
	return full_name.title()

musician = get_formatted_name('jimi', 'henrix')
print(musician)
```

#### 7.3.3 返回字典

```
def build_person(first_name, last_name):
	person = {'first': first_name, 'last': last_name}
	return person
```

#### 7.3.4 结合使用函数和 while 循环

```
def get_formatted_name(first_name, last_name):
	full_name = first_name + " " + last_name
	return full_name.title()
	
while True:
	print("\nPlease tell me your name: ")
	f_name = input("First name: ")
	l_name = input("Last name: ")
	
	formatted_name = get_formatted_name(f_name, l_name)
```

### 7.4 传递列表

```
def greet_users(names):
	for name in names:
		msg = "Hello, " + name.title() + "!"
		print(msg)
        
usernames = ['hannah', 'ty', 'margot']
greet_users(usernames)
```

#### 7.4.1 在函数中修改列表

将列表传递给函数后，函数就可对其进行修改。

#### 7.4.2 禁止函数修改列表

将列表的副本传递给函数，可以：

```
function_name(list_name[:])
```

切片法创建列表的副本。

### 7.5 传递任意数量的实参

```
def make_pizza(*toppings):
	print(toppings)

make_pizza('pepperoni')
```

#### 7.5.1 结合使用位置实参和任意数量实参

如果要函数接受不同类型的实参，必须在函数定义中将接纳任意数量实参的形参放在最后。Python 先匹配位置实参和关键字实参，再将余下的实参都收集到最后一个形参中。

#### 7.5.2 使用任意数量的关键字实参

``` 
def build_profile(first, last, **user_info):
	profile = {}
	profile['first_name'] = first
	profile['last_name'] last
	for key, value in user_info.items():
		profile[key] = value
	return profile

user_profile = build_profile('albert', 'einstein', location = 'princeton', field = 'physics')
print(user_profile)
```

### 7.6 将函数存储在模块中

#### 7.6.1 导入整个模块

`pizza.py`

```
def make_pizza(size, *toppings):
	print("\nMaking a " + str(size) + "-inch pizza with the following toppings:")
	for topping in toppings:
		print("- " + toppings)
```

`making_pizza.py`

```
import pizza

pizza.make_pizza(16, 'pepperoni')
```

#### 7.6.2 导入特定的函数

```
from module_name import fucton_name
```

#### 7.6.3 使用 as 给函数指定别名

```
from pizza import make_pizza as mp
```

#### 7.6.4 使用函数给模块指定别名

```
import module_name as mn
mn.fuction_name
```

#### 7.6.5 导入模块中所有函数

```
from module import *
```

### 7.7 函数编写指南

应给函数指定描述性名称，且只在其中使用小写字母和下划线。给模块命名时也一样。

注释应该紧跟函数定义后面，并采用文档字符串格式

给形参指定默认值时，等号两边不要有空格，对于函数调用中的关键字实参，也应遵循这种规定。

## Chapter 8：类

面向对象编程。编写类时，定义的一大类对象都有通用的行为。基于类创建对象时，每个对象都自动具备这种通用行为，然后可根据需要赋予对象独特的个性。

通过类来创建对象称为实例化。

### 8.1 创建和使用类

#### 8.1.1 创建 Dog 类

```
class Dog()

	def _init_(self,name,age):
	"""初始化属性name和age"""
		self.name = name
		self.age = age
	
	def sit(self):
		print(self.name.title() + " is now sitting.")
```

==根据约定，在 Python 中首字母大写的名称指的是类。==

1. 方法 `_init_()`

   类中的函数称为**方法**，方法 `_init()` 是一个特殊的方法，每当根据类创建新实例时，Python 都会自动运行它。==开头和末尾各有两个下划线==，旨在避免 Python 默认方法与普通方法发生名称冲突。

   方法 `_init_()` 定义成了三个形参：self、name 和 age。形参 self 必不可少，创建实例时，将自动传入实参 self，每个与类相关联的方法的调用都自动传递实参 self，他是一个指向实例本身的引用，让类能够访问类中的属性和方法。 

   类中定义的变量有前缀 self，以 self 为前缀的变量都可提供类中的所有方法使用，还可以通过类的任何实例来访问这些变量。

2. 在 Python 2.7 中创建类

   ```
   class ClassName(object):
   	--snip--
   ```

   

#### 8.1.2 根据类创建实例

```
class Dog():
	--snip--
	
my_dog = Dog('willie', 6)

print("My dog's name is " + my_dog.name.title() + ".")
```

`_init_()` 并未显式地包含 return 语句。

1. 访问属性

   要访问实例的属性，可使用句点表示法。

2. 调用方法

   根据类创建实例后，可使用句点表示法来调用类中定义的任意方法。

3. 创建多个实例

### 8.2 使用类和实例

#### 8.2.1 Car 类

```
class Car():
	
	def __init__(self, make, model, year):
		self.make = make
		self.model = model
		self.year = year
		
	def get_descriptive_name(self):
		long_name = str(self.year) + ' ' + self.make + ' ' + self.model
		return long_name.title()
		
mu_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())
```

#### 8.2.2 给属性指定默认值

类中每个属性都必须有初始值，哪怕值是 0 或者空字符串。

添加方法 `read_odometer()` ，初始值总是 0.

```
class Car():
	
	def __init__(self, make, model, year):
		self.make = make
		self.model = model
		self.year = year
		self.odometer_reading = 0
		
	def get_descriptive_name(self):
		long_name = str(self.year) + ' ' + self.make + ' ' + self.model
		return long_name.title()
		
	def read_odometer(self):
		print("This car has " + str(self.odometer_reading) + " miles on it.")
		
mu_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())
my_new_car.read_odometer()
```

#### 8.2.3 修改属性的值

1. 直接修改属性的值

   ```
   my_new_car.odometer_reading = 23
   ```

2. 通过方法修改属性的值

   ```
   def update_odometer(self,mileage):
   	self.odometer_reading = mileage
   	
   ---snip---
   my_new_car.update_odometer(23)
   ```

3. 通过方法对属性的值进行递增

   ```
   def increment_odometer(self,miles):
   	self.odometer_reading += miles
   	
   ---snip---
   my_new_car.increment_odometer(23500)
   ```

### 8.3 继承

如果要编写的类是另一个现成类的特殊版本，可以使用继承。当一个类继承另一个类时，将自动获得另一个类的所有属性和方法；原有的类称为父类，而新类称为子类。

#### 8.3.1 子类的方法 `__init__()` 

```
class ElectricCar(Car):
	def __init__(self, make, model, year):
		super.__init__(make, model, year)
		
my_tesla = Electric('tesla', 'model s', 2016)
print(my_tesla.get_descriptive_name())
```

定义子类时，必须在括号内指定父类的名称。

`super()` 是一个特殊函数，它让 Python 调用父类的方法 `__init__()` ，让实例包含父类的所有属性。父类也称为超类（superclass)，因此得名。

#### 8.3.2 Python 2.7 中的继承

```
class Car(object):
	---snip---

class ElectricCar(Car):
	def __init__(self, make, model, year):
		super(ElectricCar,self).__init__(make, model, year)
```

#### 8.3.3 给子类定义属性和方法

让一个类继承另一个类后，可添加区分子类和父类所需的新属性和新方法。

```
class Car():
	---snip---
	
class ElectricCar(Car):
	def __init__(self, make, model, year):
		super.__init__(make, model, year)
		self.battery_size = 70
	
	def describe_battery(self):
	print("This car has a " + str(self.battery_size) + "-kwh battery.")
	
```

#### 8.3.4 重写父类的方法

假设 Car 类有一个名为 `fill_gas_tank` 的方法，对于电动车来说毫无意义，因此可以重写它：

```
class ElectricCar(Car):
	---snip---

	def fill_gas_tank(self):
		print("This car doesn't need a gas tank!")
```

如果有人对电动车调用方法 `fill_gas_tank` ，Python 将自动忽略 Car 类中的方法转而运行上述代码。

#### 8.3.5 将实例用作属性

例如，在不断给 ElectricCar 类添加细节时，会发现其中包含很多专门针对汽车电瓶的属性和方法，可以将这些属性和方法提取出来，放到另一个名为 Battery 的类中，并将一个 Battery 实例用作 ElectricCar 类的一个属性：

```
class Car()
	---snip---

class Battery():
	def __init__(self, battery_size=70):
		self.battrey_size = battery_size
	
	def describe_battery(self):
		print("This car has a " + str(self.battery_size) + "-kwh battery.")
		
class ElecricCar(Car):
	def __init__(self, make, model, year):
		super().__init__(make, model, year)
		self.battery = Battery
		
my_tesla = Electric('tesla', 'model s', 2016)
my_tesla.battery.describe_battery()
```

### 8.4 导入类

#### 8.4.1 导入单个类	

`car.py`

```
class Car():
	def __init__(self, make, model, year):
		self.make = make
		self.model = model
		self.year = year
		self.odometer_reading = 0
		
	def get_descriptive_name(self):
		long_name = str(self.year) + ' ' + self.make + ' ' + self.model
		return long_name.title()
		
	def read_odometer(self):
		print("This car has " + str(self.odometer_reading) + " miles on it.")
		
	def update_odometer(self):
		if mileage >= self.odometer_reading:
			self.odometer_reading = mileage
		else:
			print("You can't roll back an odometer!")
	
	def increment_odometer(self,miles):
		self.odometer_reading += miles
		
```

`my_car.py`	

```
from car import Car

my_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())

my_new_car.odometer_reading = 23
my_new_car.read_odometer()
```

#### 8.4.2 在一个模块中存储多个类

`car.py`

```
class Car()::
	---snip---

class Battery():
	---snip---
	
class ElectricCar(Car):
	---snip---

```

`my_electric_car.py`

```
from car import Car, ElectricCar
```

#### 8.4.3 从一个模块中导入多个类

#### 8.4.4 导入整个模块

```
import car
```

#### 8.4.5 导入模块中所有的类（不推荐）

```
from module_name import *
```

#### 8.4.6 在一个模块中导入另一个模块

`electric_car.py`

```
from car import Car

class Battery():
	---snip---
	
class ElectricCar(Car):
	---snip---
```

`car.py`

```
class Car():
	---snip---
```

`my_cars.py`

```
from car import Car
from electric_car import ElectricCar

---snip---
```

### 8.5 Python 标准库

Python 标准库是一组模块，安装的 Python 都包含它。

比如模块 collections 中的一个类——OrderedDict，它的行为与字典几乎相同，区别只在于记录了键-值对的添加顺序。

`favorite_languages.py`

```
from collections import OrderedDict

favorite_languages = OrderedDict()

favorite_languages['jen'] = 'python'
favorite_languages['sarah'] = 'c'
favorite_languages['phil'] = 'python'

for name, language in favorite_languages.items()
	print(name.title() + "'s favorite language is " + language.title())
```

### 8.6 类编码风格

类名应采用驼峰命名法，即将类名中每个单词的首字母都大写，而不使用下划线。实例名和模块名都采用小写格式，并在单词之间加上下划线。

对于每个类，都应紧跟在类定义后面包含一个文档字符串，简要地描述类的功能，并遵循编写函数的文档字符串时采用的格式约定。

在类中，可使用一个空行来分隔方法；在模块中，可使用两个空行来分隔类。

先导入标准库模块的 import 语句，在添加一个空行，然后导入自己编写的模块的 import 语句。

## Chapter 9：文件与异常

### 9.1 从文件中读取数据

可以一次性读取文件的全部内容，也可以以每次一行的形式逐步读取。

#### 9.1.1 读取整个文件

`pi_digits.txt` :

```
3.1416926535
  8979323846
  2643383279
```

`file_reader.py`

```
with open('pi_digits.txt') as file_object;
	contents = file_object.read()
	print(contents)
```

==关键字 `with` 不需要访问文件后将其关闭，python 会在合适的时候自动将其关闭。==

得到的结果为:

```
3.1416926535
  8979323846
  2643383279
  
```

`read()` 到达文件末尾时会返回一个空字符串，将这个空字符串显示出来就是一个空行。要删除末尾的空行，可以使用 `rstrip()` 删除字符串末尾的空白：

```
print(contents.rstrip())
```

#### 9.1.2 文件路径

```
with open('text_files/filename.txt') as file_object
```

在 windows 系统中用反斜杠 \ 而不是 /。

绝对路径通常比相对路径要长，因此将其储存在一个变量中，再将该变量传递给 open( )。

#### 9.1.3 逐行读取

```
file_name = 'pi_digits.txt'

with open(file_name) as file_object:
	for line in file_object:
		print(line)
```

但这样每行之间会出现空行，因为每行末尾会有换行符，而 print 有人会添加换行符，因此：

```
file_name = 'pi_digits.txt'

with open(file_name) as file_object:
	for line in file_object:
		print(line.rstrip())
```

#### 9.1.4 创建一个包含文件各行内容的列表

```
with open('pi_digits.txt') as file_object;
	lines = file_object.readlines()
	
for line in lines:
	print(line.rstrip())
```

#### 9.1.5 使用文件的内容

```
with open('pi_digits.txt') as file_object;
	lines = file_object.readlines()
	
pi_string = ''

for line in lines:
	pi_string +=lines.rtrip()

print(pi_string)
```

==在读取文本文件时，Python 将其中所有文本都解读为字符串，如果读取的是数字，并要将其作为数值使用，必须用函数 `int()` 将其转换成整数，或者用函数 `float()` 将其转换成浮点数。==

#### 9.1.6 包含一百万位的大型文件

#### 9.1.7 圆周率中包含你的生日嘛

```
with open('pi_digits.txt') as file_object;
	lines = file_object.readlines()
	
pi_string = ''

for line in lines:
	pi_string += lines.rtrip()

birthday = input("Enter your birthday, in the form mmddyy: ")
if birthday in pi_string:
	ptint ...
else:
	print ...
```

### 9.2 写入文件

#### 9.2.1 写入空文件

```
filename = 'programming.txt'

with open(filename, 'w') as file_object
	file_object.write("I love programming!")
```

打开文件时，可指定读取模式( ' r ' )，写入模式（' w '）、附加模式（' a '）或者能让你读取和·写入的模式（' r+ '）。

==Python 只能将字符串写入文件，如果要将数值数据写入文本文件中，必须先使用函数 `str()` 将其转换为字符串格式。==

#### 9.2.2 写入多行

要让每个字符串都单独占一行，需要在 `write()` 语句中包含换行符：

```
with open(filename, 'w') as file_object
	file_object.write("I love programming!\n")
	file_object.write("I love creating new games!\n")
```

#### 9.2.3 附加到文件

以附加模式打开文件时，Python 不会在返回文件对象之前清空文件，而写入文件的行都将添加到文件末尾。

### 9.3 异常

异常是使用 `try-except` 代码块处理的， `try-except` 让 Python 执行指定的操作，同时告诉 Python 发生异常时该怎么办。使用了 `try-except` 代码块时，即便出现异常，程序也将继续运行：显示你编写的友好的错误消息，而不是令用户迷惑的 `traceback`。 

#### 9.3.1 处理 ZeroDivisionError 异常

比如

```
print(5/0)
```

python 无法这样做，因此会看到一个 traceback，这种情况下，Python 将停止运行程序，并指出引发了哪种异常，而我们可根据这些信息对程序进行修改。

#### 9.3.2 使用 try-except 代码块

当认为可能发生了错误时，可编写一个 try-except 代码块来处理可能发生的异常。

```
try:
	print(5/0)
except ZeroDivisionError:
	print("You can't divide by zero!")
```

#### 9.3.3 使用异常避免崩溃

如果程序能妥善地处理无效输入，就能再提示用户提供有效输入，而不至于崩溃。创建一个只执行处罚运算的简单计算器：

```
print("Give me two numbers, I'll divide them.")
print("Enter 'q' to quit.")

while True:
	first_num = input("\nFirst Number:")
	if first_num == 'q':
		break
	second_num = input("\nSecond Number:")
	if first_num == 'q':
		break
	answer = int(first_num) / int(second_num)
	print(answer)
```

#### 9.3.4 else 代码块

```
print("Give me two numbers, I'll divide them.")
print("Enter 'q' to quit.")

while True:
	first_num = input("\nFirst Number:")
	if first_num == 'q':
		break
	second_num = input("\nSecond Number:")
	if first_num == 'q':
		break
	try:
		answer = int(first_num) / int(second_num)
	except ZeroDivisionError:
		print("You can't divide by zero!")
	else:
		print(answer)
```

#### 9.3.5 处理 FileNotFoundError 异常

```
filename = 'alice.txt'

try:
	with open(filename) as f_obj
		contents = f_obj.read()
except FileNotFoundError:
	msg = "Sorry, the file " + filename + " doesn't exist."
	print(msg)
```

#### 9.3.6 分析文本

方法 `split()` 以空格为分隔符将字符串分拆成多个部分，并将这些部分都存储到一个列表中



