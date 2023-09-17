## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

Answer:<br>
T(n) = 3T(n - 1) = 3 * 3T(n - 2) = ... = 3<sup>n</sup>T(n - n) = 3<sup>n</sup>

$O(3^n)$

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

Answer:<br>
T(n) = 2T(n - 1) - 1 = 2 * (2T(n - 2) - 1) - 1 =<br>
4T(n - 2) - 2 - 1 = 4 * (2T(n - 3) - 1) - 2 - 1 =<br>
8T(n - 3) - 4 - 2 - 1 = 2<sup>n</sup>T(n - n) - (2<sup>n</sup> - 1) =<br>
2<sup>n</sup> - 2<sup>n</sup> + 1 = 1

O(1)


## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1): # O(n)
        for j in range(1, n + 1): # O(1) due break
            print("*", end = "")
            break
          print()
```

Answer: O(n)

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j <= n: # O(log(n))
            j = 2 * j
            k = 1
            while k <= n: # O(log(n))
                k = 2 * k
                count += 1
```

Answer: $O(nlog^2(n))$

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j + n // 2 <= n: # O(n)
            j += 1
            k = 1
            while k <= n: # O(log(n))
                k = 2 * k
                count += 1
```

Answer: $O(n^2log(n))$

## 6. Найти сложность приведенной ниже программы: 

```py
def function(n):
    i = 1
    s = 1
    while s <= n: # O(sqrt(n))
        i += 1
        s += i
        print('*')
```

Answer:<br>
Тут присутствует арифметическая прогрессия<br>
S<sub>n</sub> = $(2a_1 + d(k - 1)) * k\over 2$, где выводиться (опуская расчёты), что<br>
$S_n = \dfrac{k^2 + k}{2}$<br>

$O(\sqrt(n))$


## 7. Найти сложность приведенной ниже программы: 

```py
def function(n):
    count = 0
    for i in range(n): # O(n)
        for j in range(i, i * i): # O(n^2)
            if j % i == 0:
                for k in range(j): # O(n^2)
                    print('*')
```

Answer: $O(n^5)$


## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n): # O(sqrt(n))
        s = s + i
        i+=1
```

Answer: $O(\sqrt(n))$ (Объяснения +- аналогичны как к 6 заданию)

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n): # O(n)
            print(i, end= " ")
```

Answer: O(n)

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b): # O(max(a, b))
        if (a > b):
            a = a - b
        else:
            b = b - a
```

Answer:<br>
In the best case: O(1), when a == b<br>
In the worst case: O(max(a, b))

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n: # O(sqrt(n))
        print("Sirius")
        i += 1
```

Answer: $O(\sqrt(n))$

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x): # O(logx(n))
    print("Sirius")
```

Answer: $O(log_x(n))$

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): # O(n)
        for j in range(1,n-math.floor(n/2)+1): # O(n)
            k=1
            for k in range(1,n+1,2*k): # O(log(n))
                 print("Sirius");
```

Answer: $O(n^2log(n))$

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): # O(n)
        for j in range(1,n+1,i): # O(n)
            print("Sirius")

```

Answer: $O(n^2)$

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): # O(n)
        for j in range(1, n+1, 4): # O(n)
            print("Sirius")
```             

Answer: $O(n^2)$

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n): # O(log(n))
        j = n
        while (j > 0): # O(log(n))
            j = j // 2
        i = i * 2
```

Answer: $O(log^2(n))$

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n): # O(log(n))
        j = j * 2
```

Answer: $log(n) + 1$

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N): # O(N)
    a = a + random()
 
for i in range(M): # O(M)
    b = b + random()
 ```

Answer: $O(N + M)$

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0
for i in range(N): # O(n)
    for j in reversed(range(i,N)): # O(n)
        a = a + i + j;
 ```

Answer: $O(n^2)$

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0
for i in range(n//2,n): # O(n)
    for j in range(2,n,pow(2,j)): # O(log(n)) 
        k = k + n / 2
 ```

Answer: $O(n log(n))$

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0): # O(log(n))
    a += i
    i //= 2
``` 

Answer: $O(log(n))$

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n): # O(log k (n))
    i = i * k
```

Абстрагируемся от синтаксиса python

Answer: $O(log_k(n))$

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): # O(n)
    for j in range(i): # O(n)
        value = value + 1
```

Answer: $O(n^2)$