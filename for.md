## 2739

- print option
- range 역순


```python
# print end

print('variable1','variable2',end= ' ')
```

    variable1 variable2 


```python
# print sep

print('Hello', 'Python', sep='')    # 문자열 sep에 빈 문자열을 지정
print('Hello', 'Python', sep=' ')   # 문자열 sep에 공백 문자열을 지정
print(1920, 1080, sep='x')          # 변수 sep에 x를 지정
```

    HelloPython
    Hello Python
    1920x1080



```python
# print format

print('{0} and {1}'.format('spam', 'eggs'))

print('{1} and {0}'.format('spam', 'eggs'))
 
num1=1
num2=2

print('{0} {1}'.format(num1,num2))
```

    spam and eggs
    eggs and spam
    1 2



```python
# 서식문자

n=1024
print('n equals %d.'%n)
```

    n equals 1024.



```python
N = int(input())

for i in range(1,10):
    print('{0} * {1} = {2}'.format(N,i,N*i))
    
    
print("-"*100)


for i in range(1,10):
    print( N,"*",i,"=", N*i )
    
```

    9
    9 * 1 = 9
    9 * 2 = 18
    9 * 3 = 27
    9 * 4 = 36
    9 * 5 = 45
    9 * 6 = 54
    9 * 7 = 63
    9 * 8 = 72
    9 * 9 = 81
    ----------------------------------------------------------------------------------------------------
    9 * 1 = 9
    9 * 2 = 18
    9 * 3 = 27
    9 * 4 = 36
    9 * 5 = 45
    9 * 6 = 54
    9 * 7 = 63
    9 * 8 = 72
    9 * 9 = 81


## 10950


```python
T = int(input())

for i in range(T):
    A,B = map(int,input().split())
    print(A+B)
```

    3
    1 1
    2
    10 10
    20
    20 3
    23


## 8393


```python
sum = 0
n = int(input())
for i in range(n+1):
    sum+=i

print(sum)
```

    10
    55


## 15552

### sys.stdin.readline()

- sys : 파이썬 인터프리터가 제공하는 변수와 함수를 직접 제어할 수 있게 해주는 모듈

- input()대신 sys.stdin.readline()을 사용하는 이유

- 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶을 경우 .rstrip()을 추가로 해 주는 것이 좋다.


한 두줄 입력받는 문제들과 다르게, 반복문으로 여러줄을 입력 받아야 할 때는 input()으로 입력 받는다면 시간초과가 발생할 수 있습니다. 




```python
# 1. 문자열을  받을 때

#sys.stdin.readline()은 return값이 문자열이므로 그냥 문장을 하나 받을 때 사용가능하다.
#sys.stdin.readline()을 출력하면 문자열에 개행문자(\n)가 기본으로 추가됨도 확인 가능하다.



import sys
sentence = sys.stdin.readline()


        
```


```python
# 2. 한 개의 정수를 입력받을 때

# sys.stdin.readline()의 return 값은 문자열(string)이기 때문에 정수로 입력받으려면 형변환을 해줘야한다.
# sys.stdin.readline()으로 받은 문자열은 개행문자(\n)을 포함한다. 
# 문자열을 int()로 형변환을 해주면 개행문자는 사라지고 정수형태만 남는다.


import sys
number = int(sys.stdin.readline())



```


```python
# 3. 여러 개의 정수를 입력받을 때

# 여러개의 정수를 입력받으려면 map 함수를 사용하면 된다.
# map함수는 요소를 지정된 함수로 처리해주는 함수다.

import sys
a,b = map(int,sys.stdin.readline().split())


```


```python
# 4. 문자열 N줄을 입력받아 리스트에 저장할 때

import sys 
n = int(sys.stdin.readline()) 
data = [sys.stdin.readline().strip() for i in range(n)]


```


```python
import sys

T = int(input()) 
for i in range(T):
        A,B = map(int, sys.stdin.readline().split())
        print(A+B)
```

## 2741


```python
import sys

n = int(input())
# n = int(sys.stdin.readline())

for i in range(1,n+1):
    print(i)


```

## 2742


```python
# range?
# range(start, stop[, step])
```


```python
# n = int(sys.stdin.readline())

n = int(input())

for i in range(n,0,-1):  
    print(i)

# -1 : 10 9 8 7 6 5 4 3 2 1 > 0 stop 
# -2 : 10 8 6 4 2 > 0 stop
# -3 : 10 7 4 1 > 0 stop
```

## 11021


```python
import sys

T = int(input()) 

for i in range(1,T+1):
        A,B = map(int, sys.stdin.readline().split())
        print('Case #{0}: {1}'.format(i,A+B))
```


```python
T = int(input()) 

for i in range(1,T+1):
        A,B = map(int, input().split())
        print('Case #{0}: {1}'.format(i,A+B))
```

## 11022


```python
import sys

T = int(input()) 
for i in range(1,T+1):
        A,B = map(int, sys.stdin.readline().split())
        print('Case #{0}: {1} + {2} = {3}'.format(i,A,B,A+B))
```


```python
T = int(input())

for i in range(1,T+1):
        A,B = map(int, input().split())
        print('Case #{0}: {1} + {2} = {3}'.format(i,A,B,A+B))
```

## 2438


```python
N = int(input())

for i in range(1,N+1):
    print("*"*i)


```

## 2439


```python
N = int(input())

for i in range(N,0,-1):
    star = N - i + 1
    #print(" "*(i-1),"*"*star)
    
    
    print('{0}{1}'.format(" "*(i-1),"*"*star))
```


```python
N = int(input())

for i in range(N,0,-1):
    star = N - i + 1
    print(" "*(i-1),"*"*star,sep='')
```


```python

print("hello","world")
print("hello","world",sep='')
```

## 10871


```python
N,X = map(int,input().split())

s = [int(input().strip()) for i in range(N)]

for i in range(len(s)):
    if s[i] < X:
        print(s[i])

```


```python
import sys

N,X = map(int,input().split())

s = [int(sys.stdin.readline.strip()) for i in range(N)]

for i in range(len(s)):
    if s[i] < X:
        print(s[i])


```
