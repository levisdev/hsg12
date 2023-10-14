#### Viết công thức truy hồi của các hàm sau và lập trình để thực hiện các hàm này bằng đệ quy.

1. Hàm factorial(n) = n! (tính n giai thừa).

```python
def factorial(n):
    if n == 1:
        return n
    return factorial(n - 1) * n

print(factorial(5))
```

2. Hàm exp(a,n) = an (lũy thừa).

```python
def exp(a, n):
    if n == 1:
        return a
    return exp(a, n-1) * a

print(exp(2, 3))
```

3. Hàm S(n) = 1 + 2 + ... + n

```python
def S(n):
    if n == 1:
        return 1
    return S(n-1) + n

print(S(100))
```

4. Hàm Sq(n) = 1^2 + 2^2 + ... + n^2

```python
def Sq(n):
    if n == 1:
        return 1
    return Sq(n-1) + n * n

print(Sq(10))
```

5. Hàm Seven(n) = tổng các số tự nhiên chẵn không vượt quá n.

```python
def Seven(n):
    if n % 2 == 1:
        n -= 1
    if n == 2:
        return 2
    return Seven(n-2) + n

print(Seven(20))
```

6. Hàm Sodd(n) = tổng các số tự nhiên lẻ không vượt quá n.

```python
def Sodd(n):
    if n % 2 == 0:
        n -= 1
    if n == 1:
        return 1
    return Sodd(n-2) + n

print(Sodd(20))
```

#### Dãy số Fibonacci

Viết hàm đệ quy tính số Fibonacci thứ n.

```python
def Fibonacci(n):
    if (n == 0 or n == 1):
        return n
    return Fibonacci(n-1) + Fibonacci(n-2)

print(Fibonacci(5))
```

#### Dãy số Lucas.

Viết hàm đệ quy tính số Lucas thứ n.

```python
def Lucas(n):
    if n == 0:
        return 2
    if n == 1:
        return 1
    return Lucas(n-1) + Lucas(n-2)

print(Lucas(5))
```

#### Dãy số Pell.

Viết hàm đệ quy tính số Pell thứ n.

```python
def Pell(n):
    if (n == 0 or n == 1):
        return n
    return 2 * Pell(n-1) + Pell(n-2)

print(Pell(5))
```
