## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

Answer: T(n) = 3T(n-1) = 3(3T(n-1-1) = 3(3(3T(n-3)) = 3^n T(n-1) = ^nT(0) = 3^n, O(3^n)

## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

Answer: T(n) = 2T(n-1) - 1 = 2 (2T(n - 1 - 1) - 1 = 2(2T(n-1-1)-1=2(2T(n-2)-1)-1 = 4T(n-2)-2-1 = 4T(n-2) - 3=2^n - 1 - 2^n-1-2^n-2

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
Answer: O(n)

## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): -> n
        j = 1
        while j <= n:
            j = 2 * j -> log n
            k = 1
            while k <= n:
                k = 2 * k
                count += 1
```
O(nlog^2n)
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
                k = 2 * k -> log n
                count += 1
```
Answer: O(n^2 log n) 

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
Answer: O(n^2)
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
Answer: O(n^5)

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n):
        s = s + i
        i+=1
```
Answer: O(n^2)

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n):
            print(i, end= " ")
```
Answer: O(n)

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 


```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```             
In the best case - O(1), in the worst - O (max a, b)

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n:
        print("Sirius")
        i += 1
```
Answer: O(n^0, 5)

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x):
    print("Sirius")
```
Answer: O (log n)

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
Answer: O(n^2 log n)

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1):
        for j in range(1,n+1,i):
            print("Sirius");

```
Answer: O(n^2)

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): -> n
        for j in range(1, n+1, 4): -> n
            print("Sirius")
```             
Answer: O(n^2)

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n):
        j = n -> n log n
        while (j > 0):
            j = j // 2
        i = i * 2 -> log n
```
Answer: O(log^2 n)

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n):
        j = j * 2 -> log n
```
Answer: O(log n)
## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N):
    a = a + random()
 
for i in range(M): -> M
    b = b + random()
 ```
Answer: O(N+M)

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N): -> N
    for j in reversed(range(i,N)):
        a = a + i + j;
 ```
Answer: O(n^2)

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n): -> n
    for j in range(2,n,pow(2,j)):
        k = k + n / 2; -> log n
 ```
Answer: O(n log n)

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0):
    a += i
    i //= 2 -> log n
``` 
Answer: O(logk n)

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n):
    i = i * k -> logk(n))
```
Answer: O(logk(n))

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): -> n
    for j in range(i):
        value = value + 1
```
Answer: O(n^2)
