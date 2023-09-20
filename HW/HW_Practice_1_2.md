## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

$
T(n) = 3T(n - 1) = 3(3T(n - 2)) = ... = 3^{(n - 1)}(3T(n - n)) = 3^n \\
\text{Ответ: } O(3^n)
$

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

$
T(n) = 2T(n - 1) - 1 = 2(2T(n - 2) - 1) - 1 = 4T(n - 2) - 2 \\ = 2^nT(n - n) - 2^{n - 1} - 2^{n - 2} - ... - 2^0 = 2^n - (2^n - 1) = 1 \\
\text{Ответ: } O(1) 
$

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1): # O(n)
        for j in range(1, n + 1): #O(1), т.к. одна итерация
            print("*", end = "")
            break
          print()
```
$
O(n) * O(1) = O(n) \\
\text{Ответ: } O(n)
$

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j <= n:
            j = 2 * j # => O(log n)
            k = 1
            while k <= n:
                k = 2 * k # => O(log n)
                count += 1
```

$
O(n) * O(log{_2}{n}) * O(log{_2}{n}) = O(n * log{_2}^2{n}) \\
\text{Ответ: } O(n * log{_2}^2{n})
$

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j + n // 2 <= n: # O(n)
            j += 1
            k = 1
            while k <= n: # O(log n)
                k = 2 * k
                count += 1
```

$
O(n) * O(n) * O(log{_2}{n}) = O(n^2log{_2}{n})
$

## 6. Найти сложность приведенной ниже программы: 

```py
def function(n):
    i = 1
    s = 1
    while s <= n:
        i += 1
        s += i
        print('*')
```
$
\text{Чтобы получить элемент на i итерации надо воспользоваться формулой арифметической прогрессии: }\\
\frac{1 + i}{2} * i \\ \text{отсюда следует, что для нахождения кол-ва итераций для числа n: } \frac{1 + i}{2} * i = n => i^2 + i - n = 0\\
\text{Мы получили квадратное уравнение и для нахождения кол-ва итерация мы берем почти корень от числа n => } O(\sqrt{n})
$

## 7. Найти сложность приведенной ниже программы: 

```py
def function(n):
    count = 0
    for i in range(n): # O(n)
        for j in range(i, i * i): # O(n^2)
            if j % i == 0:
                for k in range(j): # O(n)
                    print('*')
```

$
\text{Ответ: } O(n^4)
$

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n):
        s = s + i # увеличиваем на 1
        i+=1
```
$
\text{Ответ: }O(n)
$

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n): # O(n)
            print(i, end= " ")
```
$
\text{Ответ: }O(n)
$

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```
$
\text{Если взять два числа: a = 100, b = 1, то программа выполнится за O(100) => } O(max(a, b))
$

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n: # O(n ** .5)
        print("Sirius")
        i += 1
```
$
\text{Ответ: } O(\sqrt{n})
$

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  # в худшем случае O(n)
  # в лучшем случае O(1)
  for i in range(1, n, i * x):
    print("Sirius")
```
$
\text{Ответ: } O(n)
$

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): # O(n)
        for j in range(1,n-math.floor(n/2)+1): # O(n)
            k=1;
            for k in range(1,n+1,2*k): # O(n)
                 print("Sirius");
```

$
\text{Ответ: } O(n^3)
$

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): # O(n)
        for j in range(1,n+1,i): # O(n)
            print("Sirius");

```

$
\text{Ответ: } O(n^2)
$

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): # O(n)
        for j in range(1, n+1, 4): # O(n)
            print("Sirius")
```

$
\text{Ответ: } O(n^2)
$

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n): # O(log n)
        j = n
        while (j > 0): # O(log n)
            j = j // 2
        i = i * 2
```

$
\text{Ответ: } O(log{_2}^2{n})
$

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n): # O(log n)
        j = j * 2
```
$
\text{Ответ: } O(log{_2}{n})
$

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N): # O(N)
    a = a + random()
 
for i in range(M): # O(M)
    b = b + random()
 ```

$
\text{Ответ: } O(N + M)
$

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N): # O(N)
    for j in reversed(range(i,N)): # O(N)
        a = a + i + j;
 ```

$
\text{Ответ: } O(N^2)
$

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n): # O(n)
    for j in range(2,n,pow(2,j)): # O(log n)
        k = k + n / 2;
 ```

$
\text{Ответ: } O(n * log{_2}{n})
$

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0):
    a += i
    i //= 2 # O(log n)
``` 

$
\text{Ответ: } O(log{_2}{n})
$

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n):
    # в худшем случае O(n)
    # в лучшем случае O(1)
    i = i * k
```
$
\text{Ответ: } O(n)
$

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): # O(n)
    for j in range(i): # O(n)
        value = value + 1
```

$
\text{Ответ: } O(n^2)
$