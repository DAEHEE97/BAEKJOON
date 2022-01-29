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

- 입력으로 주어진 숫자(number) N개(idx)의 합을 출력



```python
N = int(input())

number = input()


sum = 0

# idx i

for i in range(N):
    sum += int(number[i])

print(sum)
```

    5
    543217
    15


# 10809

- 각각의 알파벳에 대해서, a가 처음 등장하는 위치, b가 처음 등장하는 위치, ... z가 처음 등장하는 위치를 공백으로 구분해서 출력
- 만약, 어떤 알파벳이 단어에 포함되어 있지 않다면 -1을 출력


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

# test case
T = int(input())
lst = []


for i in range(T):    
    #lst.append(sys.stdin.readline().strip())
    lst.append(input())

    
for i in range(T):
    
    # 반복횟수와 문자열 구분
    n,S = lst[i].split() 
    n = int(n)
    # idx i
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

- 첫째 줄에 이 단어에서 가장 많이 사용된 알파벳을 대문자로 출력한다. 
- 단, 가장 많이 사용된 알파벳이 여러 개 존재하는 경우에는 ?를 출력한다.


```python

word = input()

word = word.upper()


# zero list
lst = [0 for i in range(91-65)]

# count 
for i in range(len(word)):
    
    for j in range(90+1-65): # 65 ~ 90
        J = j+65
        
        if word[i] == chr(J):
            lst[j] +=1

# count list            
print(lst)

# 중복 제거
idx_list = [i for i, value in enumerate(lst) if value == max(lst)]

if len(idx_list) >= 2:
    print("?")
else :
    idx = idx_list[0]    
    print(chr(idx+65))
    
    
    
```

    zZa
    [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 2]
    Z


## filter

- filter를 이용하여 test_list에서 3의 위치를 모두 반환하는 코드
- 더불어 filter는 lambda와 같이 사용하면 유용


```python
test_list = [1, 3, 4, 3, 6, 7]

result_list = list(filter(lambda x: test_list[x] == 3, range(len(test_list))))
print(result_list)
```

    [1, 3]


## enumerate

- enumerate는 value와 index를 같이 반환하는 파이썬 내장 함수


```python
test_list = [1, 3, 4, 3, 6, 7]
result_list= [i for i, value in enumerate(test_list) if value == 3]
print(result_list)

```

    [1, 3]


## for i


```python
test_list = [1, 3, 4, 3, 6, 7]
result_list = [ i for i in range(len(test_list)) if test_list[i] == 3 ]
print(result_list)
```

    [1, 3]



```python
test_list = [1, 3, 4, 3, 6, 7]

result_list = []

# i = idx
for i in range(len(test_list)):
    if test_list[i] == 3:
        result_list.append(i)
        
print(result_list)
```

    [1, 3]


# 1152


```python
lst = input().split()
print(len(lst))
```

    hello world
    2


# 2908


```python
A,B = input().split()

a0=int(A[2])
a1=int(A[1])
a2=int(A[0])

b0=int(B[2])
b1=int(B[1])
b2=int(B[0])

A = 100*a0+10*a1+a2
B = 100*b0+10*b1+b2


if A > B:
    print(A)
else : print(B)

```

    734 893
    437



```python
A,B = input().split()

a = [ A[i] for i in range(len(A)) ]
b = [ B[i] for i in range(len(B)) ]

print(a,b)


```

    734 893
    ['7', '3', '4'] ['8', '9', '3']


## swap


```python
a = 1
b = 2
c = 3

a,b,c = c,a,b
print(a,b,c)
```

    3 1 2


# 5622



```python
string = input()

alphabet_lst = "ABC DEF GHI JKL MNO PQRS TUV WXYZ".split()

d = {}

# dictionary
for i in range(len(alphabet_lst)):

    for j in range(len(alphabet_lst[i])):
        
        word = alphabet_lst[i]
        d[word[j]] = i+3
        

print(d)
sum = 0

for j in range(len(string)):
    
    for i in range(65,90+1):
        
        if chr(i) in string[j] :
            #print(chr(i))
            sum += d[chr(i)]

print(sum)
```

    WA
    {'A': 3, 'B': 3, 'C': 3, 'D': 4, 'E': 4, 'F': 4, 'G': 5, 'H': 5, 'I': 5, 'J': 6, 'K': 6, 'L': 6, 'M': 7, 'N': 7, 'O': 7, 'P': 8, 'Q': 8, 'R': 8, 'S': 8, 'T': 9, 'U': 9, 'V': 9, 'W': 10, 'X': 10, 'Y': 10, 'Z': 10}
    13


# 2941

- for i in lst: replace()
- 특정문자 index()로 문제해결시 중복 문제가 발생하여 replcae


```python
c_lst = ['c=', 'c-', 'dz=', 'd-', 'lj', 'nj', 's=', 'z=']

word = input()

for i in c_lst :
    word = word.replace(i, '*')

print(len(word))


```

    c=c=kk
    4


# 1316



```python
import sys


N = int(input())

word_lst = [input() for i in range(N)]
# word_lst = [sys.stdin.readline() for i in range(N)]

for word in word_lst:
    
    for i in range(len(word)-1):
        
        if word.index(word[i]) > word.index(word[i+1]):
            N -= 1
            break
        else:
            continue
            
print(N)
        
    
```

    3
    akaka
    aaabb
    asd
    2

