혼자 공부하는 C 언어

Chapter 12. 문자열

□ gets 함수

stdin 스트림 파일로부터 한 줄의 데이터를 읽는 함수

#include<stdio,h>

int main()

{

  // gets()의 함수 원형

  char *gets (char *str);

  return 0;

}

​

□ strcpy 함수

문자열을 복사한다.

#include<stdio.h>

int main()

{

  // strcpy()의 함수 원형

  char *strcpy (char *dest, const char* src);

  return 0;

}