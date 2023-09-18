## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**Answer: O(3^n)**

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**Answer: O(1)**

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n): 
    if (n==1):
        return
    for i in range(1, n+1): # n раз
        for j in range(1, n + 1): # 1 раз
            print("*", end = "")
            break
          print()
```
**Answer: O(n)**

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # n раз
        j = 1
        while j <= n: # logn 
            j = 2 * j
            k = 1
            while k <= n: # logn
                k = 2 * k
                count += 1
```
**Answer: O(nlog^2n)**

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # n раз
        j = 1
        while j + n // 2 <= n: # n раз
            j += 1
            k = 1
            while k <= n: # logn
                k = 2 * k
                count += 1
```
**Answer: O(n^2logn)**

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
    for i in range(n): # n раз
        for j in range(i, i * i): # n^2 раз
            if j % i == 0:
                for k in range(j): # n^2 раз
                    print('*')
```
**Answer: O(n^5)**

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
        for i in range(n): # n раз
            print(i, end= " ")
```
**Answer: O(n)**

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```             
**Answer: Лучший O(1)**
        **Худший O(max(a/2; b/2)**
## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n: # log(n**0.5)
        print("Sirius")
        i += 1
```
**Answer: O(log(n**0.5))**

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x): # logx(n)
    print("Sirius")
```
**Answer: O(logx(n))**

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): # n раз
        for j in range(1,n-math.floor(n/2)+1): # n раз 
            k=1;
            for k in range(1,n+1,2*k): # logn раз
                 print("Sirius");
```
**Answer: O(n^2logn)**

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): # n раз
        for j in range(1,n+1,i): # n раз
            print("Sirius");

```
**Answer: O(n^2)**

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): # n раз
        for j in range(1, n+1, 4): # n раз
            print("Sirius")
```
**Answer: O(n^2)**           

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n): # logn раз
        j = n
        while (j > 0): # logn раз
            j = j // 2
        i = i * 2
```
**Answer: O(log^2(n))**

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n): # 1 раз
    j = 1
    while (j <= n): # logn раз
        j = j * 2
```
**Answer: O(logn + 1)**

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N): # N раз
    a = a + random()
 
for i in range(M): # M раз
    b = b + random()
 ```
**Answer: N + M**

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N):  # n раз
    for j in reversed(range(i,N)):  # n раз
        a = a + i + j;
 ```
**Answer: O(n^2)**

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n):  # n раз
    for j in range(2,n,pow(2,j)): # logn раз
        k = k + n / 2;
 ```
**Answer: O(nlogn)**

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0): # logn раз
    a += i
    i //= 2
```
**Answer: O(logn)**

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n): # logn раз
    i = i * k
```
**Answer: O(logk(n))**

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): # n раз
    for j in range(i): # n раз
        value = value + 1
```
**Answer: O(n^2)**
