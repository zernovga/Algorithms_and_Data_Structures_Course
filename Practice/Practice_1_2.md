## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

$T(n) = 3T(n - 1) = 3(3T(n - 2)) = 3(3(3T(n - 3))) = 3(3(3(3T(n - 4)))) = 3^4 * T(n - 4) =$ \
$= ... = 3^n * T(n - n) = 3^n * T(0) = 3^n * 1 = 3^n$ \
Ответ: $3^n$

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

$T(n) = 2T(n - 1) - 1 = 2(2T(n - 2) - 1) - 1 = 2(2(2T(n - 3) - 1) - 1) - 1 = 2(2(2(2T(n - 4) - 1) - 1) - 1) - 1 = 2^4 * T(n - 4) - 8 - 4 - 2 - 1 =$ \
$= ... = 2^n * T(n - n) - \frac{1 * (2^n - 1)}{2 - 1} = 2^n * T(0) - (2^n - 1) = 2^n * 1 - (2^n - 1) = 2^n - 2^n + 1 = 1$ \
Ответ: $1$

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1): # O(n)
        for j in range(1, n + 1): O(1)
            print("*", end = "")
            break
          print()
```

$O(n * 1) = O(n)$ \
Ответ: $O(n)$

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n // 2) = O(n)
        j = 1
        while j <= n: # O(log_2{n})
            j = 2 * j
            k = 1
            while k <= n: # O(log_2{n})
                k = 2 * k
                count += 1
```

$O(n * log_2{n} * log_2{n}) = O(n * log_2{n}^2)$ \
Ответ: $O(n * log_2{n}^2)$

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n // 2) = O(n)
        j = 1
        while j + n // 2 <= n: # O(n // 2) = O(n)
            j += 1
            k = 1
            while k <= n: # O(log_2{n})
                k = 2 * k
                count += 1
```

$O(n * n * log_2{n}) = O(n^2 * log_2{n})$ \
Ответ: $O(n^2 * log_2{n})$

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

$n = \frac{k * (k + 1)}{2}$ \
$2n = k * (k + 1)$ \
$n = k^2$ \
$k = \sqrt{n}$ \
Ответ: $O(\sqrt{n})$

## 7. Найти сложность приведенной ниже программы: 

```py
def function(n):
    count = 0
    for i in range(n): # O(n)
        for j in range(i, i * i): # O(n^2 - n) = O(n^2)
            if j % i == 0: # O(n^2 / 2) = O(n)
                for k in range(j): # O(n^2)
                    print('*')
```

$O(n * n * n^2) = O(n^4)$ \
Ответ: $O(n^4)$

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n):
        s = s + i
        i+=1
```

$n = \frac{k * (k + 1)}{2}$ \
$2n = k * (k + 1)$ \
$n = k^2$ \
$k = \sqrt{n}$ \
Ответ: $O(\sqrt{n})$

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5): # O(1)
        print("Sirius", end ="")
    else:
        for i in range(n): # O(n)
            print(i, end= " ")
```

Ответ: При $0 < n < 5: O(1)$, иначе: $O(n)$

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```             

$O(max(\frac{a}{2}, \frac{b}{2})) = O(max(a, b))$ \
Ответ: $O(max(a, b))$

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n: O(\sqrt{n})
        print("Sirius")
        i += 1
```

Ответ: $O(\sqrt{n})$

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x): # O(\log_x{n})
    print("Sirius")
```

Ответ: $O(\log_x{n})$

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): # O(n / 2) = O(n)
        for j in range(1,n-math.floor(n/2)+1): # O(n / 2) = O(n)
            k=1;
            for k in range(1,n+1,2*k): # O(\log_2{n})
                 print("Sirius");
```

$O(n * n * \log_2{n}) = O(n^2 * \log_2{n})$ \
Ответ: $O(n^2 * \log_2{n})$

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): # O(n)
        for j in range(1,n+1,i): # O(n)
            print("Sirius");

```

$O(n * n) = O(n^2)$ \
Ответ: $O(n^2)$

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): # O(n / 3) = O(n)
        for j in range(1, n+1, 4): # O(n / 4) = O(n)
            print("Sirius")
```

$O(n * n) = O(n^2)$ \
Ответ: $O(n^2)$

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n): # O(\log_2{n})
        j = n
        while (j > 0): # O(\log_2{n})
            j = j // 2
        i = i * 2
```

$O(\log_2{n} * \log_2{n}) = O(\log_2{n}^2)$ \
Ответ: $O(\log_2{n}^2)$

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n): # O(\log_2{n})
        j = j * 2
```

Ответ: $O(\log_2{n})$

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N): # O(N)
    a = a + random()
 
for i in range(M): # O(M)
    b = b + random()
 ```

Ответ: $O(N + M)$

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N): # O(N)
    for j in reversed(range(i,N)): # O(N)
        a = a + i + j;
 ```

$O(N * N) = O(N^2)$ \
Ответ: $O(N^2)$

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n): # O(n / 2) = O(n)
    for j in range(2,n,pow(2,j)): # O(\log_2{n})
        k = k + n / 2;
 ```

Ответ: $O(n * \log_2{n})$

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0): # O(\log_2{N})
    a += i
    i //= 2
```

Ответ: $O(\log_2{N})$

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n): # O(\log_2{N})
    i = i * k
```

Ответ: Если предположить, что код будет работать, то $O(\log_2{N})$

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n):
    for j in range(i):
        value = value + 1
```

$O(\frac{2 + 1 * (n - 1)}{2} n) = O((n / 2) * n) = O(n^2)$ \
Ответ: $O(n^2)$
