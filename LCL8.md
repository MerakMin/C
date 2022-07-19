혼자 공부하는 C 언어

Chapter 08. 배열

□ 배열 array

기본 자료형을 여러 묶어서 사용하는 것. 인덱스를 가지고 순차적으로 순회하며 변수에 접근할 수 있다.

배열 선언 : 어떤 이름을 가지고 어떤 형태의 변수가 몇 개인지를 컴파일러에 알리는 것

#include<stdio.h>

int main()

{

  int ary[5] = {1, 2, 3, 4, 5};

  for (int i = 0; i < 5; i++)

  {

    printf("%d", ary[i]);

  }

}

​

□ 첨자 index

배열에서 순차적으로 나열된 요소에 매겨진 번호. 요소에 접근할 때 사용한다. 영문명 그대로 인덱스라고도 한다.

​

□ sizeof 연산자

변수가 메모리에 할당된 크기를바이트 단위로 반환하는 함수

#include<stdio.h>

int main()

{

  int ary[5] = {1, 2, 3, 4, 5};

  printf("%d", sezeof(sry)); // 출력 : 20

  

  (int *)malloc(sizeof(int) * n);

}