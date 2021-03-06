# 201206 과제

## 정수->이진수 변환

1. 변환할 10진수 정수를 2로 나누고 나머지(0 혹은 1)을 적는다.
2. 나눌 수 없을때까지 나눈다.
3. 적어둔 나머지를 반대로 적는다.


```
156%2 = 0
78%2 = 0
39%2 = 1
19%2 = 1
9%2 = 1
4%2 = 0
2%2 = 0
      1
156(10진수) = 10011100(2진수)
```

## 문자세트

> 문자셋 (charset, Character Set)

하 나의 언어권에서 사용하는 언어를 표현하기 위한 모든 문자(활자)의 모임을 문자셋(charater set)이라고 한다.   
다시 말하면 우리가 얘기하는 언어를 책으로 출판할 때 필요한 문자(활자)를 모두 모은 것이라고 생각하면 된다. 추가적으로 부호와 공백 등과 같은 특수 문자도 문자셋에 포함된다.   

## 인코딩

> 인코딩 (encoding)

인코딩은 문자셋을 컴퓨터가 이해할 수 있는 바이트와 매핑하는 규칙이다.    
예를 들면 ASCII Code에서 A,B,C 등은 문자셋이고 A는 코드 65, B는 코드 66 등 바이트 순서와 매핑한 것이 인코딩이다.

## 최소공배수 알고리즘
```
a,b = 최소공배수를 구하고자 하는 두 수   
1. 최대공약수 구하기   
2. 최소공배수 = (a * b) / 최대공약수   
```

```a = 30 , b = 54```
> 1. 최대공약수 구하기 (유클리드 호제법)
```
def cgs(a,b) :
    while b!=0 :
        r = a%b
        a = b;
        b = r;
    return a;
```

> 2. 최소공배수 구하기
```
def lcm(a,b) :
    return a*b/cgs(a,b)
```
> 3. 결과
```int(lcm(30,54))```
= 270
