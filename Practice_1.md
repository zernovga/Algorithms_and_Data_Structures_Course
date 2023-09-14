# Практическая работа 1

## Задание 1

Дан набор функций: $
n!, 2^n, 2n^2, 5n~log~n, 20n, 10n 
$.

Определить при каком значении $n$ $2n^2$ является наиболее эффективной.

*Answer: при n=1*

## Задание 2
Выберете наилучшую асимптотику для $5n+3$:
1. $O(1)$
1. $O(n)$
1. $O(n^2)$
1. $O(n~log~n)$
1. $O(log~n)$ 

*Answer: 5n + 3 -> 5n -> n, O(n) вариант: 2)*
## Задание 3

Найдите ассимптотику в среднем случае для следующего фрагмента кода:

```python
sum = 0
for i in range(0, n * n):
    sum += 1
```
*Answer: sum = 0
for i in range (0, n*n):	-> n*n = n^2
	sum += 1,  O(n^2)*

## Задание 4

Определите колчиество операций суммирования и асимптотику.

```python
def task4(values: list, size: int):
    sum = 0
    for i in range(0, size):
        sum += values[i]
    for i in range(0, 20):
        sum += i
    return sum
```
*Answer: def task4(values: list, size: int):
		sum = 0
		for i in range(0, size): -> size - n раз
    			sum += values[i]
		for i in range(0, 20): -> 20 раз
    			sum += i
		return sum, n + 20, O(n)*

## Задание 5

Определите колчиество операций суммирования и асимптотику.

```python
def task5(values: list, size: int):
    sum = 0
    for i in range(0, size):
        sum += values[i]
        for j in range(0, 20):
            sum += i
    return sum
```
*Answer: def task5(values: list, size: int):
		sum = 0
		for i in range(0, size): -> size(начало цикла)
    			sum += values[i]
    			for j in range(0, 20): -> 20*size (внутри цикла)
        				sum += i
		return sum, 20size+size = 21size, O(n)*

## Задание 6

Определите колчиество операций суммирования и асимптотику.

```python
def task6(values: list, size: int):
    sum = 0
    for i in range(0, size):
        sum += values[i]
        for j in range(0, size):
            sum += i
    return sum
```
*Answer: def task6(values: list, size: int):
		sum = 0
		for i in range(0, size): -> size (начало цикла)
    			sum += values[i]
    			for j in range(0, size): -> size*size(внутри цикла)
       				sum += i
		return sum, size^2+size, O(n^2+n)*

## Задание 7

Сравнивая два данных алгоритма, для каких значений $n$ Алгоритм А быстрее?

Алгоритм А | Алгоритм Б
---|---
Сложений: $n^2+n$ | Сложений: $21n$
Сложность: $O(n^2)$| Сложность: $O(n)$
*Answer: n^2 + n < 21n
n^2 - 20n < 0
n(n-20) < 0
n= 0 или n = 20, для значений до 20*

## Задание 8

Определите колчиество операций суммирования и асимптотику.

```python
def task8(values: list, size: int):
    sum = 0
    j = 0
    for i in range(0, 1000):
        sum += i
    for i in range(0, size):
        j = 1
        while j <= size:
            sum += values[j-1]
            j *= 2
    return sum
```
*Answer: def task8(values: list, size: int):
		sum = 0
		j = 0
		for i in range(0, 1000): -> 1000 раз
    			sum += i
		for i in range(0, size): -> size раз
    			j = 1
    			while j <= size: -> log size
        				sum += values[j-1]
        				j *= 2
		return sum, 1000+ size log size(1000 + n log n), O(n log n)*

## Задание 9

Напишите алгоритм поиска максимального элемента в массиве. Для это алгоритма проверьте его свойства и найдите ассимптотику.
Для написания алгоритма используйте естественный язык, не язык программирования!
*Answer: 1. Берём множество элементов массива
2. Считаем первый элемент максимальным
3. Сравниваем со всеми элементами массива
4. Если значение больше считаем его максимальным, если нет продолжаем двигаться по массиву
5. Пройдя по массиву, выводим максимальный из массива
Асимптотика О(n)*
