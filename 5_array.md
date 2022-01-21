# 10818

- list 입력


```python
import sys 


N = int(input()) 
# N = int(sys.stdin.readline()) 

lst = list(map(int, input().split()))
# lst = list(map(int,sys.stdin.readline().split()))

print(min(lst),max(lst))


```

## 입력

__space 기준 int 입력 > list로 변경__
- lst = list(map(int,sys.stdin.readline().split()))
- lst = [map(int,sys.stdin.readline().split())]


__Enter \n 기준 int 입력 > list로 변경__
- lst = [int(sys.stdin.readline().strip()) for i in range(N)]
- lst = [int(input()) for i in range(N)]

__Enter \n 기준 문자열 입력 > 문자열 list로 변경__
- lst = [sys.stdin.readline().strip() for i in range(N)]
- lst = [input() for i in range(N)]




```python
import sys 

#N = int(sys.stdin.readline()) 
N = int(input())

# space 구분 /  N값에 상관없이 입력받은 문자 int로 변환후 list로 저장


lst = list(map(int,sys.stdin.readline().split()))
lst = list(map(int, input().split()))


# \n로 구분 / 입력받은 N값 만큼 

lst = [int(sys.stdin.readline().strip()) for i in range(N)]
lst = [int(input()) for i in range(N)]


# lst.append()
lst = list()
for i in range(N):
    lst.append(int(input()))
    
```

# 2562

- int(sys.stdin.readline().strip())



```python
import sys

# lst = [int(sys.stdin.readline().strip()) for i in range(9)]
lst = [int(input()) for i in range(9)]


print(max(lst))              # 최대 값
print(lst.index(max(lst))+1) # 몇 번째 수 인지

```

# 2577

- import re



```python
import sys
import re

# lst = [int(sys.stdin.readline().strip()) for i in range(3)
lst = [int(input()) for i in range(3)]

N = lst[0]*lst[1]*lst[2]

string = str(N)

# 문자열 리스트
numbers = re.findall(r'\d', string)


for i in range(10):
    
    cnt = 0
    
    for n in numbers:
        if i == int(n) :
            cnt+=1
            
    print(cnt)
```

## re


```python
import re

tmp_string = '11a22bb333'

# 숫자 연속으로 
numbers = re.findall("\d+", tmp_string)
print(numbers)


# 숫자 하나씩
numbers = re.findall("\d", tmp_string)
print(numbers)

        
```

# 3052

- list to set


```python
import sys


# input_lst = [int(sys.stdin.readline().strip()) for i in range(10)]
input_lst  = [int(input()) for i in range(10)]

lst = []

for i in input_lst:
    lst.append(i%42)

list_to_set = set(lst) 

print(len(list_to_set))
```

## numpy


```python
import numpy as np

input_lst  = [int(input()) for i in range(10)]
lst = []

for i in input_lst:
    lst.append(i%42)
    
lst = np.unique(lst)

print(len(lst))
```

# 1546


```python
import sys

N = int(input())

#lst = list(map(int,sys.stdin.readline().split()))
lst = list(map(int,input().split()))


M = max(lst)
new_lst = list()

for i in lst:
    new_lst.append((i/M) * 100)
    

sum = 0
for i in new_lst:
    sum+=i

print(sum/N)

```

# 8958

- variable


```python
import sys 

N = int(input())


for i in range(N):
    
    lst = [input()]
    #lst = [sys.stdin.readline().strip()]

    cnt = 0
    score = 0
    
    for i in lst: # i = OXOOXOOX

        for j in range(len(i)):

            if i[j] == "O":
                cnt += 1
                score += cnt
            else:
                cnt = 0
                
    
    
    print(score)

            

            
            
```

# 4344

- print('{:.3f}%'.format())


```python
N = int(input())


for i in range(N):
    
    #lst = list(map(int,input().split()))
    lst = list(map(int,sys.stdin.readline().split()))
    
    s   = 0
    
    for i in range(1,len(lst)):
        
        s+=lst[i]
        mean = s / lst[0]
    
    c   = 0

    for i in range(1,len(lst)):
        if lst[i] > mean:
            c+=1
    
    
        
    print('{:.3f}%'.format(c/lst[0]*100))
    
```
