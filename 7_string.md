# 11654


```python
# ord()
# str to ASCII

N = input()
print(ord(N))
```

    A
    65


# 11720


```python
N = int(input())

M = input()


sum = 0
for i in range(N):
    sum += int(M[i])

print(sum)
```

    5
    54321
    15


# 10809


```python
# chr()
# ASCII to str

S = input()

for i in range(97,122+1):
    try:
        print(S.index(chr(i)),end=" ")
    except:
        print(-1,end=" ")
```

    baekjoon
    1 0 -1 -1 2 -1 -1 -1 -1 4 3 -1 -1 7 5 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 

# 2675


```python
import sys

T = int(input())
lst = []
for i in range(T):
    

    #lst.append(sys.stdin.readline().strip())
    lst.append(input())

for i in range(T):
    
    n,S = lst[i].split()
    n = int(n)
    
    for i in range(len(S)):
        print(S[i]*n,end="")

    print()




```

    2
    3 ABC
    5 /HTP
    AAABBBCCC
    /////HHHHHTTTTTPPPPP


# 1157


```python

word = input()

word = word.upper()


# list
lst = [0 for i in range(91-65)]

# count 
for i in range(len(word)):
    
    for j in range(90+1-65): # 65 ~ 90
        J = j+65
        
        if word[i] == chr(J):
            lst[j] +=1
    
    
# max idx
idx_list = [i for i, value in enumerate(lst) if value == max(lst)]

if len(idx_list) >= 2:
    print("?")
else :
    idx = idx_list[0]    
    print(chr(idx+65))
    
    
    
```

    hello
    L


## filter

- filter를 이용하여 test_list에서 3의 위치를 모두 반환하는 코드이다. 
- filter를 사용하고 list로 감싸줘야 우리가 원하는 형태를 얻을 수 있다. 
- 더불어 filter는 lambda와 같이 사용하면 유용하니 꼭 기억하자.


```python
test_list = [1, 3, 4, 3, 6, 7]

res_list = list(filter(lambda x: test_list[x] == 3, range(len(test_list))))
print(res_list)
```

    [1, 3]


## enumerate

- enumerate는 value와 index를 같이 반환하는 파이썬 내장 함수이다. 
- filter를 사용 했을 때와 같은 결과를 얻을 수 있다. 
- 개인적으로 enumerate가 직관적이고 사용하기 간편하다.



```python
test_list = [1, 3, 4, 3, 7, 7]

res_list = [i for i, value in enumerate(test_list) if value == max(test_list)]
print(res_list)

```

    [4, 5]

