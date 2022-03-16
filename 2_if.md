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

- 윤년이면 1, 아니면 0을 출력
- 윤년은 연도가 4의 배수이면서, 100의 배수가 아닐 때 또는 400의 배수일 때이다.


```python
year = int(input())

if year % 4 == 0 and year % 100 != 0 or year % 400 == 0:
    print(1)
else : print(0)

```

    2000
    1


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

- -분, -시 처리


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


## 2525 - 1

- 초과 minute 시간 처리


```python
hour, minute = map(int,input().split())
cooking_minute = int(input())

cooked_minute = minute + cooking_minute

# + 한 minute 를 60분을 기준으로 hour, minute 분리
# 73 > (1,13)

Ch,Cm = divmod(cooked_minute,60)


# + 한 hour 가 24:00 을 넘을 경우 처리
if (hour+Ch >= 24):
    
    tmp,cooked_hour = divmod(hour+Ch,24)
    print(cooked_hour,Cm)
    
else:
    print(hour+Ch,Cm)
    
    
```

    23 48
    25
    0 13


## 2525 - 2 


```python
H, M = map(int,input().split())
C = int(input())

H = H + (C // 60) # 60분 초과 계산 후 hour
M = M + (C % 60)  # 60분 초과 계산 후 minute 


# + 한 minute 가 60 초과시 minute > hour 승격, 나머지 hour 계산
if M >= 60 : 
    H+=1
    M-=60

# 24:00     
if H >= 24 :
    H-=24

print(H,M)
```

    23 48
    25
    0 13


## 2480

- 입력, case 분리


```python
n1,n2,n3 = map(int,input().split())


if n1 == n2 == n3:
    print(10000+1000*n1)

elif(n1 == n2 != n3):
    print(1000+100*n1)

elif(n1 == n3 != n2):
    print(1000+100*n1)
    
elif(n2 == n3 != n1):
    print(1000+100*n2)
else:
    print(max(n1,n2,n3)*100)
        
```

    6 2 5

