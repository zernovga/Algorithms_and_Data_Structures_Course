## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**ответ: O(3^n)**

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**Ответ: O(1)**

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1):
        for j in range(1, n + 1):
            print("*", end = "")
            break
          print()
```

Ответ: O(n)

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1):
        j = 1
        while j <= n:
            j = 2 * j
            k = 1
            while k <= n:
                k = 2 * k
                count += 1
```

Ответ: O(n log^2 n)

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1):
        j = 1
        while j + n // 2 <= n:
            j += 1
            k = 1
            while k <= n:
                k = 2 * k
                count += 1
```

**Ответ: O(n^2 * log n)**

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

## 7. Найти сложность приведенной ниже программы: 

```py
def function(n):
    count = 0
    for i in range(n):
        for j in range(i, i * i):
            if j % i == 0:
                for k in range(j):
                    print('*')
```

**Ответ: O(n^5)**

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n):
        s = s + i
        i+=1
```

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n):
            print(i, end= " ")
```

Ответ: O(n)

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```             
Ответ: худший случай: O(max a/2, b/2)
лучший: O(1)

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n:
        print("Sirius")
        i += 1
```
Ответ: O(n^0,5)

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x):
    print("Sirius")
```

Ответ: O(log n)

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)):
        for j in range(1,n-math.floor(n/2)+1):
            k=1;
            for k in range(1,n+1,2*k):
                 print("Sirius");
```

Ответ: O(n^2 * log n)

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1):
        for j in range(1,n+1,i):
            print("Sirius");

```

Ответ: O(n^2)

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1):
        for j in range(1, n+1, 4):
            print("Sirius")
```             

Ответ: O(n^2)

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n):
        j = n
        while (j > 0):
            j = j // 2
        i = i * 2
```

Ответ: O(log^2 n)

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n):
        j = j * 2
```

Ответ: O(log n)

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N):
    a = a + random()
 
for i in range(M):
    b = b + random()
 ```

Ответ: O(N + M)

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N):
    for j in reversed(range(i,N)):
        a = a + i + j;
 ```

Ответ: O(n^2)

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n):
    for j in range(2,n,pow(2,j)):
        k = k + n / 2;
 ```

Ответ: O(n log n)

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0):
    a += i
    i //= 2
``` 

Ответ: O(log n)

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n):
    i = i * k
```

Ответ: O(log n)

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n):
    for j in range(i):
        value = value + 1
```
Ответ: O(n^2)
