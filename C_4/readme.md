# 4주차 C언어 실습
 - 4주차 복습
   (복습 내용)
   ~~~ 
   
 - 4주차 실습

```
#include <stdio.h>

int main() {
    
    double x, y, result;

    printf ("두 개의 실수를 입력하시오: ");
    scanf("%lf %lf" &x, &y);

    result = x + y;
    printf("%f / %f = %f", x, y, result);

    result = x / y;
    printf("%f / %f = %f", x, y, result);

return 0;
}
```