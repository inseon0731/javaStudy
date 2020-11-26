# 3주차 과제: 연산자 #

## 목표 ##
자바가 제공하는 다양한 연산자 학습하기.

## 1) 산술 연산자 ##
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

## 2) 비트 연산자 ##


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