# КОЛЛЕКЦИЯ МЕТОДОВ И ФУНКЦИЙ **Python**

## [ОГЛАВЛЕНИЕ](#оглавление)
* [Тернарный оператор](#тернарный-оператор)
* [Моржовый оператор](#моржовый-оператор)
* [Оператор вывода данных](#оператор-вывода-данных)
* [Объявление переменной](#объявление-переменной)
* [Как сделать комментарий?](#как-сделать-комментарий)
* [Интерполяция](#интерполяция)
* [Округление числа](#округление-числа)
* [Таблица списки кортежи множества словари](#таблица-списки-кортежи-множества-словари)
* [Списки](#списки)
* [Генерация списка - примеры](#генерация-списка-примеры-записи)
* [Методы списка](#методы-списка)
* [Срез списка](#срез-списка)
* [Кортежи](#кортежи)
* [Словари](#словари)
* [Множества](#множества)
___
### [Тернарный оператор](#тернарный-оператор)
##### [оглавление](#оглавление)
```python
res = 'Yes' if ((y % 4 == 0) and (y % 100 != 0)) or (y % 400 == 0) else 'No'

print('yes' if (k < m * n) and (k >= m or k >= n) and (k % m == 0 or k % n == 0) else 'no')

countMin = count_1 if count_1 < count_0 else count_0
```
___
### [Моржовый оператор](#моржовый-оператор)
##### [оглавление](#оглавление)
* Оператор `морж` записывается так **`:=`** и представлен в Python 3.8.
* Используется только для присваивания переменных внутри других выражений.
* Можно использовать везде — от циклов до функций генераторов списка или операторов if для обходного присваивания переменных.
```python
# пример в цикле WHILE
list = []
number = None
while number != 0:
    number = int(input("Введите число: "))
    list.append(number)
# можно записать как
while (number := int(input("Введите число: "))) != 0:   # моржовый оператор
    list.append(number)


```
___
### [Оператор вывода данных](#оператор-вывода-данных)
##### [оглавление](#оглавление)
```Python
print(var1, var2, var3)
print(var1)
```
Печать без новой строки
```Python
print(value1, value2, sep='', end='')
sep='' # разделитель для значений
end='' # аргумент по умолчанию явл чимволом новой строки
       # Способ печати без новой строки-установить end в виде пустой строки
print("I am a sentence", "I am also a sentence", sep="; ", end="")
       # I am a sentence; I am also a sentence

```

___
### [Объявление переменной](#объявление-переменной)
##### [оглавление](#оглавление)

```python
a = 1
b = 2
a, b, c = 1, "python", [1,2,3]
print(a, b, c) 

s = 'hello,'
w = "world" 
print(s, w)

```
___
### [Как сделать комментарий?](#как-сделать-комментарий)
##### [оглавление](#оглавление)
`ctrl + /`
```python
# print(1)
```
`alt + shift + a`
```python
'''print(1)
print(1)
print(1)
print(1)'''
```
___
### [Интерполяция](#интерполяция)
##### [оглавление](#оглавление)

```python
a, b, s = 3, 11 ,2022
print(a, b, s)                                 # 3 11 2022
print(a, '-', b, '-', s)                       # 3 - 11 - 2022
print('{} - {} - {}'.format(a, b, s))          # 3 - 11 - 2022
print(f'first - {a} second - {b} third - {s}') # first - 3 second - 11 third - 2022
```
___
### [Округление числа](#округление-числа)
##### [оглавление](#оглавление)
`round(number, ndigits)`
— округляет число `number` до `ndigits` знаков после запятой.

По умолчанию операция проводится до нуля знаков — до ближайшего целого числа. 
```python
round(3.5)      # 4
round(3.75, 1)  # 3.8
```
Если дробная часть равна 0,5, то округляют до ближайшего четного значения.
```python
round(3.5)  # 4
round(4.5)  # 4
```
Так же можно использовать `int`
```python
int(5.9)    # 5
int(-5.77)  # -5
```
**ОКРУГЛЕНИЕ из БИБЛИОТЕКИ MATH**
Для обработки алгоритмов сначала проводят импорт модуля.
```python
import math
```
```python
math.ceil(3.25)     #  4
math.ceil(-3.25)    # -3
# Функция преобразовывает значение в большую сторону (вверх).
```
```python
math.floor(3.9)     #  3
math.floor(-2.1)    # -3
# Округление происходит в меньшую сторону (вниз).
```
```python
math.trunc(7.11)    #  7
math.trunc(-2.1)    # -2
# Функция характеризуется отбрасыванием дробной части.
```
___
### [Таблица списки кортежи множества словари](#таблица-списки-кортежи-множества-словари)
##### [оглавление](#оглавление)
|Тип коллекции|Изменяемость|Индексированность|Уникальность|Создание|
|-------------|:----------:|:---------------:|:----------:|:------:|
| [список](#списки) `list`| + | + | - | [ ], list()|
| [кортеж](#кортежи) `tuple`| - | + | - | ( ), tuple()|
| [множество](#множества) `set`| + | - | + | {elm1, elm2}, set()|
| неизменное множество `frozenset`| - | - | + | frozenset()|
| [словарь](#словари) `dict`| +элементы___ -ключи_______ +значения____ | - | +элементы___ +ключи_______ -значения____ | { }, {key: value,}, dict()|

___
### [Списки](#списки)
##### [оглавление](#оглавление)

```python
list_1 = []          # Создание пустого списка
list_2 = list()      # Создание пустого списка
list_1 = [7, 9, 11, 13, 15, 17]
```
```python
list_1 = [7, 9, 11, 13, 15, 17]
print(list_1[0])     # 7
```
```python
list_1 = list()          # создание пустого списка
for i in range(5):       # цикл выполнится 5 раз
    n = int(input())     # пользователь вводит целое число
    list_1.append(n)     # сохранение элемента в конец списка
# 1-я итерация цикла(повторение 1): n = 12, list_1 = [12]
# 2-я итерация цикла(повторение 2): n = 7,  list_1 = [12, 7]
# 3-я итерация цикла(повторение 3): n = -1, list_1 = [12, 7, -1]
# 4-я итерация цикла(повторение 4): n = 21, list_1 = [12, 7, -1, 21]
# 5-я итерация цикла(повторение 5): n = 0,  list_1 = [12, 7, -1, 21, 0]
print(list_1) # [12, 7, -1, 21, 0]
```
```python
list_1 = [7, 9, 11, 13, 15, 17]
print(len(list_1))   # 6
```
Взаимодействие цикла `for` со списком:

```python
list_1 = [12, 7, -1, 21, 0]
for i in list_1:
    print(i)             # вывод каждого элемента списка
# 1-я итерация цикла(повторение 1): i = 12
# 2-я итерация цикла(повторение 2): i = 7
# 3-я итерация цикла(повторение 3): i = -1
# 4-я итерация цикла(повторение 4): i = 21
# 5-я итерация цикла(повторение 5): i = 0
```
```python
list_1 = [12, 7, -1, 21, 0]
for i in range(len(list_1)):
    print(list_1[i])     # вывод каждого элемента списка
# 1-я итерация цикла(повторение 1): list_1[0] = 12
# 2-я итерация цикла(повторение 2): list_1[1] = 7
# 3-я итерация цикла(повторение 3): list_1[2] = -1
# 4-я итерация цикла(повторение 4): list_1[3] = 21
# 5-я итерация цикла(повторение 5): list_1[4] = 0
```
### [Генерация списка-примеры записи](#генерация-списка-примеры-записи)
##### [оглавление](#оглавление)

```python
list = []

# создаст 10 элементов со значением 0
list = [0] * 10

# создаст с 0-ми значениями в количестве введенным пользователем
list = [0] * int(input('Enter a number: '))
for i in range(len(list)):
    list[i] = random.randint(0, 9) # присвоит случайное число от 0 до 9

# с использванием моржового оператора
for i in range(len(list := [0] * int(input('Enter a number: ')))):
    list[i] = random.randint(0, 9)

# генератор списков
list = [random.randint(0, 9) for i in range(int(input('Enter a number: ')))]

# можно и так
list = [i for i in range(int(input('Enter a number: ')))]
list = [i for i in range(number)]
# возможна и более сложная конструкция
list = [i * 2 for i in range(11) if i % 2 == 0] # [0, 4, 8, 12, 16, 20]

list = [c * 3 for c in 'list' if c != 'i']      # ['lll', 'sss', 'ttt']

list = [c + d for c in 'list' if c != 'i' for d in 'spam' if d != 'a'] # ['ls', 'lp', 'lm', 'ss', 'sp', 'sm', 'ts', 'tp', 'tm']
```
___
Метод **`pop`** удаляет последний элемент из списка:
```python
list_1 = [12, 7, -1, 21, 0]
print(list_1.pop())  # 0
print(list_1)        # [12, 7, -1, 21]
print(list_1.pop())  # 21
print(list_1)        # [12, 7, -1]
print(list_1.pop())  # -1
print(list_1)        # [12, 7]
```
Удаление конкретного элемента из списка. 

Надо указать значение индекса в качестве аргумента функции **`pop`**:
```python
list_1 = [12, 7, -1, 21, 0]
print(list_1.pop(0)) # 12
print(list_1)        # [7, -1, 21, 0] 
```
Функция `insert` - добавление элемента на нужную позицию.
```python
list_1 = [12, 7, -1, 21, 0]
print(list1.insert(2, 11))
print(list1) # [12, 7, 11, -1, 21, 0] 
```
___
### [Методы списка](#методы-списка)
##### [оглавление](#оглавление)
* `append()`: Добавляет элемент в конец списка
       
    ```python
    odd = [1, 3, 5]
    odd.append(7)
    print(odd)       # [1, 3, 5, 7]
    ```
* `extend()`: Добавляет все элементы списка в другой список
       
    ```python
    odd = [1, 3, 5]
    odd.extend([9, 11, 13])
    print(odd)       # [1, 3, 5, 7, 9, 11, 13]
    ```
* `конкатенация` -  также можем использовать оператор **`+`** для объединения списков
    ```python
    odd = [1, 3, 5]
    print(odd + [9, 7, 5])  # [1, 3, 5, 9, 7, 5]
    print(["re"] * 3)       # ["re", "re", "re"]
    ```
* `insert()`: Вставить элемент по указанному индексу
    ```python
    odd = [1, 9]
    odd.insert(1,3)
    print(odd)       # [1, 3, 9] 
    odd[2:2] = [5, 7]
    print(odd)       # [1, 3, 5, 7, 9]
    ```
* `remove()`: Удаляет элемент из списка  
    ```python
    my_list = ['p','r','o','b','l','e','m']
    my_list.remove('p')
    print(my_list)   # ['r', 'o', 'b', 'l', 'e', 'm']
    ```
* `pop()`: Удаляет и возвращает элемент по указанному индексу 
    ```python
    my_list = ['p','r','o','b','l','e','m']
    print(my_list.pop(1))   # 'o'  
    print(my_list)          # ['r', 'b', 'l', 'e', 'm']    
    print(my_list.pop())    # 'm' без индекса удаляет последний элемент списка
    ```
* `del` - ключевое слово, может удалить один или несколько элементов, или полностью весь список
    ```python
    my_list = ['p','r','o','b','l','e','m']
    del my_list[2]   # Удаляем один элемент
    print(my_list)   # ['p', 'r', 'b', 'l', 'e', 'm']

    del my_list[1:5] # Удаляем несколько элементов
    print(my_list)   # ['p', 'm']

    del my_list      # Удаляем весь список
    print(my_list)   # # Ошибка: список не определен
    ```
* `[]` также можно удалить элементы в списке, назначив пустой список фрагменту элементов
    ```python
    my_list = ['p','r','o','b','l','e','m']

    my_list[2:3] = []       # ['p', 'r', 'b', 'l', 'e', 'm']
    print(my_list)

    my_list[2:5] = []
    print(my_list)          # ['p', 'r', 'm']
    ```
* `clear()`: Удаляет все элементы из списка 
    ```python
    my_list = ['p','r','o','b','l','e','m']
    my_list.clear()   
    print(my_list)   # []
    ```
* `index()`: Возвращает индекс первого соответствующего элемента   
    ```python
    my_list = [3, 8, 1, 6, 0, 8, 4]
    print(my_list.index(8)) # 1
    ```
* `count()`: Возвращает количество элементов, переданных в качестве аргумента
    ```python
    my_list = [3, 8, 1, 6, 0, 8, 4]
    print(my_list.count(8)) # 2
    ```
* `sort()`: Сортировка элементов в списке в порядке возрастания 
    ```python
    my_list = [3, 8, 1, 6, 0, 8, 4]
    my_list.sort()
    print(my_list)   # [0, 1, 3, 4, 6, 8, 8]
    ```
* `reverse()`: Обратный порядок элементов в списке 
    ```python
    my_list = [3, 8, 1, 6, 0, 8, 4]
    my_list.reverse()
    print(my_list)   # [8, 8, 6, 4, 3, 1, 0]
    ```
* `copy()`: Возвращает поверхностную копию списка  
    ```python
    my_list = [3, 8, 1, 6, 0, 8, 4]
    list = []
    print(list)      # []
    list = my_list.copy()
    print(list)      # [3, 8, 1, 6, 0, 8, 4]
    ```
___
### [Срез списка](#срез-списка)
##### [оглавление](#оглавление)

```python
list_1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list_1[0])               # 1
print(list_1[1])               # 2
print(list_1[len(list_1)-1])   # 10
print(list_1[-5])              # 6
print(list_1[:])               # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(list_1[:2])              # [1, 2]
print(list_1[len(list_1)-2:])  # [9, 10]
print(list_1[2:9])             # [3, 4, 5, 6, 7, 8, 9]
print(list_1[6:-18])           # []
print(list_1[0:len(list_1):6]) # [1, 7]
print(list_1[::6])             # [1, 7]
```
___
### [Кортежи](#кортежи)
##### [оглавление](#оглавление)
Кортеж — это неизменяемый список.
Кортеж нужен, если:
* необходима защита каких-либо данных от изменений (намеренных или случайных).
* занимает меньше места в памяти и работают быстрее, по сравнению со списками

```python
t = ()               # создание пустого кортежа
print(type(t))       # <class 'tuple'>
t = (1,)
print(type(t))       # <class 'tuple'>
t = (1)
print(type(t))       # <class 'int'>
t = (28, 9, 1990)    
print(type(t))       # <class 'tuple'>
```
Можно распаковать кортеж в независимые переменные:
```python
t = tuple(['red', 'green', 'blue'])
red, green, blue = t
print('r:{} g:{} b:{}'.format(red, green, blue)) # r:red g:green b:blue

```
___
### [Словари](#словари)
##### [оглавление](#оглавление)
**`Словари`** — неупорядоченные коллекции произвольных объектов с доступом по ключу.

В `списках` в качестве ключа используется индекс элемента.

В `словаре` для определения
элемента используется значение ключа (строка, число).

```python
dictionary = {}
dictionary = {'up': '↑', 'left': '←', 'down': '↓', 'right': '→'}
print(dictionary)         # {'up':'↑', 'left':'←', 'down':'↓', 'right':'→'}
print(dictionary['left']) # ← типы ключей могут отличаться
print(dictionary['up'])   # ↑ типы ключей могут отличаться
dictionary['left'] = '⇐'
print(dictionary['left']) # ⇐
print(dictionary['type']) # KeyError: 'type'
del dictionary['left']    # удаление элемента
```
___
### [Множества](#множества)
##### [оглавление](#оглавление)
Одно множество может содержать значения любых типов.

Если у Вас есть два множества, можн совершать над ними любые стандартные операции, например:
* объединение
* пересечение
* разность

```python
colors = {'red', 'green', 'blue'}
print(colors)         # {'red', 'green', 'blue'}
colors.add('red')
print(colors)         # {'red', 'green', 'blue'}
colors.add('gray')
print(colors)         # {'red', 'green', 'blue','gray'}
colors.remove('red')
print(colors)         # {'green', 'blue','gray'}
colors.remove('red')  # KeyError: 'red'
colors.discard('red') # ok
```
```python
a = {1, 2, 3, 5, 8}
b = {2, 5, 8, 13, 21}
c = a.copy()                                     # c = {1, 2, 3, 5, 8}
u = a.union(b)                                   # u = {1, 2, 3, 5, 8, 13,
i = a.intersection(b)                            # i = {8, 2, 5}
dl = a.difference(b)                             # dl = {1, 3}
dr = b.difference(a)                             # dr = {13, 21}
q = a.union(b).difference(a.intersection(b))     # q = {1, 21, 3, 13}
```
**`frozenset`** - неизменяемое или замороженное множество, с которым не будут
работать методы удаления и добавления.
```python
a = {1, 2, 3, 5, 8}
b = frozenset(a)
print(b)             # frozenset({1, 2, 3, 5, 8})
```
___