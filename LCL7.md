혼자 공부하는 C 언어

Chapter 07. 함수

□ 함수 function

기능을 수행하는 코드 단위

함수 정의 : 함수를 실제 코드로 만드는 것

함수 호출 : 함수를 필요로 하는 곳에서 사용하는 것

함수 선언 : 프로그램의 상단에서 어떤 함수를 만들어서 쓸 것이라고 컴파일러에 정보를 주는 것

함수 원형 : 함수명, 매개변수, 반환형을 적은 것

​

□ 함수 원형을 선언하는 이유

컴파일러가 함수를 호출하는 코드를 만나기 전에, 매개변수가 어떤 자료형이고 몇 개인지 알려 잘못된 매개변수를 전달하면서 생기는 에러를 막을 수 있도록 한다.

​

□ 재귀호출 함수 recursive function

함수 안에서 자신을 호출하는 함수

*재귀함수에 들어가야할 코드

1. 종료 조건을 검사하는 코드

2. 재귀를 하며 수행할 코드 (출력 등)

3. 자기 자신을 호출하는 코드

​

□ 어떤 상황에서 재귀를 쓰나요?

재귀 함수는 반복문을 쓴느 경우보다 간결한 코드로 구현할 수 있다는 장점이 있다. 혹은 반복문보다 많은 메모리를 쓰는 대신 비교적 빠른 작업을 할 수 있는 문제들이 있는데, 일부 정렬 알고리즘이 그런 경우이다.

​

□ 매개변수 parameter

함수가 처리할 데이터를 저장하는 변수

​

□ 인수(argument)와 매개변수(parameter)

#include<stdio.h>

int main()

{

  int result = 0;

  for (int i = 0; i < length; i++)

  {

    result += arr[i];

  }

  return result;

}

. . .

int myVar = mySum (myArray, 6);

. . .