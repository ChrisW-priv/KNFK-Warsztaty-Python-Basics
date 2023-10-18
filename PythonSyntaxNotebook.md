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
- string
- booleans
- list 
- tuple
- set
- dictionary

# Pętle

W pythonie mamy dostepne dwie petle: `for` oraz `while`. W znaczącej przewadze
będziecie używać for dlatego na niej się skupimy (while działa tak samo jak 
wszędzie)

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
# Ćwiczenia podstawy
Zrób program co robi coś fajnego:
#TODO
# Funkcje
#TODO
# Ćwiczenia funkcje
#TODO
# IO - Input Outpus w praktyce
#TODO
# Importowanie modułów
#TODO
