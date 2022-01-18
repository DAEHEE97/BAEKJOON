## 10952

- map(int,sys.stdin.readline().split()

- while(1)
- while(False) > run X



```python
import sys

while(1):
    n1,n2 = map(int,sys.stdin.readline().split())
    if (n1 == 0 and n2 == 0):
        break
    print(n1+n2)
```

## 10951

- try except



```python
import sys

while(1):
    try:
        n1,n2 = map(int,sys.stdin.readline().split())
        print(n1+n2)
    except:
        break

```

## 1110

- divmod


```python
N   = int(input())
FN  = N
cnt = 0


while(1):
    
    
    n1,n2 = divmod(N,10)
    n12   = n1 + n2
    
    t1,t2 = divmod(n12,10)
    newN  = n2 *10 + t2
    
    cnt+=1
    
    if newN == FN:
        break
    
    N = newN
    

print(cnt)
```


```python
N   = int(input())
FN  = N
cnt = 0

while(1) :

    m,d = divmod(N,10)
    s = m + d

    s%=10
    
    newN = d*10 + s

    cnt+=1
    
    if(newN == FN): break

    N = newN


print(cnt)

```
