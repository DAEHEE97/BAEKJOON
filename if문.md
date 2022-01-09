## 1330


```python
A,B = map(int,input().split())
if A > B :
    print(">")
elif A < B :
    print("<")
else : print("==")
```

    3 6
    <


## 9498


```python
score = int(input())
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else: print("F")
    
```

    88
    B


## 2753


```python
year = int(input())

if year % 4 == 0 and year % 100 !=0 or year % 400 ==0:
    print(1)
else : print(0)

```

    2022
    0


## 14681


```python
x = int(input())
y = int(input())


if x > 0 and y > 0:
    print(1)
elif x > 0 and y < 0:
    print(4)
elif x < 0 and y > 0:
    print(2)
elif x < 0 and y < 0:
    print(3)

```

    8
    3
    1


## 2884


```python
hour = 24
minute = 60

alarm = 45

H, M = map(int,input().split())

M -= alarm 

if (M < 0):
    M += minute
    H -= 1
    
    if (H < 0):
        H += hour
        

print(H,M)

```

    10 30
    9 45

