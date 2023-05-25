# C언어 13주차
- 정올 1430번 : 숫자의 갯수

```
#include <stdio.h>
int main(void){
    
    int a=150, b=266, c=427, sum=0, count=0; //scanf("%d %d %d", &a, &b, &c);
    char t[10]={0};
    
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    
    sum = a*b*c
    printf("sum:%d\n",sum);
    
    while(1)
    {
        count = sum % 10;
        sum /= 10;
        t[count]++;
        
        if(sum==0)
        {
            break;
        }
    }
    for (int i=0; i <= 9; i++)
    {
        printf("%d\n", t[i]);
    }
    return 0;
}
```

ㄴ 오류 
