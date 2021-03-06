# etc

## `print`
- default \n


```python
print('variable1')
print('variable2')
```

    variable1
    variable2


### `print end`


```python
print('variable1',end= '')
print('variable2')
```

    variable1variable2


### `print sep =`

- print 변수 2개 이상


```python
print('Hello', 'Python', sep='')    # 문자열 sep에 빈 문자열을 지정
print('Hello', 'Python', sep=' ')   # 문자열 sep에 공백 문자열을 지정
print(1920, 1080, sep='x')          # 변수 sep에 x를 지정

print()
print('variable1','variable2',sep= '\n')


```

    HelloPython
    Hello Python
    1920x1080
    
    variable1
    variable2


### `print ( '{0} {1} '.format( , ) )`


```python
print('{0} and {1}'.format('spam', 'eggs'))

print('{1} and {0}'.format('spam', 'eggs'))
 
num1=1
num2=2

print('{0} {1}'.format(num1,num2))
```

    spam and eggs
    eggs and spam
    1 2


### `print %`


```python
# 서식문자

n=1024
print('n equals %d.'%n)
```

    n equals 1024.


# for

## 2739


```python
N = int(input())

for i in range(1,10):
    print('{0} * {1} = {2}'.format(N,i,N*i))
    
    
print()


for i in range(1,10):
    print( N,"*",i,"=", N*i )
    
```

    10
    10 * 1 = 10
    10 * 2 = 20
    10 * 3 = 30
    10 * 4 = 40
    10 * 5 = 50
    10 * 6 = 60
    10 * 7 = 70
    10 * 8 = 80
    10 * 9 = 90
    
    10 * 1 = 10
    10 * 2 = 20
    10 * 3 = 30
    10 * 4 = 40
    10 * 5 = 50
    10 * 6 = 60
    10 * 7 = 70
    10 * 8 = 80
    10 * 9 = 90


## 10950

- n 횟수
- `for i in range(n)` 


```python
n = int(input())

for i in range(n):
    A,B = map(int,input().split())
    print(A+B)
```

    3
    1 4
    5
    2 6
    8
    3 10
    13


## 8393

- 값 value
- `for i in range(0,n+1)` 


```python
sum = 0

v = int(input())

for i in range(v+1):
    sum+=i

print(sum)
```

    10
    55


## sys
- sys : 파이썬 인터프리터가 제공하는 변수와 함수를 직접 제어할 수 있게 해주는 모듈


### sys.stdin.readline( )



- `input()`대신 `sys.stdin.readline()`을 사용하는 이유
- __한 두줄 입력받는 문제들과 다르게, 반복문으로 여러줄을 입력 받아야 할 때는 input()으로 입력 받는다면 시간초과가 발생할 수 있습니다.__ 

- `sys.stdin.readline()`의 return 값은 문자열(string)이기 때문에, 정수로 입력받으려면 int()형변환을 해줘야한다.


- int() 형 변환시 \n 자동 제거되므로, 여러개의 정수를 입력받을시 `map` 함수를 사용 `map(int,sns.stdin.readline().strip())`



### strip()

- `strip()` : 양쪽 문자열에 공백이나 인자가된 문자열의 모든 조합을 제거
- `rstrip()` : 문자열에 오른쪽 공백이나 인자가된 문자열의 모든 조합을 제거
- `lstrip()` : 문자열에 왼쪽 공백이나 인자가된 문자열의 모든 조합을 제거

- `sys.stdin.readline()`으로 입력시 '\n' 자동 추가 되므로 `sys.stdin.readline().rstirp()` 하여 \n 제거 




## 15552




```python
# 1. 문자열을  받을 때

import sys

sentence = sys.stdin.readline().rstrip()

print(sentence)
    
```


```python
# 2. 한 개의 정수를 입력받을 때

# sys.stdin.readline()으로 받은 문자열은 개행문자(\n)을 포함한다. 
# 문자열을 int()로 형변환을 해주면 개행문자는 사라지고 정수형태만 남는다.


import sys
number = int(sys.stdin.readline())
print(number)
```


```python
# 3. 여러 개의 정수를 입력받을 때

import sys
n1,n2 = map(int,sys.stdin.readline().split())
print(n1,n2)

```


```python
# 4. 문자열 N 줄을 입력받아 lst 에 저장할 때

import sys 
n = int(sys.stdin.readline()) 
data_lst = [sys.stdin.readline().strip() for i in range(n)]


```

## 2741


```python
import sys

v = int(input())
# n = int(sys.stdin.readline())

for i in range(1,v+1):
    print(i)

```

    10
    1
    2
    3
    4
    5
    6
    7
    8
    9
    10


## 2742


- `range(start, stop[, step])`


```python
# n = int(sys.stdin.readline())

n = int(input())

for i in range(n,0,-1):  
    print(i)

print()
    
for i in range(n,0,-2):  
    print(i)
    
print()
   
for i in range(n,0,-3):  
    print(i)
    
# -1 : 10 9 8 7 6 5 4 3 2 1 > 0 stop 
# -2 : 10 8 6 4 2 > 0 stop
# -3 : 10 7 4 1 > 0 stop
```

    10
    10
    9
    8
    7
    6
    5
    4
    3
    2
    1
    
    10
    8
    6
    4
    2
    
    10
    7
    4
    1


## 11021


```python
T = int(input()) 

for i in range(1,T+1):
    A,B = map(int, input().split())
    print('Case #{0}: {1}'.format(i,A+B))
```

    3
     1 2
    Case #1: 3
    3 6
    Case #2: 9
    2 10
    Case #3: 12



```python
import sys

T = int(input()) 

for i in range(1,T+1):
    A,B = map(int, sys.stdin.readline().split())
    print('Case #{0}: {1}'.format(i,A+B))
```

## 11022


```python
T = int(input())

for i in range(1,T+1):
    A,B = map(int, input().split())
    print('Case #{0}: {1} + {2} = {3}'.format(i,A,B,A+B))
```


```python
import sys

T = int(input())

for i in range(1,T+1):
    A,B = map(int, sys.stdin.readline().split())
    print('Case #{0}: {1} + {2} = {3}'.format(i,A,B,A+B))
```

## 2438


```python
N = int(input())

for i in range(1,N+1):
    print("*"*i)
```

    3
    *
    **
    ***


## 2439

- 공백, 별의 개수


```python
N = int(input())

for i in range(N,0,-1):
    
    star = N - (i - 1)
    #print(" "*(i-1),"*"*star)
    
    
    print('{0}{1}'.format(" "*(i-1),"*"*star))
```

    4
       *
      **
     ***
    ****



```python
# print (,) = ' ' 이므로 , sep='' 

N = int(input())

for i in range(N,0,-1):
    star = N - i + 1
    print(" "*(i-1),"*"*star,sep='')
```

    4
       *
      **
     ***
    ****


## 10871


첫째 줄에 N과 X가 주어진다. (1 ≤ N, X ≤ 10,000)

둘째 줄에 수열 A를 이루는 정수 N개가 주어진다. 주어지는 정수는 모두 1보다 크거나 같고, 10,000보다 작거나 같은 정수이다.

X보다 작은 수를 입력받은 순서대로 공백으로 구분해 출력한다. X보다 작은 수는 적어도 하나 존재한다.


- `list(map(int,input().split()))`
- `print end=" "`


- `for i in lst`              / i는 리스트 내부 값 value v0,v1,v2 ~
- `for i in range(len(lst))`  / i는 인덱스 index 0,1,2 ~


```python
N,X = map(int,input().split())

lst = list(map(int,input().split()))

for i in lst:
    if i < X:
        print(i, end=" ")

```

    10 5
    1 10 4 9 2 3 8 5 7 6
    1 4 2 3 


```python
N,X = map(int,input().split())

lst = list(map(int,input().split()))

for i in range(len(lst)):
    if lst[i] < X:
        print(lst[i], end=" ")


```

    10 5
    1 10 4 9 2 3 8 5 7 6
    1 4 2 3 
