혼자 공부하는 C 언어

Chapter 16. 

□ stdlib.h 헤더 파일

메모리 동적 할당이나 문자열을 정수로 변환하는 함수 등 다양한 기능의 범용 함수가 정의된 헤더 파일.

​

□ 동적 할당 dynamic allocation

프로그램 실행 중에 저장 공간을 할당하는 것. 주로 코드 실행 중에 배열에 저장할 값의 개수가 결정되는 경우에 사용된다.

#include<stdio.h>

int main()

{

  int *arr;

  · · ·

  arr = (int *)malloc(sizeof(int) * n);

  return 0;

}

​

□ 메모리 누수 memory leak

메모리 공간을 사용하고 나서 반환하지 않았을 때 할당된 채로 사용하지 않는 공간이 생기는 것.

누스 → 새어나감 → 내용물 부족해짐

→ 메모리 공간이 새어나갈 빈 공간이 부족한 상태.

​

□ 명령행 인수 command line argument

명령행에서 프로그램을 실행시킬 때 프로그램의 이름 외에 함께 주는 프로그램에 필요한 정보

$ ./HongongExample arg1 arg2 → 리눅스 계열

C:\> HongongExample arg1 arg2 → 윈도우

#include<stdio.h>

int main(int argc, char** argv)

· · ·

→ int argc = 명령행 인수의 개수. 프로그램의 이름을 포함하기 때문에 항상 1 이상이다.

→ char** argv = 명령행 인수를 가진 이차원 배열. 문자열을 가진 배열이라고 생각하면 된다.

argv[0] : HongongExample

argv[1] : arg1

argv[2] : arg2