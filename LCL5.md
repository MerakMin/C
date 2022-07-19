혼자 공부하는 C 언어

Chapter 05. 선택문(if, switch ~ case)

□ 제어문 - 특정 조건에 따라 실행하거나 실행하지 않아야 할 때 사용하는 문장

선택문 : if문, swith ~ case문

반복문 : for문, while문, do~while문

분기문 : break문, continue문, return문

​

□ 블록 block

함수, 반복문, 선택문 등의 중괄호로 이루어진 단위를 말한다.

if (조건식)

{

· · ·              ( {···} = 이것이 블록! 실행문이 하나 뿐이라면 중괄호 생략 가능 )

}

​

□ 조건문 conditional statement

특정 조건을 만족할 때 코드를 실행하는 문법

if문 : 괄호 내의 조건식이 참이면 블록 내의 문장을 실행한다

else : if문의 조건식이 거짓이면 블록 내의 문장을 실행한다. 필요 없으면 없어도 된다.

else if문 : if문의 조건식이 거짓일 때 실행시킬 코드에 추가 조건을 걸고 싶을 때 사용한다. 마찬가지로 필요 없으면 else if를 사용하지 않아도 된다.

#include<stdio.h>'

int main()

{

  if (a > 0)

     printf("a는 양수입니다.\n"); // 중괄호를 사용하지 않으면 조건식이 참일 때 한 줄만 실행

  else if (a == 0)

  {

    printf("a는 0입니다.\n");

  }

  else

  {

    printf("a는 음수입니다.\n");

  }

}

​

□ 매달린 esle 문제 Dangling esle Problem

if문을 중첩해서 사용할 때 뒤따르는 esle의 위치가 모호해지면서 생기는 문제

​

□ switch ~ case문

여러 선택지 중 만족하는 선택지의 코드를 실행하는 문법

switch문 : 괄호에 비교대상을 넣어 블록내의 각 case문을 검사한다

case : 'case(해당하는 값) : '과 같이 적는다. 해당하는 값은 비교대상 변수에 맞는 자료형의 데이터를 적는다. 정수, 문자, 열거상수 들이 될 수 있다.

default : 어떤 케이스도 비교 대상과 맞지 않을 때 이 문장을 실행할 수 있다. case문을 모두 적은 후 마지막에 적을 수 있으므로, 위의 case문에 해당하지 않을 떄 실행시키는 용도로 사용할 수 있다.

break문 : 반복문, 선택문 블럭을 빠져나오게 하는 예약어

#include<stdio.h>

int main()

{

  switch (ch)

  {

    case 'a' : // 이 케이스에서 break 문이 없기 때문에 블록을 빠져나가지 않고 다음 case 문으로 넘어간다.

    case 'b' :

         printf("ch는 a 혹은 b입니다\n"); // a일 경우에도 출력된다.

         break;

    case 'c' :

         printf("ch는 c입니다\n");

         break;

   default :

         printf("a도 b도 c도 아닙니다\n");

         break; // 이 break문을 적지 않아도 이 블록을 빠져나갈 수 있다.

  }

}

​

□ 분할 정복 기법 divide and conquer

재귀에 기반하여 큰 문제를 작게 쪼개 해결하여 결과를 취합하는 문제 해결 기법