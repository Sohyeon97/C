# 4주차 C언어 실습
 - 4주차 복습
   
   https://codingadinga.tistory.com/11 <br>
   ++i : 선위연산자 : 증가<br>
   https://www.acmicpc.net/problem/2588 : 오늘 문제
   
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

```

#include <stdio.h>

int main(void)
{
    int x=10, y=10;

    printf("x=%d\n",x);
    printf("++x의 값=%d\n", ++x);
    printf("x=%d\n\n", x);

    printf("x=%d\n",y);
    printf("y++의 값=%d\n", y++);
    printf("y=%d\n\n", y);


    return 0;
}

```


Q. 편의점에서 물건을 구입하고 만 원을 냈을 때, 거스름돈의 액수와 점원이<br>
지급해야 할 거스름돈을 화폐와 동전수를 계산하는 프로그램을 작성해보자.

*조건 : 물건 값을 입력하시오: 8600 <br>
       투입한 금액을 입력하시오: 10000<br>
       거스름돈은 다음과 같습니다.<br>
       천원권: 1장<br>
       오백원 동전: 0개<br>
       백원 동전: 4<br>

```

#include <stdio.h>
int main(void)
{
    int money, change;
    int price, c5000, c1000, c500, c100;

    printf("물건 값을 입력하시오: ");
    scanf("%d", &price); 

    printf("투입한 금액을 입력하시오: ");
    scanf("%d", &money); 

    change = money - price; 
    c1000 = change / 1000;
    change = change % 1000; 
    c500 = change / 500;  
    change = change % 500; 

    printf("\n천원권: %d장\n", c1000);
    printf("오백원 동전: %d개\n", c500);
    printf("백원 동전: %d개\n", c100);

    return 0;
}

```
