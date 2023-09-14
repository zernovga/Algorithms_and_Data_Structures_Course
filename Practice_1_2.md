## 1. Найти сложность приведенного ниже соотношения:  

$
T(n) = \begin{cases} 
    3T(n-1), &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**ответ:T(n) = 3T(n-1) = 3(3T(n-1-1)) = 3^n**
## 2. Найти сложность приведенного ниже соотношения:  
$
T(n) = \begin{cases} 
    2T(n-1) – 1 &\text{если } n>0,\\
    1, &\text{иначе} 
\end{cases}
$

**ответ:T(n) = 2T(n-1)-1 = 2(2T(n-1-1)-1)-1 = 4T(n-2)-3 = 4(2T(n-2-1)-1)-2-1 = 8T(n-3)-4-2-1 = 2^nT(n-n)-2^(n-1)-…-2^0 = 2^n-(2^n-1) = 1**

## 3. Найти сложность приведенной ниже программы:

```python
def funct(n):
    if (n==1):
        return
    for i in range(1, n+1): # O(n)
        for j in range(1, n + 1):
            print("*", end = "")
            break
          print()
```
**ответ:O(n)**


## 4. Найти сложность приведенной ниже программы:

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j <= n: # O(log2(n))
            j = 2 * j
            k = 1
            while k <= n: # O(log2(n))
                k = 2 * k
                count += 1
```
**ответ:O(n(log2(n))^2)**

## 5. Найти сложность приведенной ниже программы: 

```python
def funct(n):
    count = 0
    for i in range(n//2, n+1): # O(n)
        j = 1
        while j + n // 2 <= n: # O(n)
            j += 1
            k = 1
            while k <= n: # O(log2(n))
                k = 2 * k
                count += 1
```
**ответ:O(n^2*log2(n))**

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
**ответ:-**

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
**ответ:O(n^5)**

## 8. Найти сложность приведенной ниже программы: 

```python
def function(n):
    i = 1
    s = 1
    while (s < n): # O(n)
        s = s + i
        i+=1
```
**ответ:O(n)**

## 9. Найти сложность приведенной ниже программы: 


```python
def fun(n):
    if (n < 5):
        print("Sirius", end ="")
    else:
        for i in range(n):
            print(i, end= " ")
```
**ответ:O(n)**

## 10. Найти сложность приведенной ниже программы в лучшем и в худшем случае: 

```python
def fun(a, b):
    while (a != b):
        if (a > b):
            a = a - b
        else:
            b = b - a
```     
**ответ: лучший случай:O(1), худший случай:O(max(a,b))**        

## 11. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    i = 0
    while i*i < n:
        print("Sirius")
        i += 1
```
**ответ:O(n^0.5)**

## 12. Найти сложность приведенной ниже программы: 

```py
def fun(n, x):
  for i in range(1, n, i * x):
    print("Sirius")
```
**ответ:O(log x (n))**

## 13. Найти сложность приведенной ниже программы: 

```py
import math
 
def fun(n):
    for i in range(0,math.floor(n/2)): # O(n)
        for j in range(1,n-math.floor(n/2)+1): # O(n)
            k=1
            for k in range(1,n+1,2*k): # O(log2(n))
                 print("Sirius")
```
**ответ:O(n^2*log2(n))**

## 14. Найти сложность приведенной ниже программы: 

```python
def fun(n):
    for i in range(1,n+1): # O(n)
        for j in range(1,n+1,i): # O(n)
            print("Sirius")

```
**ответ:O(n*log(n))**

## 15. Найти сложность приведенной ниже программы: 

```py
def fun(n):
    for i in range(n//3 + 1): # O(n)
        for j in range(1, n+1, 4): # O(n)
            print("Sirius")
```  
**ответ:O(n^2)**           

## 16. Найти сложность приведенной ниже программы:  

```py
def fun(n):
    i = 1
    while (i < n): # O(log2(n))
        j = n
        while (j > 0): # O(n)
            j = j // 2
        i = i * 2
```
**ответ:O(n*log2(n))**         

## 17. Найти какое число сравнений будет сделано при выполнении следующего фрагмента кода?  
```py
def fun(n):
    j = 1
    while (j <= n):
        j = j * 2
```
**ответ:O(log2(n))**   

## 18. Найти сложность приведенной ниже программы: 
 
```py
a = 0
b = 0
for i in range(N):
    a = a + random()
 
for i in range(M):
    b = b + random()
 ```
 **ответ:O(2n)**   

## 19. Найти сложность приведенной ниже программы: 
 
```py
a = 0;
for i in range(N):
    for j in reversed(range(i,N)):
        a = a + i + j
 ```
 **ответ:O(n^2)**   

## 20. Найти сложность приведенной ниже программы: 
 
```py
k = 0;
for i in range(n//2,n): # O(n)
    for j in range(2,n,pow(2,j)): # O(log2(n))
        k = k + n / 2
 ```
  **ответ:O(n*log2(n))**   

## 21. Найти сложность приведенной ниже программы: 
```py
a = 0
i = N
while (i > 0):
    a += i
    i //= 2
``` 
  **ответ:O(log2(n))**   

## 22. Найти сложность приведенной ниже программы: 

```py
for i in range(n):
    i = i * k
```
  **ответ:O(log k (n))**   

## 23. Найти сложность приведенной ниже программы: 

```py
value = 0
for i in range(n): # O(n)
    for j in range(i): # O(n)
        value = value + 1
```
  **ответ:O(n^2)**   