## Viết hàm bubble sort dùng đệ quy

```python
a = [0,5,1,7,1,1,2,8,7]

def bubbleSort(arr, n):
    k = 0
    for i in range(n-1):
        if a[i] > a[i+1]:
            a[i], a[i+1] = a[i+1], a[i]
            k += 1
    if k == 0:
        return arr
    return bubbleSort(arr, n-1)

print(bubbleSort(a, len(a)))
```

## Sô tự nhiên -> nhị phân

In dạng chuỗi

```python
def binary(n):
    if n > 1:
        binary(n//2)
    print(n%2, end="")

binary(10)
```

In dạng bit

```python
res = []

def binary(n):
    global res
    if n > 1:
        binary(n // 2)
    res += [n%2]
    return res

print(binary(2))
```

## Nhị phân -> thập phân

```python
s = "1111"
l = len(s)
res = 0

def decimal(s):
    if s == "":
        return 0
    global res
    p = 1
    k = l - len(s)
    for _ in range(k):
        p *= 2
    res += int(s[len(s)-1]) * p
    decimal(s[:len(s)-1])
    return res

print(decimal(s))
```

## thập phân -> thập lục phân

```python
chars = {
    0: '0', 1: '1', 2: '2', 3: '3', 4: '4',
    5: '5', 6: '6', 7: '7', 8: '8', 9: '9',
    10: 'A', 11: 'B', 12: 'C', 13: 'D', 14: 'E', 15: 'F'
}

def hex(n):
    if n > 1:
        hex(n//16)
    print(chars[n%16], end="")

hex(910)
```

## thập lục phân -> thập phân

```python
s = "ABC"
l = len(s)
res = 0

chars = {
    '0': 0, '1': 1, '2': 2, '3': 3, '4': 4,
    '5': 5, '6': 6, '7': 7, '8': 8, '9': 9,
    'A': 10, 'B': 11, 'C': 12, 'D': 13, 'E': 14, 'F': 15
}

def decimal(s):
    if s == "":
        return 0
    global res
    p = 1
    k = l - len(s)
    for _ in range(k):
        p *= 16
    res += chars[s[len(s)-1]] * p
    decimal(s[:len(s)-1])
    return res

print(decimal(s))
```
