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
