# 3주차 과제: 연산자 #

## 목표 ##
자바가 제공하는 다양한 연산자 학습하기.

* 연산자 : +,-와 같이 연산을 나타내는 기호를 의미한다.
* 수식 : 연산자와 피연산자로 구성된 수식을 의미한다.
* 연산자의 사용형태는 크게 3가지이다.
	* 단항 연산자 : 하나의 피연산자만을 가짐
	* 이항 연산자 : 하나의 연산자에 두개의 피연산자를 가짐
	* 삼항 연산자 : 3개의 피연산자를 가짐

## 1) 산술 연산자 ##
* 단항 연산자인 ++연산자와 --연산자는 피연산자로 변수만 사용 가능

|연산자|사용법|설명|비고|
|---|------|---------------|-----|
|+|op1+op2|op1과 op2를 더한다.|단항 및 이항|
|-|op1-op2|op1에서 op2를 뺀다.|단항 및 이항|
|*|op1*op2|op1과 op2를 곱한다.|이항|
|/|op1/op2|op1을 op2로 나눈다.|이항|
|%|op1%op2|op1을 op2로 나눈 나머지를 구한다.|이항|
|++|var++|var 값 1 증가. var 값 증가시키기 전에 평가|단항|
||++var|var 값 1 증가. var 값 증가시킨 후 평가|단항|
|--|var--|var 값 1 감소. var 값 감소시키기 전에 평가|단항|
||--var|var 값 1 감소. var 값 감소시킨 후 평가|단항|

```java
public class week03{
     public static void main(String []args){
        int a=5, b=2;
        
        int sum = a+b;
        System.out.println("a+b=" + sum); // output 7
        int sub = a-b;
        System.out.println("a-b=" + sub); // output 3
        int mul = a*b;
        System.out.println("a*b=" + mul); // output 10
        int div = a/b;
        System.out.println("a/b=" + div); // output 2
        int mod = a%b;
        System.out.println("a%b=" + mod); // output 1
        int prefixA = ++a;
        System.out.println("a의 전위 증가:" + prefixA); // output 6
        System.out.println("변수 a의 값" + a); // output 6
        int postfixB = b++;
        System.out.println("b의 후위 증가:" + postfixB); // output 2
        System.out.println("변수 b의 값" + b); // output 3
     }
}
```

* 산술 연산자 사용 시 정수의 경우는 int형으로 연산 수행
* 산술 연산자 사용 시 실수인 경우는 double형으로 연산 수행
```java
public class week03{
     public static void main(String []args){
        // 자료형이 나타낼 수 있는 범위를 벗어난 사용과 형 변환의 예
        byte a=127, b=2;
        
        byte c = (byte)(a*b);
        System.out.println("a*b의 결과를 byte로 변환 출력:" + c); // output -2
        /*
            정수연산(a*b)은 묵시적으로 int형으로 실행된다.
            a*b는 int형으로 수행하고, byte형으로 변환하여 저장된다.
            계산된 결괏값은 254이며 byte형이 표현할 수 있는 범위를 벗어나므로
            하위 8비트만 표현되어 -2가 출력된다.
        */
        
        int d = a*b;
        System.out.println("a*b의 결과를 int로 출력:" + d); // output 254
        
        int i = 1_000_000, j=1_000_000;
        int k = i*j;
        System.out.println("백만*백만의 결과를 int로 출력:" + k); // output -727379968
        /* 백만*백만의 결과가 int형 표현 범위를 벗어나므로 하위 32비트만 표현*/
        
        long m = (long)(i*j);
        System.out.println("a*b의 결과를 long으로 변환 출력:" + m); // output -727379968
        /* int 연산이 실행되며 그 결과가 이미 int를 벗어난다. */
        
        m = (long)i*j;
        System.out.println("i를 long으로 변환 후 연산:" + m); // output 1000000000000
        /* 변수가 long형이므로 long 연산이 실행된다.*/
        
        m = (long)i*(long)j;
        System.out.println("i와 j를 long으로 변환 후 연산" + m); // output 1000000000000
        /* long 연산이 실행된다.*/
        
     }
}
```

           
## 2) 비트 연산자 ##
* 비트 연산자 : 2진수로 표현된 정수를 비트 단위로 취급하는 연산자이다.
* 비트논리 연산자와 비트 시프트 연산자로 구분한다.
|연산자|사용법|설명|
|---|-----|--------------------|
| & | 5&7 | 5에 해당하는 101과 7에 해당하는 111을 비트 단위로 AND한다. |

## 3) 관계 연산자 ##
|연산자|사용법|설명|
|---|---------|---------------|
|>|op1>op2|op1이 op2보다 큰 경우|
|>=|op1>=op2|op1이 op2보다 크거나 같은 경우|
|<|op1<op2|op1이 op2보다 작은 경우|
|<=|op1<=op2|op1이 op2보다 작거나 같은 경우|
|==|op1==op2|op1과 op2가 같은 경우
|!=|op1!=op2|op1과 op2가 같지 않은 경우
|instanceof|op1 instanced op2|op1이 op2의 객체인 경우|


## 4) 논리 연산자 ##
|x|y| x||y | x&&y|
|-----|-----|-----|-----|

## 5) instanceof ##


## 6) assignment(=) operator ##


## 7) 화살표(->) 연산자 ##


## 8) 3항 연산자 ##


## 9) 연산자 우선 순위 ##


## 10) (optional) Java 13. switch 연산자 ##


## 참고 ##
* **Java in a Nutshell**, *Benjamin J.Evans David Flanagan*