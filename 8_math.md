# 1712 BREAK-EVEN POINT



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


n>1인 이유는 입=력이 N = 1인 경우, 그룹 마지막 숫자일 경우 제외


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


# 2869

A - B 가아니라 
순서대로



```python
A,B,V = map(int,input().split())
```

    5 1 6

