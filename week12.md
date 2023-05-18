# C언어 12주차

<h3><b> ● 정올 1291번 </b></h3>

```
#include <stdio.h>
int main(void) {
    int s, e;
    
    while (1) {
        printf("시작 범위 입력(2부터 9까지의 정수): ");
        scanf("%d", &s);
        
        printf("끝 범위 입력(2부터 9까지의 정수): ");
        scanf("%d", &e);
        
        if (s < 2 || s > 9 || e < 2 || e > 9) /*거짓일 때 */ {
            printf("INPUT ERROR! 올바른 범위를 입력하세요.\n");
        } else {
            break;  // 올바른 범위 입력이므로 반복문 종료
        }
    }
    
    if (s > e) {
        int temp = s;
        s = e;
        e = temp;
    }
    
    for (int i = 1; i <= 9; i++) /*for(초기값; 조건식; 증감식)*/ 
        {
        for (int j = s; j <= e; j++) {
            printf("%d * %d = %2d ", j, i, j * i);
        }
        printf("\n");
    }
    
    return 0;
}
```
ㄴ 오답 : 4 3 입력시 [3단 , 4단] 으로 출력됨

```
#include <stdio.h>
int main(void) {
    int s, e;
    
    while (1) {
        printf("구구단의 시작 범위를 입력하세요 (2부터 9까지의 정수): ");
        scanf("%d", &s);
        
        printf("구구단의 끝 범위를 입력하세요 (2부터 9까지의 정수): ");
        scanf("%d", &e);
        
        if (s < 2 || s > 9 || e < 2 || e > 9) {
            printf("INPUT ERROR! 올바른 범위를 입력하세요.\n");
        } else {
            break;  // 올바른 범위 입력이므로 반복문 종료
        }
    }
    
    if (s > e) {
        for (int i = 1; i <= 9; i++) {
            for (int j = s; j >= e; j--) {
                printf("%d * %d = %2d   ", j, i, j * i);
            }
            printf("\n");
        }
    } else {
        for (int i = 1; i <= 9; i++) {
            for (int j = s; j <= e; j++) {
                printf("%d * %d = %2d ", j, i, j * i);
            }
            printf("\n");
        }
    }
    
    return 0;
}
```
ㄴ 정답

<hr>

<h3><b> ● 배열 </b></h3>

* 배열 난수로 채우기

```
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#define SIZE 5

int main(void)
{
    int i;
    int scores[SIZE];

    srand((unsigned)time(NULL));
    
    for(i=0; i < SIZE; i++)
        scores[i] = rand() % 100;
        
    for(i=0; i < SIZE; i++)
        printf("scores[%d]=%d\n", i, scores[i]);
        
    return 0;
}
```

```
scores[0]=58
scores[1]=16
scores[2]=30
scores[3]=31
scores[4]=47
```
ㄴ 결과

<hr>

* 예제3 : 성적 평균 계산하기

```
# 학생 5명의 성적 평균을 구하는 프로그램을 배열을 이용하여 작성해보자.
<br>배열을 사용하지 않고 5개의 변수를 사용했다면 얼마나 힘들었을 지를 상상하여보자.
```

```
#include <stdio.h>
#define STUDENTS 10

int main(void)
{
    int scores[STUDENTS];
    int sum = 0;
    int i, average;
    
    for (i=0; i < STUDENTS; i++)
    {
        printf("학생들의 성적을 입력하시오:");
        scanf("%d, &scores[i]");
    }
    
    for (i=0; i < STUDENTS; i++)
        sum += scores[i];
    
    average = sum / STUDENTS;
    printf("성적 평균 = %d\n", average);
    
    return 0;
}
```

