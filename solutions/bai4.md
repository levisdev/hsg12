## Viết công thức truy hồi của các hàm sau và lập trình để thực hiện các hàm này bằng đệ quy.

1. Hàm factorial(n) = n! (tính n giai thừa).

```python
def factorial(n):
    if n == 1:
        return n
    return factorial(n - 1) * n

print(factorial(5))
```

2. Hàm exp(a,n) = a^n (lũy thừa).

```python
def exp(a, n):
    if a == 0:
        return 0
    if n == 0:
        return 1
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

## Dãy số Fibonacci

Viết hàm đệ quy tính số Fibonacci thứ n.

```python
def Fibonacci(n):
    if (n == 0 or n == 1):
        return n
    return Fibonacci(n-1) + Fibonacci(n-2)

print(Fibonacci(5))
```

## Dãy số Lucas.

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

## Dãy số Pell.

Viết hàm đệ quy tính số Pell thứ n.

```python
def Pell(n):
    if (n == 0 or n == 1):
        return n
    return 2 * Pell(n-1) + Pell(n-2)

print(Pell(5))
```

## Dãy số Pandovan.

Viết hàm đệ quy tính số Pandovan thứ n.

```python
def Pandovan(n):
    if (n == 0 or n == 1 or n == 2):
        return 1
    return Pandovan(n-2) + Pandovan(n-3)

print(Pandovan(5))
```

## Viết hàm tính tổng sau bằng kỹ thuật đệ quy.

$$ S = \frac {1} {0!} + \frac {1} {1!} + \frac {1} {2!} + ... + \frac {1} {n!} $$

```python
n = 5

def fact(n):
    if n <= 1:
        return 1
    return fact(n-1) * n

res = 0
for i in range(n+1):
    res += 1 / fact(i)

print(res)
```

## Viết hàm tính tổng sau đây bằng kỹ thuật đệ quy.

$$ S(x) = \frac {x^0} {0!} + \frac {x^1} {1!} + \frac {x^2} {2!} + ... + \frac {x^n} {n!}$$
