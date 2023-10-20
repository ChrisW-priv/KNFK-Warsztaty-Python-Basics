---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.15.2
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---


# Jak działa Jupyter Notebook?
Jupyter notebook jest narzędziem pozwalającym na interaktywne wykonywanie kodu
i analizę efektów. Składa się z komórek które w zależności od typu można albo
wykonać albo przeczytać. Tekst który czytasz to tekst w komórce 'markdown' (tekst)

Poniżej przykład komórki z kodem pythona do wykonania:
```python
print("Komórka wykonana!")
```

# Zmienne


## Nowe zmienne
W pythonie jak w każdym języku programowania potrzebne jest żeby móc zapisać 
stan do wykorzystania później (lub od razu). W pythonie jest to proste ponieważ
musimy tylko nadać nazwę zmiennej i przypisać do niej wartość.

Na przykład:
```python
a = 1
```

Nie musimy martwić się tym czy `a` jest cyfrą czy ułamkiem czy tekstem. Zmienna
to zmienna. Jak będziemy musieli poznać jej wartość najprościej ją wydrukować
na ekran konsoli. 
```python
print(a)
```

W notatnikach jupyter nie musimy używać print jeżeli chcemy poznać tylko jedną 
zmienną:
```python
a
```

Nie każda nazwa jest dozwolona ale w razie problemu łatwo to zmienić
```python
# spróbuj zrobić niedozwoloną nazwę (przy wykonaniu komórki otrzymasz error
liczba = 7
```

## Dostępne typy


### Integer vs Float

```python
# intigers:
a = 1
# floats:
b = 1.0
```

```python
a==b
```

```python
a = 3.5
a = int(a)
a
```

```python
a = '3'
a
```

```python
float(a)
```

```python
a = int(a)

# a = a+1
a+=1
# a = a-1
a-=1
# a = a*2
a*=2
# a = a/2
a/=2
```

```python
a = 16
b = 3
# a mod b - reszta z dzelnia
a%b
```

```python
a = 16
b = 3
# dzielenie i dzielenie bez reszty
a/b, a//b
```

```python
a=3
b=3
a/b, a//b
```

```python
0.9999999999999999
```

```python
0.99999999999999999
```

```python
0.1 + 0.2
```

### Booleans
```python
a = True
b = False
```

```python
int(a)
```

```python
int(b)
```

```python
0, None
bool(0)
```

```python
bool(12898109481098421)
```

```python
a == b
```

```python
c = a!=b
c
```

```python
a>b
```

```python
not a==b
```

```python
condition = True
b = 0
if condition:
    b = 1
else:
    b = 2
b
```

```python
a = True
b = True
c = 0
if not a:
    c = 1
elif a and b:
    c = 2
elif a or b:
    c = 3
elif not a or b:
    c = 4 # will never execute !
else:
    c = 5 # in this excample this one won't either
    
c
```

### String
```python
"Hello World"
```

```python
'Hello World'
```

```python
"Hello World" == 'Hello World'
```

```python
'It was her\'s book'
```

```python
"""Hello World. It's my first time learning python. Heard someone say "It's best lang for beginners" """
```

```python
new_line = '\n'
tabulation = '\t'
```

```python
a = 'Hello'
b = 'World'
c = a + ' ' + b
c
```

```python
a = 'Hello'
b = 'World'
c = f'{a} {b}'
c
```

```python
a = 'My first python course.'
a
```

```python
a[0], a[1], a[-1], a[:8], a[:-1], a[::-1]
```

```python
b = a.split(' ')
b
```

```python
c = ' '.join(b)
# c = ""
# for seq in b:
#     c += seq
#     if seq != b[-1]:
#         c += " "
c      
```

```python
a = "123"
b = "456"
a+b
```

### List and Tuples
```python
# list
a = [1,2,3,4,5,6]
# tuple
b = (1,2,3,4,5,6)
```

```python
a==b
```

```python
a = [1,2,3,4,5,6] # <- elements
#   [0,1,2,3,4,5] <- index starts from 0!
```

```python
a += [7,8,9] + [10]
a
```

```python
a[1] # second elemnet in list
```

```python
a[:4] # first 4 elements
```

```python
a[-1] # last element
```

```python
a[::2] # every second element in list
```

```python
a[::-1] # list but reversed
```

```python
sum(a)
```

```python
len(a)
```

```python
a.append(10) # a += [10]
a
```

```python
d = []
for elem in b:
    if elem != 1:
        d.append(elem)
d
```

```python
d = [elem for elem in b if elem != 1]
d
```

```python
a.remove(1)
a
```

```python
a.index(3)
```

```python
b = a.pop(-1)
b, a
```

```python
a.insert(0,1)
a
```

```python
a[0] = 0
a
```

```python
f = [0 for _ in range(15)]
f
```

```python
# Not a tuple!!!
c = (1)
c
```

```python
type(c)
```

```python
c = 1,
c, type(c)
```

```python
c = (1,2,3,4,5,6)
c += (7,8,9)
c
```

```python
c[0] = 5
c
```

```python
c = list(c)
c[0] = 5
tuple(c)
```

### Dictionary
```python
a = {}
a
```

```python
a = {'apple': 2, 
     'bananas':5, 
     'potatoes': 6
    }
a
```

```python
a.get('apple')
```

```python
a['candy'] = 7
a
```

```python
a['apple'] = 2.5
a
```

```python
print('Keys of dictionary assigned to "a" variable:')
for key in a:
    print(key)
```

```python
w = 0
for key in a:
    w += a.get(key)
w
```

```python
for key in a:
    print(key, a.get(key))
```

### Set
#TODO


# Pętle
W pythonie mamy dostepne dwie petle: `for` oraz `while`. Ponieważ większość 
algorytmów można napisać za pomocą obu to generalnie miejmy preferencję dla 
`for`. Jest szybsza i prostsza do zrozumienia.


## Pętle for

Żeby `iterować` przez zakres wartości:

Wszystkie liczby od zera do wartości: <zero, value>
```python
for i in range(5):
    print(i)
```
Wszystkie od początku do końca - 1 <begin, end)
```python
for i in range(1, 6):
    print(i)
```
Wszystkie nieparzyste od 1 do 9 (jak zrobić 2-10?)
```python
for i in range(1, 10, 2):
    print(i)
```
Elementy listy 
```python
for x in ['a', 'b', 'c']:
    print(x)
```
Elementy listy ale gorzej:
```python
v = ['a', 'b', 'c']
for i in range(len(v)):
    print([v[i]])
```
Elementy listy + index (najlepsza opcja):
```python
v = ['a', 'b', 'c']
for i, x in enumerate(v):
    print("Index of element:", i, "Value:", x)
```

## Pętle while
```python
condition = True
while condition:
    for i in range(20+1):
        if i == 15:
            condition = False
            break
        else:
            print(i)
```

```python
n = 0 
while n < 20+1:
    n += 1
    print(n)
    if n == 15:
        break
```

```python
element = 8
for i in range(10):
    print(i)
    if i == element:
        print('Element found!')
        break
else:
    print('Element not in range!')
```

```python
element = 12
n = 0 
while n < 20:
    n += 1
    print(n)
    if n == element:
        break
else:
    print('printed all numbers')
```

# Ćwiczenia podstawy
Zrób program co robi coś fajnego:
#TODO


# Funkcje
#TODO


# Ćwiczenia funkcje
#TODO


# IO - Input Outpus w praktyce
#TODO
```python
with open('sample.txt') as file:
    data = file.read()
data
```

```python
data_by_row = data.split('\n')
data_by_row
```

```python
data_by_row[0].split(',')
```

```python
data_by_row[1].split(';')
```

```python
data_by_row[2].split(' ')
```

```python
rows = []
for row in data_by_row:
    for delim in [',', ';', ' ']:
        if delim in row:
            rows.append(row.split(delim))
rows
```

```python
for i, row in enumerate(rows):
    rows[i] = '\t'.join(row)
rows
```

```python
new_data = '\n'.join(rows)
```

```python
with open('refactored.txt', 'w') as new:
    new.write(new_data)
```

# Importowanie modułów
#TODO
```python
import random
a = random.random()
a
```

```python
from random import random
a = random()
a
```

```python
import os
a = 'C:/Users/KW/'
b = 'Desktop/'
c = 'Folder on desktop'
d = os.path.join(a, b, c)
d
```

