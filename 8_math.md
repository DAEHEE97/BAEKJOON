# 1712 BREAK-EVEN POINT


- 최초로 이익이 발생하는 판매량을 출력 
- 손익분기점이 존재하지 않으면 -1을 출력



- A+(B*n) < C*n // 시간복잡도 
- A <(C-B)*n 판매이익 n 제거 +1
- B>=C 생산비용이 판매비용보다 같거나 크면 이익이 발생하지 않습니다.



```python
A,B,C = map(int,input().split())

if B>=C:
    print(-1)
else :
    print(A//(C-B)+1)
```

    1000 70 170
    11



```python
# time over
A,B,C = map(int,input().split())

n=0

if (B>=C):
    n = -1  


while(A+(B*n) >= C*n):
    
    if (B>=C):
        break
        
    else:
        n+=1

print(n)
    
```

    1000 70 170
    11


# 2292


n>1인 이유는 입력이 N = 1인 경우, 그룹 마지막 숫자일 경우 제외

- 1     > 1 (1)
- 2  7  > 2 (6)
- 8  19 > 3 (12)
- 20 37 > 4 (18)



```python
N = int(input())

cnt = 1
while N > 1:
    N = N - (6*cnt)
    cnt += 1
print(cnt)
```

    13
    3


# 1193

- N
- if 홀짝 
- i/d d/i 반복

1/1 


2,3 i/d (N=2)

- 1/2 2/1 

4,5,6  d/i (N=3)

- 3/1 2/2 1/3 

7,8,9,10 i/d (N=4)

- 1/4 2/3 3/2 4/1 

11 12 13 14 15 (N=5)

- 5/1 4/2 3/3 2/4 1/5


1 5 13 


```python
N = int(input())


count = 1

1 > 1
2,3 > 2
4,5,6 > 3
7,8,9,10 > 4


10 - 1 + 2+ 3+ 4 = 
```

# 2869

A - B 가아니라 
순서대로



```python
A,B,V = map(int,input().split())
```

    5 1 6



```python
# time over
cnt = 0
day = 1

while(1):
    
    cnt = cnt + A
    
    if (cnt >= V):
        
        break
    
    cnt = cnt - B
    day += 1

print(day)
        

```

    2



```python
import math


A,B,V = map(int,input().split())
tmp = A - B 


m,d = divmod(V , tmp)


if d == 0:
    print(m-1)
else :
    print(math.ceil(V / (A - B) ))
    
```

    100 99 1000000000
    999999999


# 2775

# 2839

# 10757

# 1011

# 1978

# 2581

# 11653

# 1929

# 4948

# 9020

# 1085

# 3009

# 4153

# 3053

# 1002
