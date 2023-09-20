## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

$3T(n-1) = 3(3T(n-2)) = ... = 3^nT(n-n) =3^n$

Ответ: $О(3^n)$

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$


$
    2T(n-1) – 1 = 2(2T(n-2) - 1) – 1 = ... = 2^n(T(n - n) - 1)

    T(1) = 2T(1-1) - 1 = 1
    T(2) = 2T(T(1)) - 1 = 1
    T(3) = 2T(T(2)) - 1 = 1
$

Ответ: $О(1)$

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1): # O(n)
        for j in range(1, n + 1): # O(1) так как при первой итерации цикол break
            print("*", end = "")
            break
          print()
```
Ответ: O(n)

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): #O(n) константы не учитывем 
        j = 1
        while j <= n: # O(logn по основанию 2)
            j = 2 * j
            k = 1
            while k <= n: # O(log n по основанию 2)
                k = 2 * k
                count += 1
```
Ответ:$ O(n*log_2^2n)$

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): #O(n)
        j = 1
        while j + n // 2 <= n: #O(n)
            j += 1
            k = 1
            while k <= n: #O(logn по основанию 2)
                k = 2 * k
                count += 1
```

Ответ:$ O(n^2*log_2n)$


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
    for i in range(n): #O(n)
        for j in range(i, i * i): #O(n^2)
            if j % i == 0:
                for k in range(j): #O(n^2)
                    print('*')
```
Ответ:$ O(n^5)$

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n):#O(√ n)
        s = s + i
        i+=1
```
Ответ:$ O(√n)$

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n):#O(n)
            print(i, end= " ")
```
График параллелен Ох до n = 5, после он равномерно растёт.

Ответ:O(n)

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```             
Ответ:

В лучшем O(1). При условии a = b.

В худшем случае O(max(a,b)). Если a либо b = 1.


## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n: #0(√n)
        print("Sirius")
        i += 1
```

Ответ:$ O(√n)$

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x): #O(n/x)
    print("Sirius")
```
Ответ: O(n/x)

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): #O(n) убираем константы 
        for j in range(1,n-math.floor(n/2)+1): #O(n) убираем константы 
            k=1;
            for k in range(1,n+1,2*k): #O(log(n))
                 print("Sirius");
```

Ответ: $(n^2*log_2n)$
 
## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): #O(n) 
        for j in range(1,n+1,i): #O(n) рассматриваем худший случай
            print("Sirius")
```
Ответ: $(n^2)$

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1):  # O(n)
        for j in range(1, n+1, 4): # O(n)
            print("Sirius")
```          
Ответ: $(n^2)$

## 16. Найти сложность приведенной ниже программы:  
```py
def fun(n):
    i = 1
    while (i < n): # O(log n по основанию 2)
        j = n
        while (j > 0): # O(log n по основанию 2)
            j = j // 2
        i = i * 2
```
Ответ: $(log_2^2n)$

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n):
        j = j * 2
```
Ответ: число сравнений $log_2n$

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N):
    a = a + random()
 
for i in range(M):
    b = b + random()
 ```
Ответ: O(N + M) так как циклы никак не связаны

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N): # O(N)
    for j in reversed(range(i,N)): # O(N) 
        a = a + i + j;
 ```
Ответ: $O(n^2)$

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n): # O(n) убираем константы 
    for j in range(2,n,pow(2,j)): # O(log n по основанию 2) убираем константы 
        k = k + n / 2;
 ```

Ответ: $O(n*log_2n)$

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0): #O(log n по основанию 2)
    a += i
    i //= 2
``` 
Ответ: $O(log_2n)$

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n): #O(n)
    i = i * k
```
Ответ: O(n)

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): #O(n)
    for j in range(i): #O(n)
        value = value + 1
```

Ответ: $O(n^2)$